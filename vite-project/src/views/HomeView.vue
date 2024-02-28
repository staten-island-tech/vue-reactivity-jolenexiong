<template>
  <div>
  <DestCard v-for="destination in destinations"
  :key="destination.name"
  :Destination="destination"/>
  </div>
 </template>
 name
 <script setup>
 import DestCard from '@/components/icons/DestCard.vue';

//  const addToCart = function

 const destinations = [
         {
           name: "Rare Beauty Positive Light Tinted Moisturizer",
           why: "good light coverage for everyday use AND has SPF",
           price: "$30",
           img: "https://www.sephora.com/productimages/sku/s2557072-main-zoom.jpg?imwidth=1224",
         },
         {
           name: "Charlotte Tilburry Highlight Beauty Light Wand",
           why: "it's so fun and easy to use and has a great natural golden highlight",
           price: "$42",
           img: "https://images.ctfassets.net/wlke2cbybljx/2pwv1Jiw2bOZQ6anGfCfsI/3bfba2e20f3019d5ced51dfeeaa52ebf/Glowgasm_BeautyLightWand_Goldgasm_Open.png?w=500&h=500&fit=fill&fm=jpg&bg=",
         },
         {
           name: "Fenty Gloss Bomb Cream(shade Fruit Snackz)",
           why: "has nice pigment and shine, also smells rlly nice + doesn't feel too heavy despite being a cream",
           price: "$22",
           img: "https://encrypted-tbn2.gstatic.com/shopping?q=tbn:ANd9GcRwux7GCi2fSrN78Cr8nkUuMBXLk8WHuPNKi34VNqUQ6DBoFseQZD0waOR4_-zIQ53VnXrGv1-YBg2Jq7K5FNrEyfvT4VxZeHv3A3UL1EIv_Uwqw3TMM4I3y94dfKpzs5d5Faiq7Gg&usqp=CAc",
         },
         {
           name: "Sheseido Eyelash Curler",
           why: "yes it may be $24 but i swear on this eyelash curler. trust, it works so great with my awful asian lashes",
           price: "$24",
           img: "https://encrypted-tbn1.gstatic.com/shopping?q=tbn:ANd9GcRrGqi9YQdJjgBiI8S9qBYrEn0BR_Nlx9Xps8rou_NIHjt7yEjGKTihbX1RoSBJzj6MB7TVLqHATcnij_FvIy2Z4O-0iz_WwS_BWc__uP7emh7bjDLzbp66BH1R8DdzsXUpM8wA1DUd&usqp=CAc",
         },
         {
           name: "Charlotte Tilbury Blush Beauty Light Wand",
           why: "i don't wear blush often but again, easy and fun application, rlly good cream blush w good pigment",
           price: "$42",
           img: "data:image/webp;base64,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",
         },
         {
           name: "Dior Lip Maximizer(Shade 015)",
           why: "this has a really nice delicate red pigment and a fun minty feeling, honestly i would say get this rather than the overrated lip oil",
           price: "$40",
           img: "https://encrypted-tbn2.gstatic.com/shopping?q=tbn:ANd9GcTF2_HUSOg7-xnjNGn7JJ9HgQldUJJf70operrT3LXOlmy6srEE6CxmtnoKNzac260SXSi58dq5EaudAztEZ_v7wvvKvYd4s1kq8UDJh5piOfC4yvP7uFFTVHzLbpsZPOWyE00xwDg&usqp=CAc",
         },
       ];
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
 