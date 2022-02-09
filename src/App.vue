<template>
  <div id="app">
   <hero-cards>
   </hero-cards>
   <villain-cards></villain-cards>
  </div>
</template>

<script>
import HeroCards from './components/HeroCards.vue'
import VillainCards from './components/VillainCards.vue'

export default {
  name: 'App',
  components: {
    HeroCards,
    VillainCards
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.song_grid {
  display: grid;
  position: absolute;
  left: 20%;
}
.play_grid {
  display: grid;
  position: absolute;
  right: 20%;
}
</style>
