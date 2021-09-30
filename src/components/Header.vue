<template>
  <div>
    <header class="containerHeader">
      <div class="logo">
        <!-- LOGO -->
        <h1>pippo</h1>
      </div>
      <div class="link">
        <h1>poppo</h1>
        <!-- <li> -->
      </div>
    </header>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/variables';

.containerHeader {
  width: 100%;
  height: 190px;
  display: flex;

    .logo {
      width: 50%;
      height: 100%;
      background-color: azure;
        
    }
    .link {
      width: 50%;
      height: 100%;
      background-color: lightgreen;
    }
}
</style>
