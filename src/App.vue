<script>
  import HeaderApp from './components/HeaderApp.vue';
  import MainApp from './components/MainApp.vue';
  import SocialApp from './components/SocialApp.vue';

  export default{
    components: {
      HeaderApp,
      MainApp,
      SocialApp,
    }
  }
</script>

<template>
 <HeaderApp/>

 <main>
  <MainApp/>
 </main>

 <footer>
  <SocialApp/>
 </footer>
</template>

<style lang="scss">
@use './styles/general.scss' as *;
</style>
