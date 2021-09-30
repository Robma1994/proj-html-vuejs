<template>
  <div id="app">
    <div class="container">
      <Header />
      <div class="container-small">
        <h1>pippo</h1>
      </div>
    </div>

  </div>
</template>

<script>
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Header
  }
}
</script>

<style lang="scss">
@import './style/generals';
.container {
  width: 100%;
  background-image: url('assets/home-banner.jpg');
  background-repeat: no-repeat;
  background-size: contain;
  height: 1000px;
}

</style>
