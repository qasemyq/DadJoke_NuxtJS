<template>
    <div>
        {{ joke }}
    </div>
</template>

<script>
import axios from 'axios'
export default {
   async asyncData({ params }) {
         const config = {
            headers: {
                Accept : "application/json"
            }
        }
        try {
            let res = await axios.get(`https://icanhazdadjoke.com/j/${ params.id }`, config);
            return { joke: res.data.joke  }
        } catch (error) {
            console.log(error);
        }
    },
        head(){
        return{
            title: 'Joke',
            meta: [
                {
                    hid: 'desciption',
                    name: 'desciption',
                    content: this.Joke
                }
            ]
        }
    }
}
</script>