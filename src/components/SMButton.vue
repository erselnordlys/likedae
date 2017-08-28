<template xmlns:v-on="http://www.w3.org/1999/xhtml" xmlns:v-bind="http://www.w3.org/1999/xhtml">
  <div id="sm-button" v-on:click="changeCurrentSM" v-bind:class="{current : isCurrent}">
    <div class="icon" v-if="vis" v-bind:class="elementClass"></div>

    <div  v-if="cur" class="cur-div">
      <div  class="icon" v-bind:class="elementClass"></div>
      <div class="text">{{msg}}</div>
    </div>
  </div>
</template>

<script>

  export default {
    name: 'SMButton',
    data () {
      return {
        msg: 'Название соц. сети'
      }
    },
    props: ['index', 'elementClass', 'isCurrent'],
    computed: {
      cur: function () {
        if (this.isCurrent) {
            return true;
        } else {
            return false;
        }
      },
      vis: function () {
        if (this.isCurrent) {
          return false;
        } else {
          return true;
        }
      }
    },
    methods: {
      changeCurrentSM: function() {
        this.$emit('changeCurrentSM', this.index)
      }
    }
  }
</script>

<style scoped>
 #sm-button {
   align-items: center;
   cursor: pointer;
   display: flex;
   justify-content: center;
   height: 60px;
 }

 .icon {
   height: 80px;
   width:50px;
 }

 .cur-div {
   display: flex;
   align-items: center;
   justify-content: center;
 }

 .inst-icon {
   background: url('../assets/ig-icon.png') center / 20px 20px no-repeat;
 }

 .fb-icon {
   background: url('../assets/fb-cicon.png') center / 10px 18px no-repeat;
 }

 .vk-icon {
   background: url('../assets/vk-grey.png') center / 22px 13px no-repeat;
 }

 .ok-icon {
   background: url('../assets/ок-icon.png') center/ 11px 20px no-repeat;
 }

 .tw-icon {
   background: url('../assets/tw-icon.png') center / 18px 18px no-repeat;

 }

</style>
