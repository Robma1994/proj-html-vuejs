<template>
  <div>
    <header class="containerHeader">
      <div class="logo verOriCentering">
        <div class="containerImg">
         <img src="../assets/gym_logo_2x.png" alt=""> 
        </div>
      </div>
      <div class="link verOriCentering">
        <ul class="ul" v-for="(link,index) in links" :key="index">
          <li >
            <a :class="(link.active == true) ? 'active' : null" href="#">{{link.text}}</a>
          </li>
        </ul>
      </div>
    </header>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      links: 
      [
        {
          text: 'HOME',
          url: '#',
          active: true
        },
        {
          text: 'ABOUT US',
          url: '#',
          active: false
        },
        {
          text: 'FACILITIES',
          url: '#',
          active: false
        },
        {
          text: 'MEMBERSHIP',
          url: '#',
          active: false
        },
        {
          text: 'TESTIMONIALS',
          url: '#',
          active: false
        },
        {
          text: 'BLOG',
          url: '#',
          active: false
        },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/variables';

.containerHeader {
  width: 100%;
  height: 240px;
  display: flex;

    .logo {
      width: 50%;
      height: 100%;
        
        .containerImg {
          width: 170px;
          height: 100px;

            img {
              width: 100%;
              height: 100%;
            }
        }
    }

    .link {
      width: 50%;
      height: 100%;

        .ul {
          padding-right: 15px;

            li {
              list-style-type: none;

                a {
                  text-decoration: none;
                  color: $colorWhite;
                  font-size: $fontSize13;

                }
                a.active {
                  color: red;
                }
            }
        }
    }
}
</style>
