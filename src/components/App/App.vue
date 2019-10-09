<template>
  <div id="app">
    <iframe
      src="https://www.seoul.go.kr"
      :scrolling="resetView ? `no`: `auto`"
      id="iframe"
      ref="iframe"
    />

    <div class="dim" v-if="resetView"></div>
    <div href="#" class="fab" @click="reset"></div>
    <div v-show="resetView" class="modal">
      <div class="modal-header">
        <div>
          <h3>ChatBot</h3>
          <p>서울시 인공지능 챗봇</p>
        </div>
        <div @click="reset" class="reset">✕</div>
      </div>
      <Chatting style="background-color:rgb(255,255,255)" />
    </div>
  </div>
</template>

<script>
import Chatting from "./Chatting.vue";

export default {
  name: "App",
  watch: {
    resetView(n) {
      if (n) {
        this.$nextTick(() => {
          var div = document.getElementById("chatArea");
          div.scrollTop = div.scrollHeight;
        });
      }
    }
  },
  components: {
    Chatting
  },
  data() {
    return {
      resetView: false
    };
  },
  methods: {
    reset() {
      this.resetView = !this.resetView;
    }
  }
};
</script>

<style lang="scss">
@import "../../scss/index.scss";
</style>
