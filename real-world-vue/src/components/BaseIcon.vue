<template>
  <div>Icon</div>
</template>

<script>
import feather from "feather-icons";

export default {
  props: {
    name: String,
    width: {
      type: [Number, String],
      default: 24,
    },
    height: {
      type: [Number, String],
      default: 24,
    },
  },
};
</script>


<style scoped>
</style>
