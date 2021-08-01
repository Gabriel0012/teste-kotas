<template>
  <NavComponent></NavComponent>
  <section class="container">
    <FamilyComponent></FamilyComponent>
    <AdministradorComponent></AdministradorComponent>
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
  },
};
</script>

<style scoped>
.container {
  width: 540px;
  margin-left: 284px;
  margin-top: 20px;
}

.fixed-content {
  width: 319px;
  position: fixed;
  top: 55px;
  right: 24%;
}
</style>
