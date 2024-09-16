<script setup lang="ts">
</script>

<template>
  <div class="sidebar-container">
    <div class="menu-items">
      <ul>
          <li><NuxtLink to="/">Home</NuxtLink></li>
          <li><NuxtLink to="events">Events</NuxtLink></li>
          <li><NuxtLink to="/me">Me</NuxtLink></li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.sidebar-container {
  background: blanchedalmond;
  height: 100dvh;
  border-right: 1px solid #2d642d;
}

a {
  color: black;
  text-decoration: none;
}

ul {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  padding: 3rem 1rem 1rem;
}

li {
  width: 100%;
  cursor: pointer;
}

li:hover {
  background-color: linen;
  border: 1px solid #2d642d;
}
</style>