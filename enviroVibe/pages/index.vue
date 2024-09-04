<script setup lang="ts">
const timesClicked= ref(0)

const clickButton = () => {
  timesClicked.value++
}
</script>

<template>
  <div>
    THIS iS THE BASE SITE
    <button @click="clickButton">Click me {{timesClicked}}</button>
  </div>
</template>