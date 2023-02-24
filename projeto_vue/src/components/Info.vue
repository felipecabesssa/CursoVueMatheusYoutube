<template>
    <div>
        <p>Estou trabalhando/Estudando no momento.</p>
        <p>Utilizo as seguintes tecnologias:</p>
        <Tecnologias />
    </div>
</template>

<script>
import Tecnologias from './Tecnologias.vue'
export default {
  components: { Tecnologias },
    name: 'Info'
}
</script>