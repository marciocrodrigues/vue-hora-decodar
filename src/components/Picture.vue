<template>
    <img :src="avatar" :alt="descricao">
</template>

<script>
export default {
    name: 'Picture',
    data() {
        return {
            avatar: "/imagens/avatar.png",
            descricao: "Marcio"
        }
    }
}
</script>