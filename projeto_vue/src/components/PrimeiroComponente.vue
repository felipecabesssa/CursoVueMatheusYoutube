<template>
    <div>
        <h2>Olá Vue!</h2>
        <h3>Meu nome é: {{ nome }} {{ sobrenome }}</h3>
        <p><strong>Profissão:</strong> {{ profissao }}</p>
        <Reutilizacao />
        <Reutilizacao />
       
    </div>
</template>

<script>
import Reutilizacao from './Reutilizacao.vue'

export default {
    name: 'PrimeiroComponente',
    components: {
        Reutilizacao
    },
    data(){
        return{
            nome: "Felipe",
            sobrenome: "Henrique",
            profissao: "Desenvolvedor WEB"
        }
    }
}
</script>