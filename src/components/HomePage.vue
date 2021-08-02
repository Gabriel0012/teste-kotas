<template>
  <NavComponent></NavComponent>
  <section class="container">
    <FamilyComponent></FamilyComponent>
    <AdministradorComponent></AdministradorComponent>
    <AboutGroup></AboutGroup>
    <QuemComponent></QuemComponent>
    <DuvidasComponent></DuvidasComponent>
    <CarrouselComponent></CarrouselComponent>
  </section>

  <section class="fixed-content">
    <CobrancaComponent></CobrancaComponent>
  </section>
</template>

<script>
import NavComponent from "./NavComponent.vue";
import FamilyComponent from "./FamilyComponent.vue";
import CobrancaComponent from "./CobrancaComponent.vue";
import AdministradorComponent from "./AdministradorComponent.vue";
import AboutGroup from "./AboutGroup.vue";
import QuemComponent from "./QuemComponent.vue";
import DuvidasComponent from "./DuvidasComponent.vue";
import CarrouselComponent from "./CarrouselComponent.vue";

export default {
  name: "HomePage",
  props: {
    msg: String,
  },
  components: {
    NavComponent,
    FamilyComponent,
    CobrancaComponent,
    AdministradorComponent,
    AboutGroup,
    QuemComponent,
    DuvidasComponent,
    CarrouselComponent,
  },
};
</script>

<style scoped>
.container {
  width: 540px;
  margin-left: 284px;
  margin-top: 20px;
}

@media screen and (min-width: 1100px) {
  .fixed-content {
    width: 319px;
    position: fixed;
    top: 55px;
    right: 23%;
  }

  .fixed-content .card {
    border-radius: 0 !important;
  }
}

@media screen and (max-width: 480px) {
  .container {
    margin-left: 0;
    width: 100%;
    margin-bottom: 84px;
  }

  .fixed-content {
    height: 84px;
    width: 100%;
    position: fixed;
    bottom: 0;
  }
}
</style>
