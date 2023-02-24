<template>
  <hr>
  <h3>----- Aula 1 a 6 - Components -----</h3>
  <hr>
  <primeiroComponente />
  <hr>
  <h3>----- Aula 7 - LifeCycle Hooks - Gancho de Ciclo de vida -----</h3>
  <hr>
  <p>Muda o nome a cada 2 segundos (this.nome dentro do setTimeOut)</p>
  <lyfeCycle />
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LyfeCycle from './components/LifeCycle.vue' 

export default {
  name: 'App',
  components: {
    PrimeiroComponente,
    LyfeCycle
  }
}
</script>