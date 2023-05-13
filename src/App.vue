<template>
  <header class="header">
    <HeaderNav></HeaderNav>
  </header>
  <main class="main">
    <MainHero></MainHero>
    <MainNew></MainNew>
    <MainPopular></MainPopular>
  </main>
  <Attribution></Attribution>
</template>

<script>
import MainHero from './components/MainHero';
import HeaderNav from './components/HeaderNav';
import MainNew from './components/MainNew';
import MainPopular from './components/MainPopular';
import Attribution from './components/Attribution'


export default {  
  name: 'App',
  components: {
    HeaderNav,
    MainHero,
    MainNew,
    MainPopular,
    Attribution
}
}

</script>

<style>

</style>
