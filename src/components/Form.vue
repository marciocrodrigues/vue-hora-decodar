<template>
    <div>
        <h2>Meu formulario</h2>
        <form action="" @submit="enviarFormulario($event)">
            <div>
                <input type="text" v-model="name" />
            </div>
            <div>
                <input type="text" v-model="email" />
            </div>
            <Submit />
        </form>     
        <p>Conteúdo</p>
        <p>Conteúdo</p>
        <p>Conteúdo</p>
    </div>
</template>

<script>

import InputText from './Form/InputText.vue';
import Submit from './Form/Submit.vue'

export default {
    name: 'Form',
    components: {
        InputText,
        Submit
    },
    data() {
        return {
            name: '',
            email: ''
        }
    },
    methods: {
        enviarFormulario(e) {
            e.preventDefault();
            const name = this.name;
            const email = this.email;
            console.log(`O nome é ${name}`);
            console.log(`O e-mail é ${email}`);
        }
    }
}
</script>

<style scoped>
    p {
        margin: 150px;
    }
</style>