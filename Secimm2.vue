<script setup>
import { TheCard, Rating } from 'flowbite-vue'
</script>
<template>

<br>
<p style="font-size: xx-large;"><center><b>Summer Outfits</b></center></p>
<br>
<div class="flex flex-row">
  <div class="grid grid-cols-1 gap-1 m-8">
    <the-card variant="image" img-src="https://i.pinimg.com/564x/cd/ae/b6/cdaeb67e11fa1caf78371f6925318949.jpg" img-alt="Desk">
    <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Kendall Jenner Just wore the Coolest Olsen-Inspired Summer Outfit</h5>
    <p class="font-normal text-gray-700 dark:text-gray-400">
        “Lagi cari baju yang murah, bahan dan kualitas oke? Ya Sweaterku solusinya!"
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
    <the-card variant="image" img-src="https://i.pinimg.com/564x/74/6e/22/746e228dff1f9c1d4adb4ad751168fda.jpg" img-alt="Desk">
    <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">great vest for spring</h5>
    <p class="font-normal text-gray-700 dark:text-gray-400">
        “Lagi cari baju yang murah, bahan dan kualitas oke? Ya Sweaterku solusinya!"
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
    <the-card variant="image" img-src="https://i.pinimg.com/564x/d3/f5/89/d3f5899df8eb94fd6066bf2505bd594a.jpg" img-alt="Desk">
    <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">A Few Cosy Pieces For Chilly  Summer Outfit</h5>
    <p class="font-normal text-gray-700 dark:text-gray-400">
        “Lagi cari baju yang murah, bahan dan kualitas oke? Ya Sweaterku solusinya!"
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
    <the-card variant="image" img-src="https://i.pinimg.com/564x/a0/f6/14/a0f614b4b0c5358e5dff2e8622d302a6.jpg" img-alt="Desk">
    <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">I Never Liked This Colour Trend Until I Saw & Other Stories</h5>
    <p class="font-normal text-gray-700 dark:text-gray-400">
        “Lagi cari baju yang murah, bahan dan kualitas oke? Ya Sweaterku solusinya!
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