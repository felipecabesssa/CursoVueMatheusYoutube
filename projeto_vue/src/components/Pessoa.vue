<template>
<div>
    <h2>Esta é a descrição da pessoa: </h2>
    <p><strong>Essas infos/lista aqui em baixo estão isoladas no componente Info.vue</strong></p>
    <Info />
    <Injecaoinformacao />
    <Info />
    <p><strong>Aqui exemplo de formulario em componente isolado (USAMOS MUITO)</strong></p>
    <Form />
    
    

    
</div>
</template>

<script>
import Info from './Info.vue'
import Form from './form/Form.vue'
import Injecaoinformacao from './injecaoinformacao.vue'
export default {
  components: { Info, Injecaoinformacao, Form },
    name: 'Pessoa',
    data() {
        return {
            nome: 'Felipe'
        }
    }
}
</script>
