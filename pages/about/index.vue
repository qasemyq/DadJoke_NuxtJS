<template>
  <div >
   <h1>About page</h1>
  </div>
</template>

<script>
export default {
    head(){
        return{
            title: 'About page',
            meta: [
                {
                    hid: 'desciption',
                    name: 'desciption',
                    content: 'This is About page'
                }
            ]
        }
    }
}
</script>