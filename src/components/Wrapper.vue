<template xmlns:v-on="http://www.w3.org/1999/xhtml" xmlns:v-bind="http://www.w3.org/1999/xhtml">
  <div id="wrapper">
    <leftside-menu></leftside-menu>
    <main-content></main-content>
  </div>
</template>

<script>
  import LeftsideMenu from './LeftsideMenu.vue'
  import MainContent from './MainContent.vue'
  export default {
    name: 'Wrapper',
    data () {
      return {}
    },
    components: {
      'leftside-menu': LeftsideMenu,
      'main-content': MainContent
    }
  }
</script>

<style scoped>

  #wrapper {
    background-color: #fff;
    display: flex;
    flex-direction: row;
    flex: 1;
    justify-content: center;
    height: 100%;
    width: 100%;
  }
</style>
