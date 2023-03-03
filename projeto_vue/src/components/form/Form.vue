<template>
    <form action="" @submit="enviarFormulario($event)">
        <div>
            <input type="text" v-model="name">
        </div>
        <div>
            <input type="text" v-model="email">
        </div>
        <div>
            <Submit />
        </div>
    </form>
</template>

<script>
import InputText from './InputText.vue'
import Submit from './Submit.vue'
export default {
    name: 'Form',
    components: {
        InputText,
        Submit
        
    },
    Data(){
        return {
            name: '',
            email: ''
        }
    },
    methods: {
        enviarFormulario(e){

            e.preventDefault();

            const name = this.name;
            const email = this.email;

            console.log('Formulário enviado !');
            console.log('O nome é: ' + name);
            console.log('O email é: ' + email);

            // Ajax - manda os dados em transação assincrona

            // Inserir no banco de dados
        }
    }
}
</script>
