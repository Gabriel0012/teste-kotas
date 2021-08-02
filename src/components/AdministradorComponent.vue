<template>
  <div class="card">
    <section class="header">
      <span>Administrador</span>
    </section>

    <section class="body">
      <img src="../assets/fotoAdmin.png" alt="Foto do administrador">

      <p class="name">{{ admin.nome }}</p>

      <div class="selos">
        <i class="fas fa-trophy"></i>
        <i class="fas fa-trophy"></i>
        <i class="fas fa-trophy"></i>
      </div>

      <p id="subtitle">selos disponíveis</p>
    </section>
  </div>
</template>

<script>
export default {
  name: "AdministradorComponent",
  props: {
  },
  data: () => {
    return {
      admin: {
        foto: '../assets/fotoAdmin.png',
        nome: 'João das Couves'
      }
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.card {
  padding: 0;
}

.name {
  color: #141728;
  font-weight: 600;
  font-size: 14px;
  margin-bottom: 36px;
}

.fa-trophy {
  color: #262F56;
  font-size: 25px;
  padding: 5px 10px;
}

#subtitle {
  margin-top: 10px;
  margin-bottom: 10px;
  color: #616161;
  font-size: 12px;
}

.card .header {
  border-bottom: 1px solid #F1F4F5;
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
