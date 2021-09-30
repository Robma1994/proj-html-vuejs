<template>
  <div id="app">
    <div class="container height728">
      <Header />
      <div class="container-small heightBanner">
        <h1>NO PAIN NO GAIN</h1>
        <p>laaaaa</p>
        <button>Join us today</button>
      </div>
    </div>
<!-- Blocco due - World Class Fitness -->
    <div class="container height300">
      <div class="container-small height300 verOriCentering">
        <div class="verOriCentering dirCol">
          <h2>World Class Fitness</h2>
          <h3>Ciao pippo</h3>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi odit in itaque reprehenderit. Voluptatibus animi deus sed?</p>
        </div>
      </div>
    </div>
<!-- Fine Blocco due - World Class Fitness -->
<!-- Blocco Tre - -->    
    <div>

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
  //background-image: url('assets/home-banner.jpg');
  //background-size: cover;
.container {
  width: 100%;
  background-color: orange;
  border: 1px solid black;
}
.container-small {
  background-color: blue;
  border: 1px solid black;
}



</style>
