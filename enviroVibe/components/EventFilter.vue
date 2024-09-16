<script setup lang="ts">
</script>

<template>
  <div class="filter-container">
    <div class="labeled">
      <label for="global">Search</label>
      <input type="text" id="global">
    </div>
    <div class="filters">
      <div class="labeled">
        <label for="country">Country</label>
        <select name="country" id="country">
          <option value="so">so</option>
          <option value="many">many</option>
          <option value="options">options</option>
        </select>
      </div>
      <div class="labeled">
        <label for="city">City</label>
        <select name="city" id="city">
          <option value="so">so</option>
          <option value="many">many</option>
          <option value="options">options</option>
        </select>
      </div>
      <div class="labeled">
        <label for="date">Date</label>
        <input type="date" id="date">
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.filter-container {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  margin: 1rem 0;

  .filters {
    display: flex;
    align-items: center;
    gap: 1rem;
  }

  .labeled {
    display: flex;
    flex-direction: column;
  }
}
</style>