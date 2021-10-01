<template>
  <div id="app">
    <div class="background container height728">
      <Header />
      <div class="container-small heightBanner orizzontalCentering">
        <div class="container-Title">
          <h1 class="title">NO PAIN NO GAIN</h1>
          <p>Motivation is what gets you started. Habit is what keeps you going </p>
          <button>Join us today</button>
        </div>
      </div>
    </div>
<!-- Blocco due - World Class Fitness -->
    <div class="container height300">
      <div class="container-small height100 verOriCentering">
        <div class="verOriCentering dirCol">
          <h2>World Class Fitness</h2>
          <h3>Ciao pippo</h3>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi odit in itaque reprehenderit. Voluptatibus animi deus sed?</p>
        </div>
      </div>
    </div>
<!-- Fine Blocco due - World Class Fitness -->
<!-- Blocco Tre - Form -->    
    <div class="container height350">
      <div class="container-small height100">
        <!-- Inserendo contenuto posso eliminare le altezze fisse e rendere il tutto dinamico -->
        
        <div class="verOriCentering height350"> <!-- Utilizzando flex con un div mancante, avrei perso elasticità-->
          <div class="height200 width300 marginR10">
            <!-- immagine -->
          </div>
          <div class="height200 width300 marginL10">
            <!-- Form -->
          </div>
        </div>
      </div>
    </div>
<!-- Fine Blocco Tre - Form -->  
    <div class="container backgroundShark">
      <div class="container-small wrapper">
        <FooterTop />
      </div>
    </div>  
    <div class="container height110 backgroundLightBlack">
      <div class="container-small height100">
        <FooterBottom />
      </div>
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import FooterTop from './components/FooterTop.vue'
import FooterBottom from './components/FooterBottom.vue'

export default {
  name: 'App',
  components: {
    Header,
    FooterTop,
    FooterBottom
  }
}
</script>

<style lang="scss">
@import './style/generals';
@import './style/variables';

.background {
  background-image: url('assets/home-banner.jpg');
  background-size: cover;
}
.container {
  width: 100%;
}
.container-small {
  //background-color: rgba($color: blue, $alpha: 0.3);
  //border: 1px solid black;
}
.title {
  font-size: $fontSize65;
  color: $colorWhite;
}

.container-Title {
  margin-top: 75px;
  color: $colorWhite;
  text-align: center;

    p {
      font-size: 16px;
      color: lightgray;
      padding: 15px 15px
    }
    button {
      border: 1px solid gray; 
      padding: 5px 5px 5px 5px;
      background-color: inherit;
      color: gray;
    }
}
.backgroundShark {
    background-color: $backgroundShark;
}
.backgroundLightBlack {
  background-color: $colorLightBlack;
}
</style>
