<template>
  <h1>Showing event {{ event.title }}</h1>
</template>

<script>
import EventService from "../services/EventService";

export default {
  props: ["id"],
  data() {
    return {
      events: {},
    };
  },
  created() {
    EventService.getEvent(this.id)
      .then((response) => {
        this.event = response.data;
      })
      .catch((error) => {
        console.log("there was an error " + error.response);
      });
  },
};
</script>
