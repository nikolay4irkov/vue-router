<template>
  <router-link class="event-link" :to="{ name: 'event-show', params: { id: event.id } }">
    <div class="event-card">
      <span>@ {{ event.time }} on {{ event.date }}</span>
      <h4 class="title">{{ event.title }}</h4>
      <BaseIcon name="users">{{ event.attendees.length }} attending</BaseIcon>
    </div>
  </router-link>
</template>

<script>
export default {
  props: {
    event: Object
  }
};
</script>

<style lang="scss" scoped>
.event-card {
  width: 300px;
  margin: 0 auto;
  padding: 20px;
  margin-bottom: 24px;
  cursor: pointer;
  border: 1px solid gray;
  transition: all 0.2s;
  text-align: left;

  &:hover {
    transform: scale(1.01);
    box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2),
      0 1px 15px 0 rgba(0, 0, 0, 0.19);
  }
}

.event-card > .title {
  margin: 0;
  font-size: 24px;
  font-weight: bold;
}

.event-link {
  color: black;
}
</style>
