<template>
  <nav>
    <div class="align-middle">
      <img alt="Vue logo" src="../assets/Frame.png" />
      <div class="search">
        <input
          type="text"
          class="input-search"
          placeholder="O que você procura?"
        />
      </div>
    </div>

    <div class="menu">
      <a href="" class="menu-bars">
        <i class="fas fa-bars"></i>
      </a>
    </div>
    <div class="buttons">
      <a href="" class="create-group">
        <i class="fas fa-plus"></i>
        Criar Grupo
      </a>

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
  props: {},
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
  box-shadow: 0px 1px 1px #e1e1e1;
}

.search::before {
  font-family: "Font Awesome 5 Free";
  font-weight: 900;
  content: "\f002";
  color: #3c5672;

  position: absolute;
  top: 15px;
  left: 150px;
}

.input-search {
  background-color: white;

  border: 2px solid #e1e1e1;
  border-radius: 50px;

  font-size: 0.9rem;
  line-height: 1.2rem;

  height: 32px;
  width: 500px;

  margin-left: 32px;
  padding-left: 50px;
}

.input-search:focus {
  outline: 1px solid #00d95a94;
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

.buttons a {
  font-size: 12px;
}

.buttons a i {
  margin-right: 5px;
  font-size: 15px !important;
  color: #30455c;
}

.create-group:hover,
.my-groups:hover {
  text-decoration: underline;
  color: #00d95a;
}

.notification {
  font-size: 20px !important;
  color: #333;
  padding: 0 20px;
}

.notification .far {
  transition: all 0.25s;
}

.notification:hover .far {
  color: #00d95a !important;
}

.align-middle {
  display: flex;
  align-items: center;
}

@media screen and (min-width: 481px) {
  .menu-bars {
    display: none;
  }
}

@media screen and (max-width: 480px) {
  .menu-bars {
    color: #333;
    text-decoration: none;
  }

  .buttons {
    display: none;
  }

  .input-search {
    width: 200px;
  }

  img {
    width: 60px;
  }

  .search::before {
    left: 130px;
  }
}
</style>
