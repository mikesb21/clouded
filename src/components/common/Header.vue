<template>
  <div>
    <v-system-bar color="primary darken-2" dark fixed app>
      <v-spacer></v-spacer>
      <v-icon>mdi-window-minimize</v-icon>
      <v-icon>mdi-window-maximize</v-icon>
      <router-link style="text-decoration: none; color: inherit" to="/">
        <v-icon>mdi-close</v-icon>
      </router-link>
    </v-system-bar>
    <v-app-bar color="primary lighten-1" padless fixed app>
      <v-row justify="center" no-gutters>
        <router-link
          v-for="link in links"
          :key="link.name"
          style="text-decoration: none; color: inherit"
          :to="link.path"
        >
          <v-btn color="white" text rounded class="my-2">{{ link.name }}</v-btn>
        </router-link>
      </v-row>
    </v-app-bar>
  </div>
</template>

<script lang="ts">
export default {
  data: () => ({
    links: [
      { name: "Home", path: "/" },
      { name: "About Us", path: "/about" },
    ],
  }),
};
</script>
