<template>
  <div class="list">
    <div class="list-title" v-if="title">{{title}}</div>
    <div class="list-subtitle" v-if="subtitle">Subtitle</div>
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "List",
  props: ["title", "subtitle"]
};
</script>