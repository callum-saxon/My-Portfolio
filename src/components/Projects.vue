<template>
    <v-container class="text-details text">
      <v-row>
        <v-col cols="4">
          <h1>// Projects.</h1>
          <v-expand-transition>
            <div
              v-if="isHovering"
              class="d-flex transition-fast-in-fast-out bg-orange-darken-2 v-card--reveal text-h2"
              style="height: 100%;"
            >
              Lorem ipsum
            </div>
          </v-expand-transition>
        </v-col>
        <v-col cols="8" style="overflow-y: scroll">
          <v-row class="row">
            <v-col v-for="project in projects" :key="project.id" cols="12" sm="10" md="9" lg="6">
              <v-sheet class="pa-0 ma-0" style="background: transparent;">
                <v-hover v-slot="{ isHovering, props }">
                  <v-card class="mx-auto" color="grey-lighten-4" v-bind="props">
                    <v-img :aspect-ratio="4/3" :src="project.logo">
                      <v-expand-transition>
                        <div
                          v-if="isHovering"
                          class="d-flex transition-fast-in-fast-out bg-orange-darken-2 v-card--reveal text-h2"
                            style="height: 100%;"
                        >
                          {{ project.name }}
                        </div>
                      </v-expand-transition>
                    </v-img>
                  </v-card>
                </v-hover>
              </v-sheet>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
</template>

<style>
.row {
  overflow-y: scroll;
}

.row::-webkit-scrollbar {
  width: 0;
}
</style>

<script setup>
const projects = [
  {id: 1, name: "BioCortex", logo: "@/assets/CLSoftware_Logo.png"},
  {id: 2, name: "CLSoft", logo: "@/assets/CLSoftware_Logo.png"},
  {id: 3, name: "Uplift.ai", logo: "@/assets/CLSoftware_Logo.png"},
  {id: 4, name: "ClimaTrack", logo: "@/assets/CLSoftware_Logo.png"},
  {id: 5, name: "BioCortex", logo: "@/assets/CLSoftware_Logo.png"},
  {id: 6, name: "CLSoft", logo: "@/assets/CLSoftware_Logo.png"},
  {id: 7, name: "Uplift.ai", logo: "@/assets/CLSoftware_Logo.png"},
  {id: 8, name: "ClimaTrack", logo: "@/assets/CLSoftware_Logo.png"},
];
</script>
