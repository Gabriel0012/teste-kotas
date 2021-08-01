<template>
  <div class="card">
    <img src="../assets/spotify.png" alt="spotify logo" />

    <h4>Spotify Family</h4>

    <p class="subtitle">
      Grupo destinado a pessoas que querem ver o melhor da Netflix em 4K a um
      preço acessível.
    </p>

    <span class="customizado">Customizado</span>

    <div class="cols">
      <div>{{ vagas.usadas }}/{{ bagas.disponiveis }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FamilyComponent",
  props: {},
};
</script>

<style scoped>
.subtitle {
  color: #616161;
  font-size: 12px;
}

.customizado {
  width: 105px;
  height: 22px;

  background: #f1f4f5;
  border-radius: 25px;

  font-size: 10px;
  line-height: 12px;
  color: #616161;
  padding: 5px 15px;
}
</style>