<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Estou em busca de novas oportunidades</p>
        <p>Utilizo as seguintes tecnologias</p>
        <ul>
            <li>Javascriopt</li>
            <li>C#</li>
            <li>ReactJs</li>
            <li>Angular</li>
        </ul>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <p>Para acessar meu portfólio <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a></p>
        <Picture />
    </div>
</template>

<script>
import Picture from './Picture.vue';

export default {
    components: { Picture },
    name: 'Info',
    data() {
        return {
            esta_trabalhando: true,
            mostrar_email: true,
            email: 'teste@teste.com.br',
            meu_link: 'https://www.google.com.br'
        }
    }
}
</script>