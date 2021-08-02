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
      <div>
        {{ vagas.usadas }} / {{ vagas.disponiveis }}
        <p>Vagas disponíveis</p>
      </div>

      <div>
        {{ pormes }}
        <p>Por mês</p>
      </div>

      <div>
        <i class="fas fa-link"></i>
        <p>Acesso por convite</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FamilyComponent",
  props: {},
  data: () => {
    return {
      vagas: {
        usadas: 2,
        disponiveis: 5,
      },
      pormes: 'R$ 7,90'
    };
  },
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

.cols {
  margin-top: 30px;
  margin-bottom: 20px;
}

.cols div {
  text-align: center;
  padding: 5px 38px;
  border-right: 1px solid #e1e1e1;
  color: #141728;
  font-size: 24px;
  font-weight: bold;
  height: 50px;
}

.cols div:last-child {
  border: 0;
}

.cols div p {
  font-size: 12px;
  color: #616161;
  font-weight: 300;
}
</style>
