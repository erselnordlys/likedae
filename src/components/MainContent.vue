<template xmlns:v-on="http://www.w3.org/1999/xhtml" xmlns:v-bind="http://www.w3.org/1999/xhtml">
  <div id="main">
    <div id="header" class="header">
      <div class="user">
        <div class="user-name">{{msg.user}}</div>
      </div>
    </div>
    <div id="dialogue" class="header">{{msg.dialogue}}</div>
    <div id="data">
      <applications class="container"></applications>
      <div id="container-2" class="container"></div>
      <div id="container-3" class="container"></div>
    </div>
  </div>
</template>

<script>
  import Applications from './Applications.vue'
  export default {
    name: '',
    data () {
      return {
        msg: {
          dialogue: 'ДИАЛОГОВОЕ ОКНО',
          user: 'Александр'
        }
      }
    },
    components: {
      applications: Applications
    }
  }
</script>

<style scoped>
  #main {
    background: #e5e5e5;
    display: flex;
    flex-direction: column;
    height: 100%;
    width: 100%;
  }
  .header {
    display: flex;
    height: 80px;
  }
  #header {
    background: #fff url('../assets/logo.png') 30px 50% / 130px 23px no-repeat;
    justify-content: flex-end;
    padding: 0 30px;

  }

  .user {
    align-items: center;
    background: url('../assets/photo.png') left / 50px 50px no-repeat;
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    width: 210px;
  }

  .user-name {
    background: url('../assets/caret-down.png') right/ 10px 10px no-repeat;
    font-size: 20px;
    margin-left: 60px;
    width: 150px;
  }

  #dialogue {
    align-items: center;
    background: #f8f8f8;
    color: #d39c00;
    display: flex;
    font-size: 16px;
    padding: 0 30px;
  }

  #data {
    background: #e5e5e5;
    display: flex;
    justify-content: space-between;
    padding: 30px 35px;
  }

  .container {
    background: #fff;
    border: 1px solid black;
    display: flex;
    max-height: 750px;
    margin-bottom: 190px;
    width: 27%;
  }
  #container-2 {
    width: 46%;
    margin: 0 30px;
  }

  #container-3 {
  }
</style>
