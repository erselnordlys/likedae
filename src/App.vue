<template>
  <div id="app">
    <wrapper></wrapper>
  </div>
</template>

<script>
  import Wrapper from './components/Wrapper.vue'
  export default {
    name: 'app',
    components: {
      wrapper: Wrapper
    }
  }
</script>

<style>
  html{
    height: 100%;
  }

  body {
    background: #e5e5e5;
    height: 100%;
  }
  #app {
    align-items: center;
    /*background-color: #4b5151;*/
    background: pink;
    color: #5a5a5a;
    font-family: Helvetica, Arial, sans-serif;
    font-size: 17px;
    /*height: auto;*/
    height: 100%;
    margin: -10px;
  }
</style>
