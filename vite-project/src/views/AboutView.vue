
<template>
  <div>
    <CharacterCard v-for = "Card in Cards"
    :key="Character.name"
    :Destination="destination"/>
  </div>
</template>

<script>
import CharacterCard from '@components/icons/CharacterCard.vue'
const Characters= [
  {
    name: "June",
    hair: "short,black",
    hobbies: ""
    
  },
  {
    name: "Jolene",
  
  }
  {
    name: "Haashne",
    
  }
]

</script>

<style scoped>

</style>
