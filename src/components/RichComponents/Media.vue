<template>
  <div class="media">
    <img class="media-image" v-if="iconUri" :src="iconUri" :alt="iconTitle" />
    <div class="media-content">
      <div class="media-title" v-if="name">{{name}}</div>
      <div class="media-subtitle" v-if="description">{{description}}</div>
    </div>
    <audio class="media-controls" controls :src="uri" />
  </div>
</template>

<style lang="scss" scoped>
.media {
  padding: 16px;
  border-radius: 12px;
  background-color: white;
  box-shadow: 0 2px 6px 2px rgba(60, 64, 67, 0.15);
}
.media-title {
  font-weight: 500;
  font-size: 20px;
  line-height: 30px;
  color: #202124;
}
.media-subtitle {
  line-height: 24px;
  color: #70757a;
}
.media-content {
  display: inline-block;
  vertical-align: top;
  margin-top: 2.5px;
  max-width: 70%;
}
.media-image {
  border-radius: 12px;
  height: 50px;
  width: 50px;
  object-fit: cover;
  margin-left: 16px;
  float: right;
  background-color: transparent;
}
.media-controls {
  padding-top: 16px;
  width: 100%;
}
</style>

<script>
export default {
  name: "Media",
  props: ["name", "description", "iconUri", "iconTitle", "uri"]
};
</script>