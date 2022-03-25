<template>
  <Blog />
</template>

<script>
  import Blog from './components/blog/Blog.vue'

  export default {
    name: 'App',
    components: {
      Blog
    }
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');

  *{
    font-family: 'Poppins', sans-serif;
    margin:0px;
    padding: 0px;
    box-sizing: border-box;
  }
  

</style>