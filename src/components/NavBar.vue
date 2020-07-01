<template>
  <div id="nav" class="nav">
    <router-link to="/">Real World Vue</router-link>
    |
    <nav>
      <router-link :to="{ name: 'event-list' }">List</router-link>
      |
      <router-link :to="{ name: 'event-create' }">EventCreate</router-link>
    </nav>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
