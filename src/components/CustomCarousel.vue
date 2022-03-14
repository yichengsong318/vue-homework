<template>
  <q-carousel
    animated
    v-model="slide"
    arrows
    swipeable
    control-color="white"
    infinite
    prev-icon="arrow_back"
    next-icon="arrow_forward"
    class="cloth-carousel rounded-borders"
  >
    <q-carousel-slide
      v-for="(image, idx) in imageData"
      :key="idx"
      :name="idx + 1"
      :img-src="image"
    />
  </q-carousel>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "CustomCarousel",
  data() {
    return {
      imageData: [
        "https://cdn.quasar.dev/img/mountains.jpg",
        "https://cdn.quasar.dev/img/parallax1.jpg",
        "https://cdn.quasar.dev/img/parallax2.jpg",
        "https://cdn.quasar.dev/img/quasar.jpg",
      ],
    };
  },
  setup() {
    return {
      slide: ref(1),
    };
  },
});
</script>

<style lang="scss">
.cloth-carousel {
  max-width: 356px;
  max-height: 356px;
  min-width: 327px;
}

@media (max-width: $breakpoint-xs-max) {
  .cloth-carousel {
    height: 327px;
  }
}
</style>
