<template>
  <h1>The List!</h1>
  <div class="container">
  <div class="about">
   <h2 class="name">{{ Destination.name }}</h2>
   <h2 class="why">{{ Destination.why }}</h2>
   <img :src="Destination.img" alt=""/>
   <h2 class="price">{{ Destination.price }}</h2>
   <h3>{{ clicked }}</h3>
   <button @click="increment">Add to Cart</button>

  </div>
</div>
</template>

<script setup>
import {ref} from "vue";
const props = defineProps({
  Destination: Object,
});

//clicker logic
const clicked = ref(0);
function increment() {
  clicked.value="added!";
}
</script>

<style scoped>
img {
  width:100px;
  height: 150px;
  align-items: center;
}

.about {
  display: flex;
  flex-wrap: wrap;
  background-color: rgb(249, 215, 221);
  margin: 5%;
  padding: 1%;
}

h2{
  align-items: center;
}

</style>