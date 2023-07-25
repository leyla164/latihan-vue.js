<template>
    <div>
       <b>Nama : {{ nama }}</b>
       <br>
       <b>Umur : {{ umur }}</b>
    </div>
</template>

<script>
//import MyComponent from './mycomponents.vue'

export default {
      props: ['nama','umur']
    }

</script>

<style>
   h1 {
     color: black;
   }
  p {
    size: 16px;
  }  
</style>