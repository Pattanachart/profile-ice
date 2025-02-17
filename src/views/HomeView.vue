<template>
  <div class="text-end">{{ dateNow }}</div>
  <div class="text-center text-body-secondary h1 m-2 p-2">
    ภัทราวดี สังข์สม (OR) GREEN
  </div>
  <div class="container mt-5">
    <div
      id="carouselExample"
      class="carousel slide"
      style="max-width: 600px; margin: auto"
    >
      <div class="carousel-inner">
        <div
          class="carousel-item"
          :class="{ active: index === 0 }"
          v-for="(image, index) in images"
          :key="image"
        >
          <img :src="image" class="d-block w-100 rounded" style="" />
        </div>
      </div>
      <button
        class="carousel-control-prev"
        type="button"
        data-bs-target="#carouselExample"
        data-bs-slide="prev"
      >
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </button>
      <button
        class="carousel-control-next"
        type="button"
        data-bs-target="#carouselExample"
        data-bs-slide="next"
      >
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
    </div>
  </div>
</template>

<script setup lang="ts">
import dayjs from "dayjs";
import { ref } from "vue";

const dateNow = dayjs().format("MMMM D, YYYY h:mm A");
const images = ref([
  "/image/resume.png",
  "/image/1.jpg",
  "/image/2.jpg",
  "/image/3.jpg",
  "/image/4.jpg",
]);
</script>
