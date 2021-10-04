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
        <div class="container-small-fitness-top verOriCentering dirCol">
          <h2 class="marginB10">World Class Fitness</h2>
          <img class="marginB10" src="./assets/divider-xx-red.png" alt="">
          <p class="textC">At Avada Gym, everything we do from top to bottom is of the highest quality to ensure we're equipped to help you reach your goals of a healthy and fit lifestyle</p>
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
    <div class="backActivities">
      <div class="container-small">
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
<!-- Sezione real world results-->
    <div class="container-real-world backgroundLightGray">
      <div class="container-small-real-world">
        <div class="container-small-top verOriCentering dirCol">
          <h2 class="marginB10">REAL WORLD RESULTS</h2>
          <img class="marginB10" src="./assets/divider-xx-red.png" alt="">
        </div>
        <div class="wrapper-testimonials">
          <div class="wrapper-card-testimonial" v-for="(testim, index) in testimonial" :key="index">
            <div class="wrapper-img paddingTop20 paddingBottom20 paddingLeft20 paddingRight20">
              <img class="height110" :src="require(`./assets/compressor-${testim.img}`)" alt="">
            </div>
            <div class="wrapper-name paddingBottom20 paddingTop20">
              <p>{{testim.descrition}}</p>
              <h4>{{testim.name}}</h4>
            </div>
          </div>
        </div>
      </div>
    </div>
<!-- FINE-->
<!-- Sezione Performance-->
    <div class="container-performance backgroundLightGray">
      <div class="container-small-performance">
        <div class="container-small-top verOriCentering dirCol">
          <h2 class="marginB10">HIGH PERFORMANCE FACILITIES</h2>
          <img class="marginB10" src="./assets/divider-xx-red.png" alt="">
        </div>
        <div class="wrapper-img-performance">
          <div class="wrapper-card" v-for="(img, index) in performance" :key="index">
            <img :src="require(`./assets/home-${img.immagine}.jpg`)" alt="">
          </div>
        </div>
      </div>
    </div>
<!-- FINE-->
<!-- Sezione Citazione-->
    <div class="container-citation">
      <div class="container-small-citation">
        <div>
         <p>"I fear not the man who was has practiced 10,000 kicks once, but I fear the man who has practiced one kick 10,000 times"</p>
        </div>
        <div>
          <h3>BRUCE LEE - QUOTE OF THE DAY</h3>
        </div>
      </div>
    </div>
<!-- FINE-->
<!-- Sezione trainers -->
    <div class="container-trainers">
      <div class="container-small-trainers">
        <div class="container-s-trainers-top verOriCentering dirCol">
          <h2 class="marginB10">MEET OUR TRAINERS</h2>
          <img class="marginB10" src="./assets/divider-xx-red.png" alt="">
        </div>
        <div class="container-s-trainers-bottom">
          <div class="wrapper-card-trainer">
            <div class="card-trainer backgroundShark" v-for="(train, index) in trainers" :key="index">
              <img :src="require(`./assets/trainer-${train.img}.jpg`)" alt="">
              <div class="card-trainer-bottom">
                <div class="card-trainer-title">
                  <h3>{{train.title}}</h3>
                  <h4>{{train.subTitle}}</h4>
                </div>
                <div class="card-trainer-des">
                  <p>{{train.description}}</p>
                </div>
                <div class="card-trainer-social">
                  <i :class="`fab ${train.facebook}`"></i>
                  <i :class="`fab ${train.twitter}`"></i>
                  <i :class="`fab ${train.instagram}`"></i>
                </div>
              </div>
            </div>
          </div>
          <div class="btn-trainers">
            <button>VIEW ALL TRAINERS</button>
          </div>
        </div>
      </div>
    </div>
<!-- FINE -->
<!-- Sezione News -->
    <div class="container-news">
      <div class="container-small-news">
        <div class="container-s-news-top">
          <h2 class="marginB10">PERFORMANCE NEWS</h2>
          <img class="marginB10" src="./assets/divider-xx-red.png" alt="">
        </div>
        <div class="container-s-news-bottom">
          <div class="wrapper-card-news">
            <div class="card-news" v-for="(element,index) in notizie" :key="index">
              <div class="cont-s-n-bot-top">
                <img :src="require(`./assets/${element.img}`)" alt="">
              </div>
              <div class="cont-s-n-bot-bot">
                <h3>{{element.title}}</h3>
                <p>{{element.description}}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
<!-- FINE -->
<!-- Sezione Goal -->
    <div class="container-goal">
      <div class="container-small-goal">

      </div>
    </div>
<!-- FINE -->
<!-- FOOTER -->
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
import testimonials from './assets/dati/testimonials.js'
import {immaginiPerfomance} from './assets/dati/performance.js'
import {dataTrainers} from './assets/dati/trainers.js'
import {news} from './assets/dati/news.js'

export default {
  name: 'App',
  components: {
    Header,
    FooterTop,
    FooterBottom
  },
  data() {
    return {
      activity: activities,
      testimonial: testimonials,
      performance: immaginiPerfomance,
      trainers: dataTrainers,
      notizie: news
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
//FINE

//SEZIONE FORM

//FINE SEZIONE FORM

//SEZIONE ACTIVITIES
.backActivities {
  background-image: url('./assets/gym_bkgd_bw-compressor.jpg');
  background-position: center;
  padding: 100px 0 100px 0;
  .container-small {
    display: flex;
    width: 60%;
    .wrapper-Activities {
      //width: calc(100% / 4);
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
        .cycleIcon {
          width: 60px;
          height: 60px;
          border: 1px solid $colorOrange;
          border-radius: 50%;
          color: $colorOrange;
            .largeIcon{
              font-size: $fontSize30;
            }
        }
        h3 {
          color: $colorWhite;
        }
        p {
          text-align: center;
          color: $colorDoveGray;
        }
    }
  }
}
//FINE SEZIONE ACTIVITIES
//SEZIONE REAL WORLD RESULTS
.container-real-world {
  width: 100%;
  padding: 100px 0 50px 0;
  //height: 550px;

    .container-small-real-world {
      //height: 100%;
      width: 60%;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      justify-content: center;

        .container-small-top {
          h2 {
            color: $colorWhite;
          }
        }
        .wrapper-testimonials{
          display: flex;
          justify-content: center;
          flex-wrap: wrap;
            .wrapper-card-testimonial {
              display: flex;
              background-color: $backgroundDarkGray;
              width: 420px;
              margin: 10px;

                .wrapper-name{
                   
                   p{
                     color: $colorDoveGray;
                     font-style: oblique;
                     line-height: 25px;
                   }
                   h4 {
                     padding-top: 3px;
                     color: $colorWhite
                   }
                }
          }
        }
        
    }
}
//FINE
//SEZIONE HIGH PERFORMANCE
.container-performance {
width: 100%;
padding: 100px 120px 100px 120px;
//height: 550px;
    .container-small-performance{
      //height: 100%;
      width: 80%;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      justify-content: center;

        .container-small-top {

            h2 {
              color: $colorWhite;
            }
        }
    }
    .wrapper-img-performance {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-wrap: wrap;
      
       .wrapper-card{
         //width: calc(100% / 3 - 20px);
         margin: 5px 20px 20px 20px;
         height: 155px;
         display: flex;
         justify-content: center;
       }
    }
}
//FINE
//SEZIONE CITATION
.container-citation {
  background-color: lightsalmon;
  height: 300px;
  width: 100%;
    .container-small-citation {
      width: 80%;
      height: 100%;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      justify-content: center;
        p {
          font-size: $fontSize20;
          color: $colorWhite;
          text-align: center;
          padding-bottom: 40px;
        }
        h3 {
          font-size: $fontSize16;
          color: $colorWhite;
          text-align: center;
        }
    }
}
//FINE
//CONTAINER TRAINERS
.container-trainers {
  background-color: $backgroundDarkGray;
  width: 100%;

    .container-small-trainers {
      width: 60%;
      margin: 0 auto;
      padding: 50px 50px;
        .container-s-trainers-top {
          h2 {
            color: $colorWhite;
          }
        } 
        .container-s-trainers-bottom {
          display: flex;
          flex-direction: column;
          align-items: center;
            .wrapper-card-trainer {
              display: flex;
                .card-trainer {
                height: 310px;
                margin: 5px 10px 5px 10px;
                  .card-trainer-bottom {
                    padding: 18px 0 18px 18px;
                      .card-trainer-title{
                        width: 175px;
                          h3, h4{
                            color: $colorWhite;
                            font-size: $fontSize13;
                            line-height: 16px;
                          }
                      }
                      .card-trainer-des {
                        width: 175px;
                          p{
                            padding: 10px 0 10px;
                            color: $colorDoveGray;
                            font-size: $fontSize13;
                            line-height: 16px;
                          } 
                      }
                      .card-trainer-social {
                        width: 175px;
                          i {
                            margin-right: 8px;
                            color: $colorWhite;
                          }
                      }
                  }
              }
            }
            .btn-trainers{
              padding-top: 50px; 
                button {
                  padding: 10px 10px 10px 10px;
                  background-color: inherit;
                  color: $colorDoveGray;
                }
            } 
        }
    }
}
//FINE
//CONTAINER NEWS 
.container-news {
  background-color: $backgroundShark;
  width: 100%;
  padding: 50px 50px;
    .container-small-news{
      width: 60%;
      margin: 0 auto;
      .container-s-news-top {
        display: flex;
        flex-direction: column;
        align-items: center;
      }
      .container-s-news-bottom {

          .wrapper-card-news {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;

              .card-news {
                background-color: $backgroundDarkGray;
                margin: 10px 10px 10px 10px;
                width: 200px;
                height: 100%;

                  .cont-s-n-bot-top {

                  }
                  .cont-s-n-bot-bot {
                    padding: 15px 15px 15px 15px;
                  }
              }
          }
      }
    }
}
//FINE
//CONTAINER GOAL
.container-goal {
  width: 100%;
  height: 200px;
  background-image: url('./assets/home-parallax.jpg');
  background-position: 20% 20%;
}
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
