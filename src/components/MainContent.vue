<template xmlns:v-on="http://www.w3.org/1999/xhtml" xmlns:v-bind="http://www.w3.org/1999/xhtml">
  <div id="main">
    <div id="header" class="header">
      <div class="user">
        <div class="user-name">{{msg.user}}</div>
      </div>
    </div>
    <dialogue class="header"></dialogue>

    <div id="data">
      <applications class="container"></applications>
      <chat class="container"></chat>
      <info class="container"></info>
      <!--<div id="container-3" class="container"></div>-->
    </div>
  </div>
</template>

<script>
  import Applications from './Applications.vue'
  import Dialogue from './DialogueBar.vue'
  import Chat from './Chat.vue'
  import Info from './Info.vue'
  export default {
    name: '',
    data () {
      return {
        msg: {
          user: 'Александр'
        }
      }
    },
    components: {
      applications: Applications,
      dialogue: Dialogue,
      chat: Chat,
      info: Info
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
    padding-right: 20px;
  }

  #data {
    background: #e5e5e5;
    display: flex;
    justify-content: space-between;
    padding: 30px 35px;
  }

  .container {
    background: #fff;
    display: flex;
    max-height: 750px;
    margin-bottom: 190px;
    min-width: 300px;
    width: 27%;
  }
  .container:nth-child(2) {
    margin: 0 30px;
    min-width: 500px;
    width: 46%;
  }

</style>
