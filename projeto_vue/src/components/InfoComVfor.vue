<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando/Estudando no momento.</p>
        <p v-else>Estou só estudando no momento</p>
        <div>
            <p v-if="usa_tecnologias">Tecnologias Backend:</p>
            <ul>
                <li v-for="(tecnologias, index) in tecnologias_backend" v-bind:key="index">
                    {{ tecnologias }}
                </li>
            </ul>
        </div>

        <div>
            <p v-if="usa_tecnologias">Tecnologias Frontend:</p>
            <ul>
                <li v-for="(tecnologias, index) in tecnologias_frontend" :key="index">
                    {{ tecnologias.id }} - {{ tecnologias.language }} 
                </li>
            </ul>
        </div>
        
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <p>Para acessar meu portifólio <a v-bind:href="meu_link" target="_blank">clique aqui</a></p>
        <div>
            <button @click="showEmail">{{ textoBotao }}</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Info',
    data() {
        return {
            esta_trabalhando: false,
            usa_tecnologias: true,
            mostrar_email: false,
            email: 'felipesoares100@hotmail.com',
            meu_link: 'http://felipesa.com.br/',
            textoBotao: 'Mostrar e-mail',
            tecnologias_backend: ['JAVA - Spring', 'JS - Vue', 'SQL Server'],
            tecnologias_frontend: [
                {id: 1, language: 'HTML'},
                {id: 2, language: 'CSS'},
                {id: 3, language: 'Vue'}
            ]
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

<style scoped>
    body{
        padding-top: ;
    }
</style>
