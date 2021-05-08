<template>
  <div>
    <input type="text" name="Rody" value="" />
    <card title="Title" v-for="item in 4"></card>
  </div>
</template>

<script>
import Card from "../components/Card.vue";
export default {
  components: { Card }
};
</script>
