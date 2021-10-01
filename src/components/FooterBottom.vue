<template>
  <div>
    <div class="left height110 verticalCentering">
      <div class="orizzontal">
        <i class="far fa-copyright marginR5"></i>
        <p>{{pro.copyright}}</p>
      </div>
      <p>{{pro.theme}}</p>
      <p>{{pro.right}}</p>
      <p>{{pro.createWith}}</p>
    </div>
    <div class="right">
      <ul class="verticalCentering height110 ">
        <li v-for="(element,index) in socials" :key="index">
          <a>
           <i :class="`fab ${element.icon}`"></i>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import proprieta from '../assets/dati/proprieta.js'
import social from '../assets/dati/social.js'
export default {
  name: 'FooterBottom',
  data() {
    return {
      pro: proprieta,
      socials: social
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/variables';
.left {
  float: left;
    i {
      color: $colorDoveGray;
    }
    p {
      color: $colorDoveGray;
      font-size: $fontSize13;

        &::after {
          content: ' |';
          margin: 10px;
      }
    }
    
    
}
.right{
float: right;
    
    li {
      list-style-type: none;

        i {
          margin-right: 10px;
          font-size: 40px;
          color: $colorOrange;
        }
    }
}
 
</style>
