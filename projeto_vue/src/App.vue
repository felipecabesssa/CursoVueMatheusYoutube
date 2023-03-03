<template>
  <div>
    <hr>
    <h3 style="color: red; text-align: center;">Aula 1 a 6 - Components</h3>
    <hr>
    <PrimeiroComponente />
    <p>O dado de app é: {{ testando }}</p>

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

    <hr>
    <h3 style="color: red; text-align: center;">Aula 9 - Diretivas - v-if, v-show, v-for</h3>
    <hr>
    <p>A diretiva vai dentro da tag, exemplo de booleano v-if dentro do paragrafo = true exibe o paragrafo, false não</p>
    <p>V-Show é parecida com o v-if porem ela só exibe ou não</p>
    <p>Exemplos no componente Info.vue acima</p>
    <p>V-for exibe uma lista (um array) na aplicação</p>

    <hr>
    <h3 style="color: red; text-align: center;">Aula 10 - Argumentos - V-BIND</h3>
    <hr>
    <p><strong>Não precisa escrever v-bind:href= toda vez, basta os : ex :href= </strong></p>
    <Info />
    <Picture />

    <hr>
    <h3 style="color: red; text-align: center;">Aula 11 - Métodos</h3>
    <hr>
    <p>Email sera exibido somente após clicar via método (Component Info.vue)</p>
    <p>Método altera o booleano (mostrar_email) pra true or false ao clicar</p>
    <p>Condicional dentro do método showEmail muda o texto do botão</p>
    
    <hr>
    <h3 style="color: red; text-align: center;">Aula 12 - CSS - Global e Scoped</h3>
    <hr>
    <p>Background ta no global e</p>
    
    <p class="teste">Header (cabeçalho) abaixo - component Header ta scoped</p>
    
    <Header />

    <hr>
    <h3 style="color: red; text-align: center;">Aula 13 - Listas - Renderização - V-for</h3>
    <hr>

    <InfoComVfor />
    <br>
    <br>
    <br>
    <br>
    
  </div>
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LyfeCycle from './components/LifeCycle.vue'
import Pessoa from './components/Pessoa.vue'
import Info from './components/Info.vue'
import Picture from './components/Picture.vue'
import Header from './components/Header.vue'
import InfoComVfor from './components/InfoComVfor.vue'

export default {
  name: 'App',
  components: {
    PrimeiroComponente,
    LyfeCycle,
    Pessoa,
    Info,
    Picture,
    Header,
    InfoComVfor
  }
}
</script>

<style>
  body {
    background-color: #333;
    color: #fff;
  }

  a {
    color: red;
  }

  .teste {
    background-color: #000;
  }
</style>