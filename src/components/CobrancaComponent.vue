<template>
  <div class="card">
    <ul>
      <li>
        <span>Mensalidade</span>
        <span>{{ formatPrice(mensalidade) }}</span>
      </li>
      <li>
        <span>Kotas</span>
        <span class="kotas">
          {{ kotas }}
          <button @click.stop="increase()">
            <i class="fas fa-plus"></i>
          </button>
          <button @click.stop="decrease()">
            <i class="fas fa-minus"></i>
          </button>
        </span>
      </li>
      <li>
        <span>Caução <i class="fas fa-info-circle"></i> </span>
        <span>{{ formatPrice(caucao) }}</span>
      </li>
      <li class="total">
        <span>Total da inscrição</span>
        <span>{{ total() }}</span>
      </li>
    </ul>

    <div class="participar">
      <div class="cols">
        <p>{{ formatPrice(assinatura) }}</p>
        <p>{{ formatPrice(snd) }}</p>
        <p>{{ formatPrice(fst) }}</p>
      </div>

      <input type="range" min="1" max="3" value="50" class="slider" step="1" />

      <div class="cols-label">
        <p>Assinatura</p>
        <p>Segundo mês</p>
        <p>Último mês</p>
      </div>

      <button>Participar</button>
    </div>
  </div>
  <p class="text-center helper">
    Você ainda não será cobrado
  </p>
</template>
<script>
export default {
  name: "CobrancaComponent",
  data: () => {
    return {
      mensalidade: 15,
      assinatura: 30,
      snd: 15,
      fst: 0,
      caucao: 15,
      kotas: 1,
    };
  },
  methods: {
    formatPrice(value) {
      let val = (value / 1).toFixed(2).replace(".", ",");
      return "R$ " + val.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ".");
    },

    total() {
      const total = this.kotas * this.mensalidade + this.caucao;
      return this.formatPrice(total);
    },

    decrease() {
      if (this.kotas > 1) {
        this.kotas -= 1;
      }
    },

    increase() {
      this.kotas += 1;
    },
  },
};
</script>

<style scoped>

@media screen and (max-width: 480px) {
  .card {
    border-radius: 0 !important;
  }
}

.card {
  background-color: white;
  padding: 0;
  /* width: 319px; */
}

ul {
  padding: 0;
}

.slider {
  width: 100%;

  -webkit-appearance: none;
  width: 100%;
  height: 2px;
  background: #01b1ec;
}

.slider::-moz-range-thumb {
  /* margin: 10px; */
  border: 1px solid #01b1ec;
  background: #01b1ec;
  cursor: pointer;

  outline: 1px solid #01b1ec;
}

li {
  display: flex;
  justify-content: space-between;
  list-style: none;
  border-bottom: 1px solid #e1e1e1;
}

.participar {
  padding: 12px;
}

.participar button {
  background-color: #01b1ec;
  width: 100%;
  color: white;
  font-size: 16px;
  padding: 16px;
  border: 0;
  border-radius: 5px;
  cursor: pointer;
  transition: all 0.25s;
  margin-top: 25px;
}

.participar button:hover {
  background-color: #0294c5;
}

.participar button:focus {
  outline: 5px solid #0294c596;
}

.fa-info-circle {
  margin-top: 5px;
  margin-left: 10px;
  color: #e1e1e1;
}

li span {
  padding: 16px;
  font-size: 14px;
}

li span:first-child {
  color: #616161;
}

li span:nth-child(2) {
  color: black;
}

li span:last-child {
  border: none !important;
}

.total span {
  color: black !important;
  font-weight: 700;
}

.cols,
.cols-label {
  display: flex;
  justify-content: space-between;
}

.cols-label p {
  font-size: 10px;
  font-weight: 300;
  color: #141728;
}

.cols p {
  font-size: 10px;
  font-weight: 400;
  color: #141728;
}

.cols p:last-child {
  color: #26b36a !important;
}

p.helper {
  color: #616161;
  font-weight: 300;
  font-size: 10px;
}

.kotas button {
  margin-left: 3px;
  background-color: #01b1ec;
  border-radius: 50%;
  color: white;
  width: 25px;
  height: 25px;
  border: 0;
  cursor: pointer;
  text-align: center;
  transition: all 0.25s;
}

.kotas button:hover {
  background-color: #0294c5;
}

.kotas button:focus {
  outline: 3px solid #0294c596;
}

.kotas button .fas {
  font-size: 12px;
}
</style>
