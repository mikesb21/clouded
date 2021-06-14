<template>
  <v-container id="home">
    <Carousel />
    <Deck />
  </v-container>
</template>

<script lang="ts">
// Vue
import { Vue, Component } from "vue-property-decorator";

// Components
import Carousel from "@/components/home/Carousel.vue";
import Deck from "@/components/home/Deck.vue";

@Component({ components: { Carousel, Deck } })
export default class Home extends Vue {}
</script>
