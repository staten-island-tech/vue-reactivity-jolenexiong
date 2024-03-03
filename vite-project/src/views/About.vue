<template>
 <div class="container"></div>
  <div class="about">
   <h2 class="name">{{ Destination.name }}</h2>
   <h2 class="why">{{ Destination.why }}</h2>
   <img :src="Destination.img" alt=""/>
   <h2 class="price">{{ Destination.price }}</h2>
   <h3>{{ clicked }}</h3>
   <button @click="addingtocart" class="addbtn"></button>
   </div>
</template>

<script setup>
import { ref, defineProps } from 'vue';

const props = defineProps ({
  Destination: Object,
  addtocart: Function,
})

const incart = ref([]);

const addingtocart = () => {
  props.addtocart(props.Destination)
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
