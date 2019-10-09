<template>
  <img class="picture" :src="uri" :alt="title" />
</template>

<style lang="scss" scoped>
.picture {
  height: auto;
  max-width: 100%;
  border-radius: 12px;
  box-shadow: 0 2px 6px 2px rgba(60, 64, 67, 0.15);
  object-fit: cover;
  background-color: transparent;
}
</style>

<script>
export default {
  name: "Picture",
  props: ["uri", "title"]
};
</script>