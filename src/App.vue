<template>
  <div id="app">
    <Header />
    <!-- OPTION A -->
    <!-- top header: nav + logo -->
    <!-- bottom header: 2 col txt left img right + icon price in absolut left  -->
    <!-- OPTION B  -->
    <!-- bottom header = jumbotron with same background image -->
    <Jumbotron />
    <!-- Awarding  Pro Barbers  -->
    <Main />
    <!-- services
    static obj
    and
    products
    a single component? try it
    + product months featured absolut?  -->
    <!-- reviews  and Posts -->
    <Footer />
    <!-- footer top -->
    <!-- footer bottom : copyright -->
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Jumbotron from "./components/Jumbotron.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";
//Font
import "@fontsource/abril-fatface"; // Defaults to weight 400.
import "@fontsource/lato"; // Defaults to weight 400.

export default {
  name: "App",
  components: {
    Header,
    Jumbotron,
    Main,
    Footer,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
@import "~@fortawesome/fontawesome-free/css/all.min.css";

#app {
  font-family: "Lato", Helvetica, Arial, sans-serif;
}
</style>
