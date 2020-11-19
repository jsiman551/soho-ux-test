<template>
  <div id="app">
    <MainContainer />
  </div>
</template>

<script>
import MainContainer from './components/MainContainer.vue'
import "./styles/main.scss"

export default {
  name: 'app',
  components: {
    MainContainer
  }
}
</script>
