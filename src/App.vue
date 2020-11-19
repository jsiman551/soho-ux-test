<template>
  <div id="app">
    <HomePage />
  </div>
</template>

<script>
import HomePage from './components/HomePage.vue'
import "./styles/main.scss"

export default {
  name: 'app',
  components: {
    HomePage
  }
}
</script>
