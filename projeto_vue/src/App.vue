<template>
  <div>
    <hr>
    <h3 style="color: red; text-align: center;">Aula 1 a 6 - Components</h3>
    <hr>
    <PrimeiroComponente />

    <hr>
    <h3 style="color: red; text-align: center;">Aula 7 - LifeCycle Hooks - Gancho de Ciclo de vida</h3>
    <hr>
    <p>Muda o nome a cada 2 segundos (this.nome dentro do setTimeOut)</p>
    <LyfeCycle />

    <hr>
    <h3 style="color: red; text-align: center;">Aula 8 - Hierarquia de components</h3>
    <hr>
    <p>Separa as responsabilidades, cada componente com a sua</p>
    <p>Criando assim uma arvore de componentes, onde um depende do outro, ou não</p>
    <Pessoa />

  </div>
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LyfeCycle from './components/LifeCycle.vue'
import Pessoa from './components/Pessoa.vue'

export default {
  name: 'App',
  components: {
    PrimeiroComponente,
    LyfeCycle,
    Pessoa
  }
}
</script>