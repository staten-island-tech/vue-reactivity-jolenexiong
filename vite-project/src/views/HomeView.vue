<template>
  <div>
    <SceneCard v-for="Scene in Scenes" 
    :key="Scene.name" 
    :Destination="destination"/>
  </div>
</template>

<script setup>
import Scene from '@/components/icons/SceneCard.vue';
const Scene = [
  {
    answer: "Pamithi",
    clue1: "Victum was covered in bruises.",
    clue2: "https://manicpanic.com/cdn/shop/products/SUL15502_Raven-Human-Hair-Glam-Strip.jpg?v=1622166495&width=500",
    clue3: "Neighbors reported hearing NightCrawler by Travis Scott."
  },
]
</script>

<style scoped></style>
