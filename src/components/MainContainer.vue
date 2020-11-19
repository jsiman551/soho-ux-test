<template>
  <div>
    <MainBanner />
    <NewsBar />
  </div>
</template>

<script>
import MainBanner from './MainBanner/index';
import NewsBar from './NewsBar/index';

export default {
  name: 'MainContainer',
  components: {
    MainBanner,
    NewsBar
  }
}
</script>
