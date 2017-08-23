<template xmlns:v-on="http://www.w3.org/1999/xhtml" xmlns:v-bind="http://www.w3.org/1999/xhtml">
  <div id="content">
      <div class="info-card card">
        <div class="info-header">{{msg.mainInfo}}</div>
        <div class="info-block">
          <div class="line name">{{msg.name}}</div>
          <div class="line vk">{{msg.vk}}</div>
          <div class="line inst">{{msg.inst}}</div>
          <div class="line tele">{{msg.tele}}</div>
        </div>
      </div>

    <div class="info-card card">
      <div class="info-header">{{msg.addInfo}}</div>
      <div class="info-block">
        <div class="line compass">{{msg.compass}}</div>
        <div class="line location">{{msg.location}}</div>
      </div>
    </div>

    <div class="info-card card">
      <div class="info-header">{{msg.company}}</div>
      <div class="info-block">
        <div class="line vk">{{msg.vkCompany}}</div>
        <div class="line desktop">{{msg.desktop}}</div>
        <div class="line tele">{{msg.tele}}</div>
        <div class="line user-company">{{msg.userCompany}}</div>
        <div class="line location">{{msg.location}}</div>
      </div>
    </div>

  </div>
</template>

<script>

  export default {
    name: 'InfoContent',
    data () {
      return {
        msg: {
          mainInfo: 'ОСНОВНАЯ ИНФОРМАЦИЯ',
          addInfo: 'ДОПОЛНИТЕЛЬНАЯ ИНФОРМАЦИЯ',
          company: 'КОМПАНИЯ',
          name: 'Александр Александров',
          vk: 'id123456',
          inst: '@mruser',
          tele: '+7 999 899 00 11',
          compass: 'канал...',
          location: 'Воронеж',
          vkCompany: 'vk.com/vkgroup',
          desktop: 'desktop.com',
          userCompany: 'Иван Иванов'
        }
      }
    }
  }
</script>

<style scoped>
  .card {
    align-items: center;
    border-bottom: 1px solid #606060;
    color: #8a8a8a;
    display: flex;
    flex-direction: column;
    font-size: 16px;
    justify-content: center;
    line-height: 22px;
    width: 100%;
  }

  .info-header {
    align-items: center;
    background-color: #f8f8f8;
    color: #383838;
    display: flex;
    height: 35px;
    justify-content: center;
    width: 100%;
  }
  .info-block {
    color: #383838;
    height: auto;
    padding-top: 20px;
    width: 100%;
  }

  .line {
    align-items: center;
    background: 30px 0 / 20px 20px no-repeat;
    height: auto;
    padding-left: 80px;
    padding-bottom: 20px;
  }

  .name {
    background-image: url('../assets/user-circle копия.png');
  }

  .vk {
    background-image: url('../assets/vk-grey.png');
    background-position: 30px 3px;
    background-size: 20px 13px;
  }

  .inst {
    background-image: url('../assets/ig-dark.png');
  }

  .tele {
    background-image: url('../assets/phone-square.png');
  }

  .compass {
    background-image: url('../assets/ compass.png');
  }

  .location {
    background-image: url('../assets/map.png');
    background-position: 33px 0;
    background-size: 15px 20px;
  }

  .desktop {
    background-image: url('../assets/ desktop.png');
  }

  .user-company {
    background-image: url('../assets/user-company.png');
  }

</style>
