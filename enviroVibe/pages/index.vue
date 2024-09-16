<script setup lang="ts">
const timesClicked= ref(0)

const clickButton = () => {
  timesClicked.value++
}
</script>

<template>
  <div class="home-container">
    <h1>EnviroVibe</h1>
    <p>Do you want to have an actual impact on the environment?</p>
    <p>Are you ready to join thousands of others, creating movement towards a better future?</p>
    <p>Feel the EnviroVibe by taking part in events all around the globe!</p>
    <NuxtLink to="/events">
      <button>Check out the events</button>
    </NuxtLink>
  </div>
</template>

<style scoped>
  .home-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 100%;
  }

  h1  {
    margin-top: 7rem;
    font-size: 4rem;
  }

  p {
    font-size: 1.5rem;
  }

  button {
    margin-top: 5rem;
    font-size: 2rem;
    background: blanchedalmond;
    border: 1px solid #2d642d;
    padding: 1rem 2rem;
    border-radius: 2rem;
  }

  button:hover {
    cursor: pointer;
    background: linen;
  }
</style>