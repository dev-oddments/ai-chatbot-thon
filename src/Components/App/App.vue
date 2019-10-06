<template>
  <div id="app" >
    <h1>hello</h1>

        <a href="#" @click="reset"><img class="fab" src="https://tva1.sinaimg.cn/large/006y8mN6gy1g7ov0vmo5pj30wc0a0wfk.jpg"/></a>
    <div v-show="resetView" class="modal" style="border-radius: 25px;box-shadow: 0 6px 14px 0 #666 ;width: 600px; height: 850px">
      <div style="border-radius: 25px 25px 0px 0px; display: flex; flex-flow: row wrap; justify-content: space-between;height: 80px; background: rgb(74,77,138)">
        <div style="padding-top: 15px; padding-left: 30px;">
            <div style="font-size: 23px;color:white;"><b>ChatBot</b></div>
            <div style="font-size: 15px;padding-top: 5px;color:white;">서울시 인공지능 챗봇</div>
        </div>
        <div style="padding-right:20px; padding-top:20px;">
            <a href="#" @click="reset"><div style="margin:auto; font-size: 30px;color:white;">  ✕ </div></a>
        </div>
      </div>
      <Chatting style="background-color:rgb(255,255,255)"  />
    </div>
  </div>
</template>

<script>
    import Chatting from './Chatting.vue'
            
    export default {
        name: 'App',
        components: {
            Chatting
        },
        data () {
            return {
                resetView: false,
            }
        },
        methods: {
            reset() {
                this.resetView = !this.resetView
            }
        }
    }
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Roboto:400,500,700')

.modal
   position: fixed
   right: 50px
   bottom: 50px

.fab
   width: 266px
   border-radius: 50px
   transition: all 0.1s ease-in-out
   font-size: 50px
   text-align: center
   line-height: 70px
   position: fixed
   right: 50px
   bottom: 50px

.fab:hover 
   transform: scale(1.05)

</style>
