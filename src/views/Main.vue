<template>
  <v-app>
    <Header />
    <Sidebar />
    <v-main style="background-color: #a8dfff">
      <v-container id="main_container" fluid>
        <router-view />
      </v-container>
    </v-main>
  </v-app>
</template>

<script lang="ts">
// Vue
import { Component, Vue } from "vue-property-decorator";

//Components
import Header from "@/components/common/Header.vue";
import Sidebar from "@/components/common/Sidebar.vue";

@Component({
  components: {
    Header,
    Sidebar,
  },
})
export default class Home extends Vue {}
</script>
