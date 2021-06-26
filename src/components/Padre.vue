<template>
  <div>
    <h2>Hola Soy Padre</h2>
    <Hijo ref="hijoRef" v-on:click="contar" v-on:value="catchValue" />
    <hr />
    <button type="button" @click="saludarHijo()">saludar hijo</button>
    <hr />
    <h3>{{ contador }}</h3>
  </div>
</template>

<script>
import Hijo from "./Hijo.vue";

export default {
  name: "Padre",
  data() {
    return {
      contador: 0,
    };
  },
  components: {
    Hijo,
  },
  methods: {
    saludarHijo() {
      this.$refs["hijoRef"].saludar();
    },
    contar(valor) {
      if (valor) {
        console.log(valor);
      }
      this.contador++;
    },
    catchValue(value) {
      //alert(value);
      console.log(value + 1);
    },
  },
};
</script>
