<template xmlns:v-on="http://www.w3.org/1999/xhtml" xmlns:v-bind="http://www.w3.org/1999/xhtml">
  <div id="sm-button"  v-bind:class="current" @click="renderIcons">
    <div v-bind:class='elementClass' class="icon"></div>
    <!--<div class="text" v-if="text">{{msg}}</div>-->
  </div>
</template>

<script>

  export default {
    name: 'SMButton',
    data () {
      return {
        classes: {0: 'inst-icon', 1: 'fb-icon', 2: 'vk-icon', 3: 'ok-icon', 4: 'tw-icon'},
        msg: 'Название соц. сети',
        text: false
      }
    },
    props: ['index'],
    computed: {
        elementClass: function () {
            console.log('rendering')
          console.log(this.cls)
            if (this.index == 3) {
              this.text = true;
            }
          return this.cls[this.index - 1];
        },

      current: function () {
        if (this.index == 3) {
            return 'current';
        }
      },

      cls: function () {
        return this.classes;
      }
    },
    methods: {
      renderIcons: function () {
          console.log('render')
        let clicked = this.classes[this.index - 1]; // ok
        let prev = this.classes[2]; // vk
        let classes = this.classes;

        let obj = {};

        for (let i = 0; i < 5; i++) {
            console.log(i)
          if (classes[i] == clicked) {
            console.log(obj)

            obj[2] = clicked;
            console.log(obj);
          } else if (classes[i] == prev) {
                obj[this.index - 1] = prev;
                console.log('prev placed')
            console.log(obj);

          } else {
                obj[i] = classes[i];
          }
        }

//        this.classes = obj;
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
   height: 100%;
   width:50px;
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
