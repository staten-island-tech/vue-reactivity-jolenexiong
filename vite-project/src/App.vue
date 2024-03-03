<script setup>
import { ref } from 'vue';
import HelloWorld from './components/HelloWorld.vue'



const cart = ref([]);

const addtocart = function(item){
  cart.value.push(item);
};

</script>

<template>
  <header>
    
    <div class="wrapper">
      <HelloWorld msg="Jolene's Makeup Essentials" />

      

      <div class="cartsection">
        <h1><p>Cart: {{ cart.length }}</p></h1>
        
      </div>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}


nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}


nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }


  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}

.cartsection {
  width: 50vw;
}
</style>
