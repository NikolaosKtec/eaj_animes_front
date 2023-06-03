<template>
  <div id="app">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200" />
    <HeadCommon/>
    <CardAnimes/>
   
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
import CardAnimes from './components/cardAnime/CardAnimes.vue';
import HeadCommon from './components/HeadCommon.vue'
// import TesteComp from './components/TesteComp.vue';
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    // TesteComp,
    HeadCommon,
    CardAnimes,
  },
  htmlAttrs: {
    lang: 'en'
  }
}
</script>


