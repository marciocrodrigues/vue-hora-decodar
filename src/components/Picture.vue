<template>
    <div>
        <img :src="avatar" :alt="descricao">
        <MudarImagem @mudar-imagem="trocarImagem" />
    </div>
</template>

<script>
import MudarImagem from './MudarImagem.vue';
export default {
    name: 'Picture',
    components: {
        MudarImagem
    },
    data() {
        return {
            avatar: "/imagens/avatar.png",
            descricao: "Marcio"
        }
    },
    methods: {
        trocarImagem() {
            if (this.avatar.includes('avatar2')) {
                this.avatar = "/imagens/avatar.png";
            } else {
                this.avatar = "/imagens/avatar2.png";
            }
        }
    }
}
</script>