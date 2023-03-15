<template>
  <div>
    <p>Componente de mensagem</p>
    <br>
    <div>
      <form id="burger-form">
        <div id="input-container">
          <label for="nome">Nome do cliente: </label>
          <input type="text" id="nome" v-model="nome" placeholder="Digite o seu nome">
        </div>

        <div id="input-container">
          <label for="pao">Escolha o pão: </label>
          <select name="pao" id="pao" v-model="pao">
            <option value="">Selecione seu pão</option>
            <option v-for="pao in paes" :key="pao.id" :value="pao.tipo">{{ pao.tipo }}</option>
          </select>
        </div>

        <div id="input-container">
          <label for="carne">Selecione a carne: </label>
          <select name="carne" id="carne" v-model="carne">
            <option value="">Selecione o tipo de carne</option>
            <option v-for="carne in carnes" :key="carne.id" :value="carne.tipo">{{ carne.tipo }}</option>
          </select>
        </div>

        <div id="input-container opcionais-container">
          <label id="opcionais-title" for="opcionais">Selecione os opcionais: </label>
          <div id="checkbox-container" v-for="opcional in opcionaisdata" :key="opcional.id">
            <input type="checkbox" name="opcionais" v-model="opcionais" :value="opcional.tipo">
            <span>{{ opcional.tipo }}</span>
          </div>
        </div>

        <div id="input-container">
          <input type="submit" class="submit-btn" value="Criar meu Burger">
        </div>
      </form>
    </div>

  </div>
</template>

<script>
export default {
  name: "BurgerForm",
  data() {
    return {
      paes: null,
      carnes: null,
      opcionaisdata: null,
      nome: null,
      pao: null,
      carne: null,
      opcionais: [],
      status: "Solicitado",
      msg: null
    }
  },
  methods: {
    async getIngredients() {

      const req = await fetch("http://localhost:3000/ingredientes");
      const data = await req.json();

      this.paes = data.paes;
      this.carnes = data.carnes;
      this.opcionais = data.opcionais;

    }
  },
  mounted() {
    this.getIngredients()
  }

}
</script>

<style scoped>
  #burger-form {
    max-width: 400px;
    margin: 0 auto;
  }

  #input-container {
    display: flex;
    flex-direction: column;
    margin-bottom: 20px;
  }

  label {
    font-weight: bold;
    margin-bottom: 15px;
    color: #222;
    padding: 0 10px;
    border-left: 4px solid #FCBA03;
  }

  input, select {
    padding: 0 10px;
    width: 400px;
  }

  #opcionais-container {
    flex-direction: row;
    flex-wrap: wrap;
  }

  #checkbox-container {
    display: flex;
    align-items: flex-start;
    width: 50%;
    margin-bottom: 20px;
  }

  #checkbox-container span, 
  #checkbox-container input {
    width: auto;
  }  

  #checkbox-container span {
    margin-left: 6px;
    font-weight: bold;
  }

  .submit-btn {
    background-color: #222;
    color: #FCBA03;
    font-weight: bold;
    border: 2px solid #222;
    padding: 10px;
    font-size: 16px;
    margin: 0 auto;
    cursor: pointer;
    transition: .5s;
  }

  .submit-btn:hover {
    background-color: transparent;
    color: #222;
  }

</style>
