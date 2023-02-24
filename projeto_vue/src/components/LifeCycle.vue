<template>
    <h2>Meu nome é: {{ nome }}</h2>
</template>

<script>
export default {
    name: 'LyfeCycle',
    data(){
        return {
            nome: 'Ainda não sei'
        }
    },
    created(){
        setTimeout(() => {
            this.nome = 'Felipe'
        }, 2000)
    },
    mounted(){
        setTimeout(() => {
            this.nome = 'Matheus'
        }, 4000)
    }
}
</script>