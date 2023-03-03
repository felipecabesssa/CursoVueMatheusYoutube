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
            this.nome = 'Matheus'
        }, 2000);

        this.lifeCycle();
    },
    mounted(){
        setTimeout(() => {
            this.nome = 'Felipe'
        }, 4000);

        this.lifeCycle();
    },
    methods: {
        lifeCycle(){
            console.log('Executou');
        }
    }
}
</script>