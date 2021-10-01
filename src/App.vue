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
    <div class="container height300 backgroundLightGray">
      <div class="container-small height100 verOriCentering">
        <div class="verOriCentering dirCol">
          <h2 class="marginB10">World Class Fitness</h2>
          <img class="marginB10" src="./assets/divider-x-red.png" alt="">
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
            <img src="./assets/home_img-compressor.jpg" alt="">
          </div>
          <div class="height200 width300 marginL10">
            <h3 class="marginB10 font-s18 colorWhite">Sign Up For A Free Training Sessione!</h3>
            <form class="orizzontal dirCol">
              <label for="name">Name</label>
              <input type="text" name="name" placeholder="Scrivi il tuo nome">
              <label for="e-mail">E-mail</label>
              <input type="text" email="e-mail" placeholder="Scrivi la tua e-mail">
              <input type="submit" value="START NOW">
            </form>
          </div>
        </div>
      </div>
    </div>
<!-- Fine Blocco Tre - Form -->  
<!-- Activities -->
    <div class="backActivities height350">
      <div class="container-small height100">
        <div class="wrapper-Activities" v-for="(activ,index) in activity" :key="index"> 
          <div class="cycleIcon verOriCentering marginB10">
            <i class="largeIcon" :class="`fas ${activ.icon}`"></i>
          </div>
          <h3 class="marginB10">{{activ.title}}</h3>
          <img class="marginB10" src="./assets/divider-x-red.png" alt="">
          <p class="marginB10">{{activ.text}}</p>
        </div>
      </div>
    </div>
<!-- Fine Activities -->
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
import activities from './assets/dati/activities.js'
export default {
  name: 'App',
  components: {
    Header,
    FooterTop,
    FooterBottom
  },
  data() {
    return {
      activity: activities
    }
  }
}
</script>

<style lang="scss">
@import './style/generals';
@import './style/variables';
//SEZIONE HEADER
.background {
  background-image: url('assets/home-banner.jpg');
  background-size: cover;
}
.container {
  width: 100%;
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

.container {
  .container-small{
    .dirCol {
        h2 {
          color: $colorWhite;
          font-size: $fontSize30;
        }
        p {
          color: $colorDoveGray;
        }
    }
  }
}
//SEZIONE WORLD
.container {
  background-color: $backgroundDarkGray;
  .container-small {
    .verOriCentering {
      .height200 {

          img {
            width: 100%;
          }
      }
    }
  }
}
//SEZIONE FORM
//FINE SEZIONE FORM

//SEZIONE ACTIVITIES
.backActivities {
  background-image: url('./assets/gym_bkgd_bw-compressor.jpg');
  background-position: center;
  .container-small {
    display: flex;
    .wrapper-Activities {
      //width: calc(100% / 4);
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
        .cycleIcon {
          width: 60px;
          height: 60px;
          border: 1px solid red;
          border-radius: 50%;

            .largeIcon{
              font-size: $fontSize30;
            }
        }
        p {
          text-align: center;
        }
    }
  }
}
//FINE SEZIONE ACTIVITIES

.backgroundShark {
    background-color: $backgroundShark;
}
.backgroundLightBlack {
  background-color: $colorLightBlack;
}
.backgroundLightGray {
  background-color: $backgroundGrayLight;
}

</style>
