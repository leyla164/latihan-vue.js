<script setup>
import { TheCard, Rating } from 'flowbite-vue'
</script>
<template>

<br>
<p style="font-size: xx-large;"><center><b>Summer Outfits</b></center></p>
<br>
<div class="flex flex-row">
  <div class="grid grid-cols-1 gap-1 m-8">
    <the-card variant="image" img-src="https://i.pinimg.com/564x/22/3c/ed/223ced6cbaecb63ce6a5d9c512a52f23.jpg" img-alt="Desk">
    <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Kendall Jenner Just wore the Coolest Olsen-Inspired Summer Outfit</h5>
    <p class="font-normal text-gray-700 dark:text-gray-400">
      “Lagi cari kardigan yang murah, bahan dan kualitas oke? Ya Sweaterku solusinya!
    </p>

  <br>
  <Rating :rating="4">
    <template #besideText>
        <p class="ml-2 text-sm font-medium text-gray-500 dark:text-gray-400">4.95 out of 5</p>
      </template>
  </Rating>

  </the-card>
</div>

  <br>
  <div class="basis-1/4  mz-5">
    <the-card variant="image" img-src="https://i.pinimg.com/564x/51/82/d5/5182d5956b23a234638b52dcbfc76667.jpg" img-alt="Desk">
    <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">great vest for spring</h5>
    <p class="font-normal text-gray-700 dark:text-gray-400">
      “Lagi cari rompi yang murah, bahan dan kualitas oke? Ya Sweaterku solusinya!""
    </p>

  <br>
  <Rating :rating="4">
    <template #besideText>
        <p class="ml-2 text-sm font-medium text-gray-500 dark:text-gray-400">4.95 out of 5</p>
      </template>
  </Rating>

  </the-card>
  </div>

  <br>
  <div class="basis-1/4  mz-5">
    <the-card variant="image" img-src="https://i.pinimg.com/564x/f5/7f/69/f57f6978cbe9d557e402350bccf655a5.jpg" img-alt="Desk">
    <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">A Few Cosy Pieces For Chilly  Summer Outfit</h5>
    <p class="font-normal text-gray-700 dark:text-gray-400">
      “Lagi cari kardigan yang murah, bahan dan kualitas oke? Ya Sweaterku solusinya!"
    </p>

  <br>
  <Rating :rating="4">
    <template #besideText>
        <p class="ml-2 text-sm font-medium text-gray-500 dark:text-gray-400">4.95 out of 5</p>
      </template>
  </Rating>

  </the-card>
  </div>
   
  <div class="basis-1/4  mz-5">
    <the-card variant="image" img-src="https://i.pinimg.com/564x/fc/26/9b/fc269bfa7f801d82bf1e2f82eceeafa4.jpg" img-alt="Desk">
    <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">I Never Liked This Colour Trend Until I Saw & Other Stories</h5>
    <p class="font-normal text-gray-700 dark:text-gray-400">
      “Lagi cari kardigan yang murah, bahan dan kualitas oke? Ya Sweaterku solusinya!"
    </p>

  <br>
  <Rating :rating="4">
    <template #besideText>
        <p class="ml-2 text-sm font-medium text-gray-500 dark:text-gray-400">4.95 out of 5</p>
      </template>
  </Rating>
  </the-card>
  </div>

</div>
 
</template>