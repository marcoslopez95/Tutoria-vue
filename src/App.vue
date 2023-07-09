<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from '@/components/TheWelcome.vue'
import { ref } from 'vue'
// 
/**
 * 
 */
const nombre = ref('')
const miEdad = ref(15)

const sumarDiezAEdad = (valor) => {
  miEdad.value += valor; 
}

const restarDiezAEdad = (valor) => {
  miEdad.value -= valor; 
}
</script>

<template>
  <header>
    <!-- {{ nombre }} -->
    <!-- <input v-model="nombre" type="text" /> -->
    <input v-model="miEdad" type="number" />
    <!-- <img 
      alt="Vue logo" class="logo" 
      src="./assets/logo.svg" 
      width="125" height="125" /> -->

    <!-- <div class="wrapper">
      <HelloWorld @hizo-click="sumarDiezAEdad" :edad="10" msg="tu puedes!" />
      <HelloWorld @hizoClick="restarDiezAEdad" :edad="miEdad" msg="Empatica" />
    </div> -->
  </header>

  <main>
    <!-- <TheWelcome /> -->
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
