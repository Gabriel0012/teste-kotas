<template>
  <nav>
    <div class="align-middle">
      <img alt="Vue logo" src="../assets/Frame.png" />
      <input
        type="text"
        class="input-search"
        placeholder="O que você procura"
      />
    </div>

    <div class="buttons">
      <a href="" class="create-group"> + Criar Grupo </a>

      <a href="" class="my-groups">
        <i class="fas fa-cube"></i>
        Meus Grupos</a
      >

      <a href="" class="notification">
        <i class="far fa-bell"></i>
      </a>
    </div>
  </nav>
</template>

<script>
export default {
  name: "NavComponent",
  props: {
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;

  height: 50px;
  padding: 5px 25px;

  background-color: white;
  box-shadow: 0px 1px 1px #E1E1E1;
}

.input-search {
  background-color: white;

  border: 1px solid #e1e1e1;
  border-radius: 50px;

  font-size: 0.9rem;
  line-height: 1.2rem;

  height: 38px;
  width: 500px;

  margin-left: 32px;
  padding-left: 12px;
}

.input-search:focus {
  outline: 3px solid #00d95a94;
  border-color: #00d95a94;
}

.create-group,
.my-groups {
  text-decoration: none;
  color: rgba(0, 0, 0, 0.842);
  padding: 10px 20px;
  border-radius: 5px;
  font-weight: light;
  transition: all 0.25s;
}

.create-group:hover,
.my-groups:hover {
  text-decoration: underline;
  color: #00d95a;
}

.notification {
  font-size: 20px;
  color: #333;
  padding: 0 20px;
  transition: all 0.25s;
}

.notification:hover {
  color: #00d95a;
}

.align-middle {
  display: flex;
  align-items: center;
}
</style>
