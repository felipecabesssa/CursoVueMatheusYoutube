<template>
    <div>
        <p>{{ compEmail }} - {{ email }}</p>
        <p v-if="esta_trabalhando">Estou trabalhando/Estudando no momento.</p>
        <p v-else>Estou só estudando no momento</p>
        <p v-if="usa_tecnologias">Utilizo as seguintes tecnologias:</p>
        <Tecnologias />
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <p>Para acessar meu portifólio <a v-bind:href="meu_link" target="_blank">clique aqui</a></p>
        <div>
            <button @click="showEmail">{{ textoBotao }}</button>
        </div>
    </div>
</template>

<script>
import Tecnologias from './Tecnologias.vue'
export default {
  components: { Tecnologias },
  name: 'Info',
  props: {
    email: String,
    esta_trabalhando: Boolean
  },
  data() {
      return {
          usa_tecnologias: true,
          mostrar_email: false,
          meu_link: 'http://felipesa.com.br/',
          textoBotao: 'Mostrar e-mail'
      }
  },
  methods: {
      showEmail(){
          this.mostrar_email = !this.mostrar_email
          if(!this.mostrar_email) {
              this.textoBotao = 'Mostrar e-mail'
          } else {
              this.textoBotao = 'Esconder e-mail'
          }
          console.log("Testando método");
      }
  }
}
</script>


