<template>
  <div class="m-2">
    <div class="text-blue-500 text-sm font-bold">Website Project</div>
    <div class="text-gray-700 font-bold text-3xl">UX Fundamental Sharing</div>
    <div class="text-sm font-bold text-gray-400">{{ this.date }}</div>
  </div>
</template>

<script>
export default {
  name: "TitleApp",
  data() {
    return {
      date: null
    };
  },
  mounted() {
    const todayDate = new Date();
    const todayDay = todayDate.toDateString();
    const todayHour = todayDate.toLocaleTimeString();
    this.date = `${todayDay}, ${todayHour}`;
  }
};
</script>

<style lang="scss" scoped></style>
