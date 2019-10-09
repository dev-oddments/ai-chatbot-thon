<template></template>

<style lang="scss" scoped>
.app-head {
  z-index: 666;
  padding: 16px;
  position: fixed;
  width: 100%;
  background-color: white;

  .app-icon {
    border-radius: 8px;
    width: 30px;
    height: 30px;
    object-fit: cover;
    background-color: transparent;
  }

  .app-info {
    display: inline-block;
    margin-left: 10px;

    .app-name {
      font-size: 18px;
      font-weight: 500;
      color: #202124;
    }
  }
  .app-poweredby {
    color: #5f6368;
    font-size: 14px;

    a[href] {
      color: #202124;
      text-decoration: none;
    }
  }
}
</style>

<script>
export default {
  name: "TopHead",
  props: ["app"]
};
</script>