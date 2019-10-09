<template>
  <a class="list-item" :href="uri" target="_blank" rel="noopener noreferrer">
    <div class="list-item-content">
      <div class="list-item-title">{{title}}</div>
      <span class="list-item-description">{{description}}</span>
      <span class="list-item-footer" v-if="footer">{{footer}}</span>
    </div>
    <div
      class="list-item-image"
      v-if="imageUri"
      :style="{backgroundImage: `url(${imageUri})`}"
      :alt="imageTitle"
    />
  </a>
</template>

<script>
export default {
  name: "ListItem",
  props: ["imageUri", "imageTitle", "title", "description", "footer", "uri"]
};
</script>