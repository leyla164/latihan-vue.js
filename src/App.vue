<script setup>
import { ref } from 'vue'

const msg = "Hello world";
const rawHtml = "<li>Daftar 1</li>";
const vhtml = "<li>Apa yaa</li>";

let a = 10
let b = 5
let c = a + b

</script>

<template>
   <div id="app">
       <span>{{ msg }}</span> <br>
       <span v-html="rawHtml"></span>
       <span v-bind:id="dynamicId"></span>
       <button :disabled="isButtonDisabled">Button</button> <br>
       <span style="color:brown" v-html="vhtml"></span> <br>
       
       bil 1 = {{ a }} <br>
       bil 2 = {{ b }} <br>
       hasil bil 1  + bil 2 = {{ c }}
   </div>

</template>