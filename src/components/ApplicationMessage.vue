<template xmlns:v-on="http://www.w3.org/1999/xhtml" xmlns:v-bind="http://www.w3.org/1999/xhtml">
  <div id="client">
    <div class="photo"></div>
    <div class="column">
      <div class="name">{{msg.name}}</div>
      <div class="message-text">{{msg.message}}</div>
    </div>
    <div class="column">
      <div class="time">{{msg.time}}</div>
      <div class="unread">{{msg.unread}}</div>
    </div>
  </div>
</template>

<script>

  export default {
    name: 'ApplicationMessage',
    data () {
      return {
          msg: {
            name: 'АЛЕКСАНДР АЛЕКСАНДРОВИЧ',
            message: 'В первой записи измен...',
            time: '22:00',
            unread: '10'
          }
      }
    }
  }
</script>

<style scoped>
  #client {
    align-items: center;
    border-bottom: 1px solid #d3d3d3;
    display: flex;
    height: 90px;
    padding: 0 15px;
  }

  .photo {
    background: url('../assets/photo.png') center / 100% no-repeat;
    height: 75px;
    margin-right: 15px;
    width: 75px;
  }

  .column {
    display: flex;
    flex-direction: column;
    height: 67px;
    justify-content: space-between;
  }
  .name {
    font-size: 14px;
    font-weight: bold;
    line-height: 18px;
  }

  .message-text {
    font-size: 14px;
    margin-bottom: 5px;
  }
  .time {
    font-size: 12px;
  }

  .unread {
    align-items: center;
    background: #65a3e5;
    border-radius: 50px;
    color: white;
    display: flex;
    font-size: 14px;
    justify-content: center;
    height: 27px;
    width: 27px;
  }
</style>
