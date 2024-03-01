<template>
 <div>
<h2>Your Cart</h2>
<ol>
  <li v-for="item in incart" :key="item.name"> {{ item.name }} - {{ item.why }} - {{ item.price }}</li>
</ol>
 </div>
</template>

<script setup>
import { ref } from 'vue';

const incart = ref([]);

const addtocart = function(item) {
  incart.value = [...incart.value, item];
}

</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
