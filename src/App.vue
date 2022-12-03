<template>
  <div id="app">
    <HeadComp @emitSceltaHeader="sceltaUtente" :arrayGeneriApptoHeader="arrayGeneriApp"
      :arrayAutoriApptoHeader="arrayAutoriApp" />
    <MainComp :selezioneApptoMain="opzioneSelezionata" @emitAutoriMain="listaAutori" @emitGeneriMain="listaGeneri" />
  </div>
</template>

<script>
import HeadComp from './components/HeadComp.vue'
import MainComp from './components/MainComp.vue'

export default {
  name: 'App',
  components: {
    HeadComp,
    MainComp
  },
  data() {
    return {
      arrayGeneriApp: [],
      arrayAutoriApp: [],
      opzioneSelezionata: " "
    }
  },
  methods: {
    listaGeneri(arrayGeneriMaintoApp) {
      this.arrayGeneriApp = arrayGeneriMaintoApp
    },
    listaAutori(arrayAutoriMaintoHeader) {
      this.arrayAutoriApp = arrayAutoriMaintoHeader
    },
    sceltaUtente(sceltaHeadertoApp) {
      this.opzioneSelezionata = sceltaHeadertoApp
    }
  }
}
</script>

<style lang="scss">
#app {
  height: 100vh;
}
</style>
