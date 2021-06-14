<template>
  <v-container>
    <v-row dense>
      <v-col v-for="color in colors" :key="color" :cols="columns">
        <v-card :color="color" dark elevation="12">
          <v-card-title class="text-h5"> Card Title </v-card-title>
          <v-card-subtitle> Blah Blah Blah... </v-card-subtitle>
          <v-card-actions>
            <v-btn text> Click Me </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import { Vue, Component } from "vue-property-decorator";

@Component({})
export default class Deck extends Vue {
  colors = [
    "primary",
    "secondary",
    "yellow darken-2",
    "red",
    "orange",
    "success",
  ];
  cols = [3, 4, 6];

  get columns() {
    return this.cols[Math.floor(Math.random() * this.cols.length)];
  }
}
</script>
