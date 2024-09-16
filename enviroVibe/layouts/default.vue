<script setup lang="ts">

</script>

<template>
  <div class="layout-container">
    <div class="sidebar">
      <Sidebar />
    </div>
    <div class="page-content">
      <slot />
    </div>
  </div>
</template>

<style scoped lang="scss">
.layout-container {
  display: flex;
  gap: 1rem;
}

.sidebar {
  position: fixed;
  top: 0;
}

.page-content {
  width: 100%;
  min-height: 100dvh;
}
</style>