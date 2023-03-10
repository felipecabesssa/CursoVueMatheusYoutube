<template>
    <img :src="avatar" :alt="descricao" style="margin-top: 15px;">
    <MudarImagem @mudar-imagem="trocarImagem" />
</template>

<script>
import MudarImagem from './MudarImagem.vue'
export default {
  components: { MudarImagem },
    name: 'Picture',
    data(){
        return{
            avatar: "/img/avatar.png",
            descricao: "Felipe Henrique"
        }
    },
    methods: {
      trocarImagem() {
        this.avatar = '/img/euEDavi.PNG'
      }
    }
}
</script>