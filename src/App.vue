<script setup>
import Item from './components/Item.vue'
</script>

<script>
import Data from "./Data/Services.json"
export default {
  data() {
    return {
      services: null
    }
  },
  mounted() {
    this.services = Data;
  }
}
</script>

<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <h1>Linktwoo</h1>
  <hr />
  <div class="items">
    <Item 
      v-for="service, index in services"
     :key="index"
     :item="service"
    />
  
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
html {
  background: url("https://user-images.githubusercontent.com/109248116/225467229-903c7c50-9126-4b32-b374-376ea8e66f48.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  min-height: 100%;
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
.items {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}
</style>
