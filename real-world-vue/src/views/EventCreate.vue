<template>
  <div>
    <h1>Create Event, {{ user.name }}</h1>
    <p>This event was created by {{ user.id }}</p>
    <p>There are {{ catLength }}</p>
    <ul>
      <li v-for="cat in categories" :key="cat">{{ cat }}</li>
    </ul>
  </div>
</template>


<script>
import { mapState, mapGetters } from "vuex";
export default {
  computed: {
    catLength() {
      return this.$store.getters.catLength;
    },
    ...mapGetters(["getEventByID"]),
    ...mapState(["user", "categories"]),
  },
};
</script>

<style scoped>
</style>
