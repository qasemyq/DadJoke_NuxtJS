<template>
  <div >
   <Joke v-for="joke in jokes"
   :key="joke.id"
   :id="joke.id"
   :joke="joke.joke"
   />

  </div>
</template>

<script>
import Joke from '@/components/Joke.vue'
import axios from 'axios'

export default {
    components: {
        Joke
    },
    async asyncData (){
        const config = {
            headers: {
                Accept : "application/json"
            }
        }
        try {
            let res = await axios.get('https://icanhazdadjoke.com/search', config);
            return {jokes : res.data.results}
        } catch (error) {
            console.log(error);
        }
    },

}
</script>