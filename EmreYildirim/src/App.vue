<template>
  <HeroMessage />
</template>

<script>
import HeroMessage from './components/HeroMessage.vue'

export default {
  name: 'App',
  components: {
    HeroMessage,
  }
}
</script>

<style>

body{
  width: 100%;
  margin: 0;
  padding: 0;
}
#app {
  display: flex;
  justify-content: space-between;
  flex-wrap: nowrap;
  flex-direction: column;
  align-items: center;

  height: 100vh;
  margin: 0;
  padding: 0;
  padding-left: 6%;
  padding-right: 6%;
  background-image: url(./assets/images/background.png);  
  background-size: cover; /* Resmi kapsayıcı elemana sığacak şekilde ölçeklendirir ve taşan kısımları keser */
  background-position: center; /* Resmi ortalar */
  background-repeat: no-repeat; /* Resmin tekrar etmesini engeller */
}


</style>
