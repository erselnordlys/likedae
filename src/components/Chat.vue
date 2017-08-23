<template xmlns:v-on="http://www.w3.org/1999/xhtml" xmlns:v-bind="http://www.w3.org/1999/xhtml">
    <div id="chat">
      <div class="header">
        <div class="link-icon"></div>
        <div class="name">{{msg.name}}</div>
        <div class="chat-icon"></div>
      </div>

      <div class="social-media">
        <div class="inst-icon"></div>
        <div class="fb-icon"></div>
        <div class="current"> <div class="vk-icon"></div> {{msg.smName}} </div>
        <div class="ok-icon"></div>
        <div class="tw-icon"></div>
      </div>

      <div class="messages">
        <messages v-for="item in 10"></messages>
      </div>
      <div class="blanc"></div>

      <div class="buttons">
        <div class="button">{{msg.btnYes}}</div>
        <div class="button">{{msg.btnNo}}</div>
      </div>

    </div>


</template>

<script>
  import Messages from './ChatMessage.vue'
    export default {
      name: 'Chat',
      data () {
            return {
                msg: {
                  btnYes: 'Взять в работу',
                  btnNo: 'Некачественный лид',
                  name: 'АЛЕКСАНДР АЛЕКСАНДРОВ',
                  smName: 'Название соц. сети'
                }
            }
        },
      components: {
          messages: Messages
      }
    }
</script>

<style scoped>
  #chat {
    background: #fff;
    display: flex;
    flex-direction: column;
    flex-grow: 1;
    height: 100%;
    min-width: 320px;
    position: relative;
  }
  ::-webkit-scrollbar {
    width: 4px;
  }

  ::-webkit-scrollbar-track {
    background: rgba(0, 0, 0, 0.1);
  }

  ::-webkit-scrollbar-thumb {
    background: #65a3e5;
  }

  .blanc {
    border-top: 1px solid #d3d3d3;
    min-height: 50px;
    width: 100%;
  }

  .header {
    background: #8dbbec;
    color: white;
    display: flex;
    flex-direction: row;
    font-size: 16px;
    justify-content: space-between;
    min-height: 80px;
  }

  .header div {
    align-items: center;
    cursor: pointer;
    display: flex;
    justify-content: center;
  }

  .name {
    color: white;
    cursor: pointer;
    font-size: 16px;
  }

  .link-icon {
    background: url('../assets/hover-link.png') center / 20px 20px no-repeat;
    cursor: pointer;
    height: 77px;
    width: 77px;
  }

  .chat-icon {
    background: url('../assets/chat-icon.png') center / 20px 20px no-repeat;
    cursor: pointer;
    height: 77px;
    width: 77px;
  }

  .buttons {
    align-self: center;
    cursor: pointer;
    display: flex;
    flex-direction: row;
    flex-grow: 1;
    height: auto;
    justify-content: space-between;
    position: absolute;
    bottom: -20px;
    width: 395px;
  }

  .button {
    align-items: center;
    background: #8dbbec;
    border-radius: 25px;
    color: white;
    cursor: pointer;
    display: flex;
    font-size: 18px;
    justify-content: center;
    height: 40px;
    min-width: 150px;
    padding: 0 10px;
    width: auto;
  }

  .button:last-child {
    background: #65a3e5;
  }

  .social-media {
    align-items: center;
    border-bottom: 1px solid #d3d3d3;
    display: flex;
    font-size: 14px;
    min-height: 80px;
    justify-content: center;
    padding: 0 15px;
    position: relative;
  }

  .social-media:after {
    bottom: -15px;
    border-left: 12px solid transparent;
    border-right: 12px solid transparent;
    border-top: 15px solid white;
    content: '';
    height: 0;
    position: absolute;
    width: 0;
  }

  .social-media:before {
    bottom: -17px;
    border-left: 14px solid transparent;
    border-right: 14px solid transparent;
    border-top: 17px solid #d3d3d3;
    content: '';
    height: 0;
    position: absolute;
    width: 0;
  }

  .social-media div {
    cursor: pointer;
    height: 60px;
    width: 10%;
  }

  .social-media .current {
    width: 60%;
    align-items: center;
    border-right: 1px solid #d3d3d3;
    border-left: 1px solid #d3d3d3;
    color: #65a3e5;
    cursor: auto;
    display: flex;
    font-size: 14px;
    line-height: 22px;
    justify-content: center;
  }

  .current div {
    padding-right: 10px;
  }

  .inst-icon {
    background: url('../assets/ig-icon.png') center / 20px 20px no-repeat;
  }

  .fb-icon {
    background: url('../assets/fb-cicon.png') center / 10px 18px no-repeat;
  }

  .vk-icon {
    background: url('../assets/vk-icon.png') center / 20px 13px no-repeat;
  }

  .ok-icon {
    background: url('../assets/ок-icon.png') center/ 12px 18px no-repeat;
  }

  .tw-icon {
    background: url('../assets/tw-icon.png') center / 18px 18px no-repeat;

  }

  .messages {
    height: auto;
    overflow: auto;
  }
</style>
