<template>
  <div>
    <SceneCard v-for="Scene in Scenes" 
    :key="Scene.name" 
    :Scene="scene"/>
  </div>
</template>

<script setup>
import SceneCard from '@/components/SceneCard.vue';
const Scenes = [
  {
    answer: "Pamithi",
    clue1: "Victum was covered in bruises.",
    clue2: "https://manicpanic.com/cdn/shop/products/SUL15502_Raven-Human-Hair-Glam-Strip.jpg?v=1622166495&width=500",
  },
  {
    answer: "June",
    clue1: "Orange peels were found at the scene of the crime.",
    clue2: "https://i.pinimg.com/originals/d4/95/e0/d495e0f73715837793ddda0d52f61662.jpg",
  },
  {
    answer: "Haashne",
    clue1: "Victim was a member of South Asian Club notorious for skipping practice.",
    clue2: "https://www.shutterstock.com/image-vector/dirty-grunge-sneaker-footprint-600nw-1172154979.jpg"
  },
  {
    answer: "Reese",
    clue1:"https://i5.walmartimages.com/seo/Summer-Fridays-Lip-Butter-Balm-Pink-Sugar_6a734c64-6ade-425c-bed5-3cae35546d84.3c4933ea73e4242cc95348ba1122727c.jpeg",
    clue2: "Murder on the Dancefloor was heard by neighbors",
  },
  {
    answer: "Jolene",
    clue1: "https://media-photos.depop.com/b1/38869099/1525399238_b7c4ccc03bfb4806843938639ac4178d/P0.jpg",
    clue2: "Victim claimed they hated Lana Del Rey",
  }
 
]




</script>

<style scoped></style>
