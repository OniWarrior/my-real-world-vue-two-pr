<template>
  <div>
    <span>@{{ event.time }} on {{ event.date }}</span>
    <h4>{{ event.title }}</h4>
    <span>{{ event.attendees.length }} attending</span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      event: {
        id: 1,
        title: "Beach Cleanup",
        date: "Tue January 30,2023",
        time: "6:00",
        attendees: [
          { id: "abc123", name: "Stephen Ryan" },
          { id: "def321", name: "Dr. Manhattan" },
        ],
      },
    };
  },
};
</script>

<style scoped>
h4 {
  color: green;
}
</style>
