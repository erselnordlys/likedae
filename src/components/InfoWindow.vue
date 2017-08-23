<template xmlns:v-on="http://www.w3.org/1999/xhtml" xmlns:v-bind="http://www.w3.org/1999/xhtml">
  <div id="info">
    <div class="header">
      <div class="header-info active"></div>
      <div class="write"></div>
      <div class="filter"></div>
      <div class="payment"></div>
      <div class="settings"></div>
    </div>

    <div class='container'>
      <components></components>
    </div>
    <div class="blanc"></div>
  </div>
</template>

<script>
  import Content from './InfoContent.vue'
  export default {
    name: 'InfoWindow',
    data () {
      return {
      }
    },
    components: {
        components: Content
    }
  }
</script>

<style scoped>
  #info {
    background: #fff;
    display: flex;
    flex-direction: column;
    height: 100%;
    min-width: 230px;
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
    min-height: 80px;
  }

  .header div {
    align-items: center;
    display: flex;
    justify-content: center;
    width: 22.5%;
  }

  .header-info {
    background: url('../assets/info-circle.png') center / 20px 20px no-repeat;
  }

  .write {
    background: url('../assets/pencil-square.png') center / 20px 20px no-repeat;
  }

  .filter {
    background: url('../assets/filter.png') center / 20px 20px no-repeat;
  }

  .payment {
    background: url('../assets/credit-card.png') center / 20px 20px no-repeat;
  }

  .settings {
    background: url('../assets/fa-gear.png') center / 20px 20px no-repeat;
    border-left: 1px solid #65a3e5;
    flex-grow: 1;
    max-width: 35px;
    min-width: 30px;
  }

  .active {
    background-color: #65a3e5;
    position: relative;
  }

  .active:after {
    border-left: 12px solid transparent;
    border-right: 12px solid transparent;
    border-top: 15px solid #65a3e5;
    bottom: -14px;
    content: '';
    left: 50%;
    margin-left: -10px;
    position: absolute;
    width: 0;
    height: 0;
  }

  .container {
    height: 100%;
    overflow: auto;
  }
</style>
