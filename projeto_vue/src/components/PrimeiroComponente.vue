<template>
    <div>
        <h2>Olá Vue!</h2>
        <h3>Meu nome é: {{ nome }} {{ sobrenome }}</h3>
        <p><strong>Profissão:</strong> {{ profissao }}</p>
    </div>
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