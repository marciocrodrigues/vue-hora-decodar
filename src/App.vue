<template>
  <div>
    <Header :esta_logado=false />
    <PrimeiroComponente />
    <p class="pragrafo-pai">O dono desse app é: {{ testando }}</p>
    <LifeCycle />
    <Pessoa />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import PrimeiroComponente from './components/PrimeiroComponente.vue';
import LifeCycle from './components/LifeCycle.vue';
import Pessoa from './components/Pessoa.vue';

export default {
  components: { 
    Header,
    PrimeiroComponente,
    LifeCycle,
    Pessoa
  },
  data() {
    return {
      testando: 'Marcio'
    }
  },
  name: 'App'
}
</script>

<style>
  body {
    background-color: #333;
    color: #FFF;
  }

  a {
    color: red;
  }

  .teste {
    background-color: #000;
  }
</style>