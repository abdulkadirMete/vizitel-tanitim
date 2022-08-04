<template>
  <carousel :settings="settings">
    <slide :key="0">
      <img class="brand" src="../assets/images/lg.png" alt="brand" />
    </slide>

    <slide :key="1">
      <img class="brand" src="../assets/images/amazon.png" alt="brand" />
    </slide>
    <slide :key="2">
      <img class="brand" src="../assets/images/rokutv.png" alt="brand" />
    </slide>

    <slide :key="3">
      <img class="brand" src="../assets/images/samsung.png" alt="brand" />
    </slide>

    <template #addons>
      <navigation />
      <pagination />
    </template>
  </carousel>
</template>

<script>
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";

export default {
  name: "App",
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },

  setup(props) {
    const settings = { autoplay: 2000, itemsToShow: 3, wrapAround: true };

    return { settings };
  },
};
</script>

<style>
.brand {
  width: 150px;
  height: 150px;
  object-fit: contain;
}

.carousel__prev,
.carousel__next {
  display: none;
}

.carousel__pagination-button {
  background-color: #8c063a !important;
}

.carousel__pagination-button--active {
  background-color: #de1e68 !important;
}

.sliderContainer{
  padding-top: 8px !important;
}

@media screen and (max-width: 550px) {
  .brand {
    width: 100px;
  }
}
</style>
