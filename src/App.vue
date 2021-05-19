<template>
  <v-app>
    <Header :isMobile="isMobile" />
    <v-main>
      <Content :isMobile="isMobile"/>
      <Footer />
    </v-main>
  </v-app>
</template>

<script>
import Content from './components/Content';
import Footer from './components/Footer';
import Header from './components/Header';

export default {
  name: 'App',
  components: { Content, Footer, Header },
  data: () => ({
    //
  }),
  computed: {
    isMobile () {
      return this.$vuetify.breakpoint.xsOnly
    }
  }
};
</script>

<style>
  #app{
    background: linear-gradient(180deg, #148EFF 0%, #001439 48.44%, #000000 77.08%);
    background-repeat: no-repeat;
    height: 100%;
    font-family: Quicksand, sans-serif;
  }
</style>
