<script setup>

import {ref, computed} from 'vue';

let a = ref (0);
let b = ref (1);

// function add (xa,xb) {
//   console.log("addition is run ", {xa, xb})

//     a.value = xa;
//     a.value = xb;
//     return a.value+b.value;
// }

// const add = computed (() => {
//   console.log("the runtime is ");
//   return a.value + b.value;
// })

const add = computed ( {

  get(){
    console.log("run time is ");
    return a.value + b.value
  },
  set(xb){
    b.value = xb
  }

})


setTimeout(() => {

  add.value = 50
}, 2000)

// setTimeout(() => {
//   a.value=50;
//   b.value=20;
// }, 2000)

</script>

<template>

  <h1> Hello world </h1>
  <!-- <h1>{{ add() }}</h1>
  <h1>{{ add() }}</h1>
  <h1>{{ add() }}</h1>
  <h1>{{ add() }}</h1> -->

    <h1> {{ add }}</h1>
    <h1> {{ add }}</h1>
    <h1> {{ add }}</h1>
    <h1> {{ add }}</h1>
    <h1> {{ add }}</h1>
    <h1> {{ add }}</h1>


</template>
