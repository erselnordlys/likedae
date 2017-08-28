<template xmlns:v-on="http://www.w3.org/1999/xhtml" xmlns:v-bind="http://www.w3.org/1999/xhtml">
  <div id="left-menu">
    <div class="button menu-btn"></div>
    <div class="button fire">
      <div class="fire-news news">{{msg.fire}}</div>
    </div>
    <div class="button comment">
      <div class="comment-news news">{{msg.comment}}</div>
    </div>
    <div class="button bell"></div>
    <div class="button calendar"></div>
    <div class="button fly"></div>
  </div>
</template>

<script>
  export default {
    name: 'LeftsideMenu',
    data () {
      return {
        msg: {
          fire: '300',
          comment: '30'
        }
      }
    }
  }
</script>

<style scoped>
  #left-menu {
    background: #606060;
    display: flex;
    flex-direction: column;
    flex-grow: 1;
    height: auto;
    min-width: 60px;
    width: 80px;
  }

  .button {
    cursor: pointer;
    height: 80px;
    position: relative;
  }

  .button:hover {
    background-color: #dcb033;
  }

  .menu-btn {
    background: #383838 url('../assets/fa-navigation.png') center / 18px 18px no-repeat;
  }

  .fire {
    background: url('../assets/ fa-fire.png') 20px 50% / 18px 18px no-repeat;
  }

  .comment {
    background: url('../assets/ fa-commenting.png') 20px 50%  / 18px 18px no-repeat;
  }
  .bell {
    background: url('../assets/ fa-bell.png') center / 18px 18px no-repeat;
  }

  .calendar {
    background: url('../assets/calendar.png') center / 18px 18px no-repeat;
  }

  .fly {
    background: url('../assets/ fa-fly.png') center / 18px 18px no-repeat;
  }

  .news {
    align-items: center;
    border-radius: 20px;
    color: white;
    cursor: pointer;
    display: flex;
    height: 30px;
    justify-content: center;
    margin-top: -15px;
    position: absolute;
    right: -10px;
    top: 50%;
    width: 40px;

    transition: all 0.5s;
  }

  .news:hover {
    height: 32px;
    margin-top: -16px;
    right: -12px;
    width: 44px;
  }

  .fire-news {
    background: #d86a43;
  }

  .comment-news {
    background: #65a3e5;
  }
</style>
