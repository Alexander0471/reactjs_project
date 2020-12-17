<template>
  <div id="app">
    <HeaderComponent></HeaderComponent>
    <Slider></Slider>
    <div class="center">

      <!--LastArticles></LastArticles>-->
      <router-view></router-view>

      <Sidebar></Sidebar>
      <div class="clearfix"></div>
    </div>
    <FooterComponent></FooterComponent>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent';
import Slider from './components/Slider';
import Sidebar from './components/Sidebar';
import FooterComponent from './components/FooterComponent';

export default {
  name: 'App',
  components: {
    HeaderComponent,
    Slider,
    Sidebar,
    FooterComponent
  }
}
</script>

<style>

@import './assets/css/styles.css';
</style>
