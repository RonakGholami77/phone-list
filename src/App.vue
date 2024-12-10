<template>
  <div id="App">
    <ThemeCard />
  </div>
</template>

<script>
import ThemeCard from './components/ThemeCard.vue'

export default {
  name: 'App',
  components: {
    ThemeCard,
  },
}
</script>

<style scoped>
#App {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin-top: 50px;
}
</style>
