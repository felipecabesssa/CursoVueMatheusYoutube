<template>
    <h1>Olá Vue!</h1>
    <h3>Meu nome é: {{ nome }} {{ sobrenome }}</h3>
    <p><strong>Profissão:</strong> {{ profissao }}</p>
</template>

<script>
export default {
    name: 'PrimeiroComponente',
    data(){
        return{
            nome: "Felipe",
            sobrenome: "Henrique",
            profissao: "Desenvolvedor WEB"
        }
    }
}
</script>