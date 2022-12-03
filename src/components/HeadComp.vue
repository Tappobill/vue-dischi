<template>
  <header>
    <div class="d-flex justify-content-center me-5 p-4 align-items-center">
      <div class="me-5">
        <label class="me-3" for="">Seleziona per Genere</label>
        <select name="" id="" v-model="valueOptionSelected">
          <option :value="element" v-for="(element, index) in arrayGeneriApptoHeader" :key="index">{{ element }}
          </option>
        </select>
      </div>

      <div>
        <label class="me-3" for="">Seleziona per Autore</label>
        <select name="" id="" @click="$emit('emitSceltaHeader', valueOptionSelected)" v-model="valueOptionSelected">
          <option :value="element" v-for="(element, index) in arrayAutoriApptoHeader" :key="index">{{ element }}
          </option>
        </select>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeadComp',
  props: {    
    arrayGeneriApptoHeader: Array,
    arrayAutoriApptoHeader: Array
  },
  data() {
    return {
      valueOptionSelected: ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
header {
  height: 10%;
  background-color: #2e3a46;
  color: white;
}
</style>
