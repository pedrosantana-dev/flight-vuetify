<template>
  <v-app :style="{ background: $vuetify.theme.themes.light.colors.primary }">
    <Sidebar />
    <v-main>
      <v-container class="px-6 mt-n2" fluid>
        <v-row>
          <v-col cols="12">
            <v-card
              color="#B49239"
              theme="dark"
              class="rounded-xl"
              height="150"
            >
              <div class="d-flex flex-no-wrap justify-space-between">
                <div>
                  <v-card-title class="text-h5 mt-10">
                    Boieng 787
                  </v-card-title>
                  <v-card-subtitle>$548</v-card-subtitle>
                </div>
                <v-img src="av.png" class="mr-4 mt-5" absolute></v-img>
              </div>
            </v-card>
          </v-col>
          <v-col cols="12" sm="4" class="mt-n4">
            <v-card class="mx-auto" height="350px">
              <v-card-item title="Doughnut">
                <Doughnut />
              </v-card-item>
            </v-card>
          </v-col>

          <v-col cols="12" sm="8" class="mt-n4">
            <v-card class="mx-auto" height="350px">
              <v-card-item title="Bubble">
                <Bubble />
              </v-card-item>
            </v-card>
          </v-col>

          <v-col cols="12" sm="8" class="mt-n4">
            <v-card class="mx-auto">
              <v-card-item title="Last Trips">
                <template v-slot:subtitle>Overview of latest month</template>
              </v-card-item>
              <v-card-text class="py-0 mt-n4">
                <v-row align="center" no-gutters>
                  <v-col cols="12">
                    <v-list lines="two">
                      <v-list-item
                        v-for="folder in folders"
                        :key="folder.title"
                        :title="folder.title"
                        :subtitle="folder.subtitle"
                      >
                        <template v-slot:prepend>
                          <v-avatar>
                            <v-img :src="folder.img"></v-img>
                          </v-avatar>
                        </template>
                        <template v-slot: append>
                          <v-btn
                            size="large"
                            color="#B49239"
                            icon="mdi mdi-airplane-off"
                          ></v-btn>
                        </template>
                      </v-list-item>
                    </v-list>
                  </v-col>
                </v-row>
              </v-card-text>
            </v-card>
          </v-col>
          <v-col cols="12" sm="4" class="mt-n4">
            <v-card height="155px">
              <v-card-item title="Bar Chart">
                <Bar class="mt-n4" />
              </v-card-item>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Sidebar from "@/components/Sidebar.vue";
import Doughnut from "../components/Doughnut.vue";
import Bubble from "../components/Bubble.vue";
import Bar from "../components/Bar.vue";
export default {
  components: { Sidebar, Doughnut, Bubble, Bar },
  data: () => ({
    folders: [
      {
        subtitle: "Pedro Santana",
        title: "pedromanu27@gmail.com",
        img: "https://images.pexels.com/photos/1130626/pexels-photo-1130626.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1",
      },
    ],
  }),
};
</script>
