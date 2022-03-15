<template>
    <div>
        <h2>Esta é a descrição da pessoa: {{ nome }} </h2>
        <Info :email="email" :esta_trabalhando="esta_trabalhando" />
        <Form />
    </div>
</template>

<script>

import Info from './Info.vue';
import Form from './Form.vue';

export default {
    name: 'Pessoa',
    components: {
      Info,
      Form
    },
    data() {
        return {
            nome: 'Marcio',
            email: 'marcio2022@teste.com.br',
            esta_trabalhando: true
        }
    }
}
</script>