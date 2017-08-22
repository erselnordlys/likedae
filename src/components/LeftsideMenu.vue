<template xmlns:v-on="http://www.w3.org/1999/xhtml" xmlns:v-bind="http://www.w3.org/1999/xhtml">
  <div id="left-menu">
    <div class="button" id="menu-btn"></div>
    <div class="button"></div>
    <div class="button"></div>
    <div class="button"></div>

  </div>
</template>

<script>
  export default {
    name: '',
    data () {
      return {}
    }
  }
</script>

<style scoped>
  #left-menu {
    background: #606060;
    display: flex;
    flex-direction: column;
    height: auto;
    min-height: 100%;
    width: 80px;
  }

  .button {
    height: 80px;
    width: 80px;
  }

  #menu-btn {
    background: #383838;
  }

  .button:hover {
    background: #dcb033;
  }
</style>
