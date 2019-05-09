<template>
  <!-- MAIN CONTAINER -->
  <div id="app">
    <Sidenav></Sidenav>
    <!-- CONTAINER POSITIONING ALL COMPONENTS NEXT TO SIDENAV -->
    <div class="grid-container">
      <Topnav></Topnav>
      <RiskCards></RiskCards>
      <LandingGraph></LandingGraph>
      <FooterPlain></FooterPlain>
    </div>
  </div>
</template>

<script>
import VueCircle from "vue2-circle-progress";
import Sidenav from "./components/Sidenav";
import Topnav from "./components/Topnav";
import RiskCards from "./components/RiskCards";
import LandingGraph from "./components/LandingGraph";
import FooterPlain from "./components/FooterPlain";

export default {
  name: "App",
  components: {
    VueCircle,
    Sidenav,
    Topnav,
    RiskCards,
    LandingGraph,
    FooterPlain
  }
};
</script>

<style>
.carousel-control-next-icon,
.carousel-control-prev-icon {
  background-color: rgb(78, 78, 78);
  margin-top: 1.5em;
}

.grid-container {
  background: #16222a; /* fallback for old browsers */
  background: -webkit-linear-gradient(to bottom, #3a6073, #16222a);
  background: linear-gradient(to bottom, #3a6073, #16222a);
  width: 85%;
  /* height: 125vh; */
  float: right;
}

@media (min-width: 1200px) {
  .navbar,
  .page-footer,
  main {
    padding-left: 270px;
  }
}

@media (max-width: 1199.98px) {
  .grid-container {
    width: 100vw;
  }
}
</style>
