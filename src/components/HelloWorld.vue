<script setup>
import { ref, toRefs } from 'vue';

const props = defineProps({
  msg: {
    type: String,
    required: true
  },
  edad: Number
}) 

const emits = defineEmits(['hizoClick'])

const alerta = () => {
  emits('hizoClick', 20)
}
</script>

<template>
  <div class="greetings">
    <h1 class="red">{{ edad + 1  }}</h1>
    <h1 class="red">{{ edadMasUno }}</h1>
    <h3 @click="alerta" style="border:1px solid red">
      You’ve successfully created a project with
      <a href="https://vitejs.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>.
    </h3>
  </div>
</template>

<style scoped>
.red {
  color: red;
}
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
