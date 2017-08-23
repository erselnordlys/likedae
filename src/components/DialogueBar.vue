<template xmlns:v-on="http://www.w3.org/1999/xhtml" xmlns:v-bind="http://www.w3.org/1999/xhtml">
  <div id="dialogue"> {{msg}}

    <div class="durations">
      <div class="respond-app respond">
        <div class="text">{{respondApp}}</div>
        <div class="number">{{numApp}}</div>
        <div class="info"></div>
      </div>
      <div class="respond-chat respond">
        <div class="text">{{respondChat}}</div>
        <div class="number">{{numChat}}</div>
        <div class="info"></div>
      </div>
    </div>
  </div>
</template>

<script>

  export default {
    name: 'DialogueBar',
    data () {
      return {
        msg: 'ДИАЛОГОВОЕ ОКНО',
        respondApp: 'Среднее время ответа на заявку (мин.)',
        respondChat: 'Среднее время ответа в чате (мин.)',
        numApp: 230,
        numChat: 30
      }
    }
  }
</script>

<style scoped>
  #dialogue {
    align-items: center;
    background: #f8f8f8;
    color: #d39c00;
    display: flex;
    justify-content:space-between;
    font-size: 16px;
    min-width: 400px;
    padding-left:30px;
    width: auto;
  }

  .durations {
    align-items: center;
    display: flex;
    flex-direction: row;
    height: 100%;
    width: auto;
  }

  .respond {
    align-items: center;
    color: #383838;
    flex-direction: row;
    display: flex;
    height: 60px;
    padding-right: 30px;
    width: auto;
  }

  .respond:last-child {
    border-left: 1px solid #e5e5e5;
    padding-left: 30px;
  }

  .text {
    text-align: end;
    width: auto;
    max-width: 180px;
  }

  .number {
    color: #d39c00;
    font-size: 40px;
    margin-left: 15px;
  }

  .info {
    background: url('../assets/fa-question-circle.png') top / 15px 15px no-repeat;
    height: 80%;
    width: 15px;
  }

</style>
