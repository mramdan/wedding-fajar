<template>
  <section class="w-full relative flex flex-col justify-center gap-3 bg-prewedding bg-cover h-screen">
    <img src="@/assets/decoration-asset-1.png" class="w-6/12 mx-auto z-0">
    <div class="w-8/12 mx-auto text-center text-gray-100">
      <p>We Are Getting Married</p>
      <h1 class="satisfy-font text-5xl lg:text-6xl my-4 font-bold text-green-300">Fulan & Fulanah</h1>
      <small>Kepada yth Bapak / Ibu</small>
      <br>
      <strong>{{ query.to }}</strong>
      <br>
      <small>Ditempat</small>
    </div>
    <wave class="absolute -bottom-1 left-0 right-0"/>
  </section>
</template>

<script setup>

import { computed } from 'vue'
import { useRoute } from 'vue-router' 
import wave from '@/assets/svg/wave.svg'

const route = useRoute()
let query = computed(() => route.query)

if (route.query.to === undefined) query = { to: 'Saudara/i' } 

</script>
