<template>
    <img :src="avatar" :alt="descricao" style="margin-top: 15px;">
</template>

<script>
export default {
    name: 'Picture',
    data(){
        return{
            avatar: "/img/avatar.png",
            descricao: "Felipe Henrique"
        }
    }
}
</script>