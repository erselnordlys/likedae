<template xmlns:v-on="http://www.w3.org/1999/xhtml" xmlns:v-bind="http://www.w3.org/1999/xhtml">
  <div id="messages">
    <div class="msgFromManager message">
      <div class="photo"></div>

      <div class="info-text">
        <div class="info">
          <div class="name manager"> {{msg.manager}}</div>
          <div class="date">{{msg.date}}</div>
        </div>
        <div class="text">{{msg.msgFromManager}}</div>
      </div>
    </div>

    <div class="msgFromCustomer message">
      <div class="photo"></div>
      <div class="info-text">
        <div class="info">
          <div class="name"> {{msg.name}}
            <div class="sm">{{msg.sm}}</div>
          </div>
          <div class="date">{{msg.date}}</div>
        </div>
        <div class="text">{{msg.msgFromCustomer}}</div>
      </div>
    </div>
  </div>
</template>

<script>

  export default {
    name: 'ChatMessage',
    data () {
      return {
        msg: {
          name: 'Александр Александрович',
          sm: 'Иван Щедрый',
          manager: 'Менеджер',
          date: '27 декабря 22:00',
          msgFromManager: '1. в первой записи изменить "индивидуальным" на "уникальным". ' +
          'Вторая вообще не нравится, но идей так и не появилось. Тавтология и язык сломала, ' +
          'пока прочла ',
          msgFromCustomer: '1. в первой записи изменить "индивидуальным" на "уникальным". ' +
          'Вторая вообще не нравится, но идей так и не появилось. Тавтология и язык сломала, ' +
          'пока прочла 2. вместо красной полосы написать сделать раздел "Почему именно мы?",' +
          ' снизу картинки + подписи. Пример прикрепила. У нас будет четыре графы. 1) 300+ ' +
          'моделей чехлов на разные телефоны. 2) 3 варианта дизайна 3) 15 минут изготовление ' +
          'чехла (отправка в тот же день) 4) Делаем из качественных материалов и используем современное оборудование.'
        }
      }
    }
  }
</script>

<style scoped>
  #messages {
    height: auto;
    overflow: auto;
  }

  .msgFromManager,
  .msgFromCustomer{
    padding: 27px 20px 20px;
    height: 100%;
  }


  .msgFromManager {
    background: #f8f8f8;
  }

  .message {
    display: flex;
    flex-direction: row;
  }

  .photo {
    background: url('../assets/photo.png') top / 100% no-repeat;
    cursor: pointer;
    height: 65px;
    margin-right: 15px;
    min-height: 40px;
    min-width: 40px;
    width: 65px;
  }

  .info {
    display: flex;
    justify-content: space-between;
  }

  .info-text {
    display: flex;
    flex-direction: column;
    height: auto;
    width: auto;
  }

  .name {
    color: #383838;
    cursor: pointer;
    font-size: 16px;
    font-weight: bold;
    line-height: 18px;
    padding-bottom: 15px;
    width: auto;
  }

  .manager {
    color: #65a3e5;
  }

  .sm {
    background: url('../assets/vk-grey.png') left / 15px 10px no-repeat;
    color: #606060;
    cursor: pointer;
    font-size: 12px;
    font-weight: normal;
    padding-left: 25px;
  }

  .date {
    background: url('../assets/clock.png') 0 2px / 14px 14px no-repeat;
    font-size: 12px;
    line-height: 18px;
    padding-left: 24px;
  }
  .text {
    font-size: 14px;
    line-height: 18px;
  }

</style>
