
<template>
    <div>
    <h1>Murder at Staten Island Tech! Who dunnit?!?</h1>
    <div class="showclues">
        <h2>{{ Scene.clue1 }}</h2>;
        <h2>{{ Scene.clue2 }}</h2>;
        <h3>{{ clicked }}</h3>;
    </div>
    </div>
</template>

<script setup>
import {ref} from "vue";
const props= defineProps({
    destination: Object,
})


const clicked = ref(0);
function increment(){
    clicked.value++;
}
</script>

<style scoped>
showclues{
    width:300px;
    height:350px;
    
}</style>