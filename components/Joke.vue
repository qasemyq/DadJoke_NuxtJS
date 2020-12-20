<template>
    <nuxt-link :to="'/jokes/' + id"> 
       <div>
            <p>{{joke}}</p>
       </div>
    </nuxt-link>
</template>

<script>
export default {
    name: 'joke',
    props: ['joke', 'id']
} 

</script>