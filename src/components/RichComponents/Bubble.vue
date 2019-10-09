<template>
  <div
    class="bubble"
    :class="{'me': from == 'me', 'loading': loading}"
    v-html="loading ? `...` : text&&text.split(`\n`).join(`<br>`)"
  ></div>
</template>
<script>
export default {
  name: "Bubble",
  props: ["text", "from", "loading"]
};
</script>