<template>
  <v-carousel class="mb-2" dark show-arrows-on-hover hide-delimiters>
    <v-carousel-item v-for="color in colors" :key="color">
      <v-sheet :color="color" height="100%" tile />
    </v-carousel-item>
  </v-carousel>
</template>

<script>
import { Vue, Component } from "vue-property-decorator";

@Component({})
export default class Carousel extends Vue {
  colors = ["primary", "secondary", "yellow darken-2", "red", "orange"];
}
</script>
