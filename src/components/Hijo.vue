<template>
  <div>
    <p>Hola Soy Hijo</p>
    <button type="button" @click="onClick()">Hijo Click</button>
    <hr />
    <button type="button" @click="emitValue()">Emit value</button>
  </div>
</template>

<script>
export default {
  name: "Hijo",
  data() {
    return {
      nombre: "",
    };
  },
  methods: {
    saludar() {
      alert("hola soy Hijo");
    },
    onClick() {
      this.$emit("click");
    },
    emitValue() {
      this.$emit("value", 2);
    },
  },
};
</script>
