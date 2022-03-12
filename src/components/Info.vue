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
        <div>
            <button @click="showEmail">{ textoBotao }</button>
        </div>
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
            mostrar_email: false,
            email: 'teste@teste.com.br',
            meu_link: 'https://www.google.com.br',
            textoBotao: 'Mostrar e-mail'
        }
    },
    methods: {
        showEmail() {
            this.mostrar_email = !this.mostrar_email
            if(this.mostrar_email) {
                this.textoBotao = 'Esconder e-mail';
            } else {
                this.textoBotao = 'Mostrar e-mail'
            }
        }
    }
}
</script>