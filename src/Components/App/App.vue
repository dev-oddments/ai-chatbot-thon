<template>
  <div id="app">
    <h1>hello</h1>
    <a href="#" @click="reset"><div class="fab"> + </div></a>
    <div v-show="resetView" class="modal" style="border-style: solid; width: 600px; height: 600px">
      <div>
        <a href="#" @click="reset"><div> close </div></a>
      </div>
      <Chatting  />
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
.modal
   position: fixed
   right: 50px
   bottom: 50px
   
.fab
   width: 70px
   height: 70px
   background-color: red
   border-radius: 50%
   box-shadow: 0 6px 10px 0 #666
   transition: all 0.1s ease-in-out
   font-size: 50px
   color: white
   text-align: center
   line-height: 70px
   position: fixed
   right: 50px
   bottom: 50px

.fab:hover 
   box-shadow: 0 6px 14px 0 #666
   transform: scale(1.05)

</style>