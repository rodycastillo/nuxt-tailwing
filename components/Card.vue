<template>
  <div
    :class="state ? 'bg-blue-100' : 'bg-green-100'"
    class="container h-full p-1 flex justify-between"
  >
    <div class="p-5 border-l-4 border-blue-500 text-gray-800 text-sm font-bold">
      {{ title }}
    </div>
    <div class="actions h-full flex items-center">
      <button
        @click="$emit('update')"
        class="bg-yellow-300 mt-1 mr-1 hover:bg-yellow-600 text-white p-3 rounded-lg"
      >
        E
      </button>
      <button
        @click="$emit('delete')"
        class="bg-red-300 mt-1 hover:bg-red-600 text-white p-3 rounded-lg"
      >
        D
      </button>
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
    },
    state: {
      type: Boolean,
      default: false
    }
  }
};
</script>
<style lang="scss" scoped></style>
