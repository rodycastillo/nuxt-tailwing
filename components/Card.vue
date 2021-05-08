<template>
  <div class="container h-full p-1">
    <div
      class="p-5 border-l-4 border-blue-500 bg-blue-100 text-blue-500 text-sm font-bold"
    >
      {{ title }}
    </div>
  </div>
</template>
<script>
export default {
  name: "Card",
  props: {
    title: {
      type: String,
      default: ""
    }
  }
};
</script>
<style lang="scss" scoped></style>
