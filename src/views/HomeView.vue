<template>
  <svg class="absolute">
    <filter id="noiseFilter">
      <feTurbulence
        type="fractalNoise"
        baseFrequency="4.29"
        numOctaves="4"
        stitchTiles="stitch"
      />
    </filter>
  </svg>
  <div class="w-full md:w-[46rem]">
    <div>
      <router-link to="/" class="font-bold">dhritiman</router-link>
    </div>
    <div class="mt-12 font-medium">
      <p class="text-justify">
        hi i'm a 20y/o guy with a computer, currently a BCA final year student.
        i'm interested in exploring things related to computers and web. i'm
        also interested in creating aesthetically pleasing and minimalistic
        interfaces.
      </p>

      <p class="my-3">i'm trying to get my life together rn.</p>

      <!-- <p>you can check my cv <a href="">here</a>.</p> -->

      <p>find me on:</p>

      <ul class="list-disc pl-7 mt-1">
        <li v-for="(item, index) in LINKS" :key="index">
          <a class="hover:underline underline-offset-2" :href="item.url">
            {{ item.name }}
          </a>
        </li>
      </ul>
    </div>
    <!-- <div class="mt-8">
    <p class="font-bold">blogs</p>
  </div> -->
  </div>
</template>

<script setup lang="ts">
const LINKS = [
  { name: "github", url: "https://github.com/dhritiman1" },
  { name: "twitter", url: "https://twitter.com/dhritimanvwv" },
  { name: "read.cv", url: "https://read.cv/vherte" },
];
</script>
