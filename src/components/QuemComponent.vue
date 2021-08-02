<template>
  <div class="card">
    <section class="header">
      <span>Quem já faz parte</span>
    </section>

    <section class="body">
      <div class="imgs">
        <div class="text-center" v-for="p in participantes" :key="p.nome">
          <img
            :src="p.foto"
            alt="foto"
          />
          <p>{{ p.nome }}</p>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "QuemComponent",
  props: {},
  data: () => {
    return {
      participantes: [
        { nome: "Maria", foto: require('../assets/part1.png') },
        { nome: "Filipe", foto: require('../assets/part3.png') },
        { nome: "Ana", foto: require('../assets/part2.png') },
      ]
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card {
  padding: 0;
}

.imgs {
  display: grid;
  grid-area: repeat(3, 33.33%);
  grid-template-columns: 33.33% 33.33% 33.33%;
}

.imgs div img {
  width: 58px;
}

.imgs div p {
  font-size: 12px;
}

.card .header {
  border-bottom: 1px solid #f1f4f5;
  padding: 16px;
}

.card .header span {
  font-weight: 700;
  font-size: 14px;
}

.card .body {
  margin-top: 10px;
  padding: 20px;
}
</style>
