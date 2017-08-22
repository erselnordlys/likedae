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
    margin: 0;
  }
  #app {
    align-items: center;
    background-color: #4b5151;
    color: #5a5a5a;
    /*display: flex;*/
    font-family: Helvetica, Arial, sans-serif;
    font-size: 17px;
    /*justify-content: center;*/
    height: 100%;
    margin: -10px;
  }
</style>
