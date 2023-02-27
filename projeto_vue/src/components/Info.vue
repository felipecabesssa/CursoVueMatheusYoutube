<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando/Estudando no momento.</p>
        <p v-else>Estou só estudando no momento</p>
        <p v-if="usa_tecnologias">Utilizo as seguintes tecnologias:</p>
        <Tecnologias />
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <p>Para acessar meu portifólio <a v-bind:href="meu_link" target="_blank">clique aqui</a></p>
        <Picture />
    </div>
</template>

<script>
import Picture from './Picture.vue'
import Tecnologias from './Tecnologias.vue'
export default {
  components: { Tecnologias, Picture },
    name: 'Info',
    data() {
        return {
            esta_trabalhando: false,
            usa_tecnologias: true,
            mostrar_email: true,
            email: 'felipesoares100@hotmail.com',
            meu_link: 'http://felipesa.com.br/'
        }
    }
}
</script>