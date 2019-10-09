<template>
  <div class="card">
    <img class="card-image" v-if="imageUri" :src="imageUri" :alt="imageTitle || title" />
    <div class="card-content">
      <div class="card-title" v-if="title">{{title}}</div>
      <div class="card-subtitle" v-if="subtitle">{{subtitle}}</div>
      <div class="card-text" v-if="text">{{text}}</div>
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ["text", "imageUri", "imageTitle", "subtitle", "title"]
};
</script>