<script setup lang="ts">
import {ref} from 'vue'

defineProps<{ msg: string }>()

const count = ref(0)


const items = [
  'https://picsum.photos/640/640?random=1',
  'https://picsum.photos/640/640?random=2',
  'https://picsum.photos/640/640?random=3',
  'https://picsum.photos/640/640?random=4',
  'https://picsum.photos/640/640?random=5',
  'https://picsum.photos/640/640?random=6'
]
</script>

<template>
  <UApp>

    <h1>{{ msg }}</h1>

     <UCard class="card">
       <UCarousel v-slot="{ item }" :items="items" :ui="{ item: 'basis-1/3' }">
         <img :src="item" width="234" height="234" class="rounded-lg">
       </UCarousel>
    </UCard>

    <p>
      Check out
      <a href="https://ui3.nuxt.dev/getting-started" target="_blank"
      >create-nuxt</a
      >, the official Vue + Nuxt  starter
    </p>
    <p>
      Learn more about IDE Support for nuxt in the
      <a
          href="https://ui3.nuxt.dev/getting-started"
          target="_blank"
      >Nuxt Docs Scaling up Guide</a
      >.
    </p>
    <p class="read-the-docs">Click on the Vue and Nuxt logos to learn more</p>
  </UApp>
</template>

<style scoped>

.read-the-docs {
  color: #888;
}
</style>
