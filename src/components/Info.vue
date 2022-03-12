<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Estou em busca de novas oportunidades</p>
        <p>Utilizo as seguintes tecnologias para back-end:</p>
        <ul>
            <li v-for="(technology, index) in backend_technologies" v-bind:key="index">{{technology}}</li>
        </ul>
        <p>Utilizo as seguintes tecnologias para front-end:</p>
        <ul>
            <li v-for="technology in frontend_technologies" :key="technology.id">{{ technology.language }}</li>
        </ul>
        <div>
            <button @click="showEmail">{{ textoBotao }}</button>
        </div>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <p class="teste">Para acessar meu portfólio <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a></p>
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
            textoBotao: 'Mostrar e-mail',
            backend_technologies: ['Javascript', 'C#'],
            frontend_technologies: [
                { id: 1, language: 'ReactJS' },
                { id: 2, language: 'Angular' },
                { id: 3, language: 'Vue' }
            ]
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

<style>
    .pragrafo-pai {
        color: red;
    }
</style>>
