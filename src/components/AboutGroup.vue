<template>
  <div class="card">
    <p>Sobre o grupo <i class="fas fa-plus text-right"></i> </p>
  </div>
</template>

<script>
export default {
  name: "AboutGroup",
  props: {
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.card {
  padding: 5px;
}

.fa-plus {
  transform: translateX(180px);
}

@media screen and (max-width: 480px) {
  .fa-plus {
     transform: translateX(90px);
  }
}
</style>
