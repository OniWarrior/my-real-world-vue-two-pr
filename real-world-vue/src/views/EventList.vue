<template>
  <div>
    <h1>Events Listing</h1>
    <EventCard></EventCard>
    <BaseIcon />
  </div>
</template>

<script>
import EventCard from "../components/EventCard.vue";
import axios from "axios";

export default {
  components: {
    EventCard,
  },
  created() {
    axios.get(" http://localhost:3000/events").then((respons) => {
      console.log(respons.data);
    });
  },
};
</script>
