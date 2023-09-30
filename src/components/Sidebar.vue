<template>
  <v-navigation-drawer v-model="drawer" color="#425C5A" class="rounded-e-xl">
    <v-sheet color="#3D5654" class="pa-4 rounded-te-xl text-center">
      <v-progress-circular
        model-value="80"
        color="#b49239"
        :size="100"
        :width="2"
      >
        <v-avatar size="85">
          <v-img
            cover
            src="https://images.pexels.com/photos/1130626/pexels-photo-1130626.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
          ></v-img>
        </v-avatar>
      </v-progress-circular>
      <div class="mt-4">Sant'Anna Lab</div>
      <span class="mb-6 text-caption">pedomanu27@gmail.com</span>
    </v-sheet>

    <v-list>
      <v-list-item
        v-for="(item, i) in links"
        :key="i"
        :value="item"
        active-class="border"
        :ripple="false"
      >
        <template v-slot:prepend>
          <v-icon :icon="item.icon" color="#B49239"></v-icon>
        </template>
        <v-list-item-title v-text="item.text"></v-list-item-title>
      </v-list-item>
    </v-list>

    <h5 class="ml-5 text-yellow-darken-2">ACTIVE USERS</h5>
    <v-row align="center" class="spacer ml-16 mt-4" no-gutters>
      <v-col cols="4" sm="2" md="1">
        <v-avatar size="36px">
          <v-img
            alt="Avatar"
            cover
            src="https://images.pexels.com/photos/1130626/pexels-photo-1130626.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
          ></v-img>
        </v-avatar>
      </v-col>
      <v-col cols="4" sm="2" md="1">
        <v-avatar size="36px">
          <v-img
            alt="Avatar"
            cover
            src="https://images.pexels.com/photos/769772/pexels-photo-769772.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
          ></v-img>
        </v-avatar>
      </v-col>
      <v-col cols="4" sm="2" md="1">
        <v-avatar size="36px">
          <v-img
            alt="Avatar"
            cover
            src="https://images.pexels.com/photos/7463159/pexels-photo-7463159.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
          ></v-img>
        </v-avatar>
      </v-col>
      <v-col cols="4" sm="2" md="1">
        <v-avatar size="36px">
          <v-img
            alt="Avatar"
            cover
            src="https://images.pexels.com/photos/13285972/pexels-photo-13285972.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
          ></v-img>
        </v-avatar>
      </v-col>

      <v-col cols="4" sm="2" md="1">
        <v-avatar size="36px" color="#B49239">+70</v-avatar>
      </v-col>
    </v-row>

    <div style="position: relative; z-index: 9999" class="mt-2">
      <v-img
        contain
        max-height="100"
        src="https://images.pexels.com/photos/2705756/pexels-photo-2705756.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
      ></v-img>
    </div>
  </v-navigation-drawer>
</template>

<script setup>
import { ref } from "vue";
const links = [
  { text: "DASHBOARD", icon: "mdi mdi-home-outline" },
  { text: "FLIGHTS", icon: "mdi mdi-airplane-off" },
  { text: "MALLET", icon: "mdi mdi-wallet-outline" },
  { text: "REPORTS", icon: "mdi mdi-file-chart-outline" },
  { text: "STATISTICS", icon: "mdi mdi-chart-pie" },
  { text: "SETTINGS", icon: "mdi mdi-cog-outline" },
];
const drawer = ref(true);
</script>

<script>
export default {
  data: () => ({
    cards: ["Today", "Yesterday"],
    drawer: null,
  }),
};
</script>

<style></style>
