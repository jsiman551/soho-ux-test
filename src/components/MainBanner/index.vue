<template>
  <div class="main-banner-container">
      <Menu />
      <div class="title-text">
          <p>Nos especializamos en</p>
          <p class="green-text">interfaces digitales que los usuarios aman</p>
          <button>hablemos de tu proyecto</button>
      </div>
  </div>
</template>

<script>
import Menu from '../Menu/index';

export default {
    name: 'MainBanner',
    components: {
        Menu
    }
}
</script>
