<template>

  <div class="orizzontal verOriCentering">
    <div class="wrapper">
      <div class="wrapper-item">
        <h1>{{contact.title}}</h1>
        <p>{{contact.street}}</p>
        <p>{{contact.city}}</p>
        <p>{{contact.phone}}</p>
        <p>{{contact.email}}</p>
      </div> 
    </div>
    <div class="wrapper">
      <div class="wrapper-item">
        <h1>{{question.title}}</h1>
        <div class="orizzontal">
          <i class="fas fa-chevron-right"></i>
          <p>{{question.question_one}}</p>
        </div>
        <div class="orizzontal">
          <i class="fas fa-chevron-right"></i>
          <p>{{question.question_two}}</p>
        </div>
      </div>
    </div>
    <div class="wrapper">
      <div class="wrapper-item">
        <h1>{{open.title}}</h1>
        <div>
          <p>Weekends {{open.monday}} - {{open.friday}}</p>
          <p>{{open.open}} - {{open.close1}}</p>
        </div>
        <div>
          <p>Weekends {{open.saturday}} - {{open.sunday}}</p>
          <p>{{open.open}} - {{open.close2}}</p>
        </div>
      </div>
    </div>
    <div class="wrapper">
      <img src="../assets/gym_ad-compressor.jpg" alt="">
    </div>
  </div>
</template>

<script>
import contacts from '../assets/dati/contacts.js'
import questions from '../assets/dati/questions.js'
import openingTimes from '../assets/dati/openingTimes.js'
export default {
  name: 'FooterTop',
  data() {
    return {
      contact: contacts,
      question: questions,
      open: openingTimes
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/variables';
.wrapper {
  width: calc(100% / 4);
  height: 100%;

    .wrapper-item {
      width: 80%;
        h1 {
          font-size: $fontSize16;
          color: gray;
          margin-bottom: 15px;
        }
        i, p {
            color: $colorDoveGray;
        }
        i {
            font-size: $fontSize13;
            margin-right: 3px;
        }
    }
     
}

  
</style>
