<template>
  <v-container>
    <v-responsive class="align-center text-center">
      <v-card class="page">
        <v-card-text>
          <v-window v-model="tab">
            <v-window-item value="experience" class="experience">
              <Experience/>
            </v-window-item>

            <v-window-item value="about" class="about">
              <About/>
            </v-window-item>

            <v-window-item value="projects" class="projects">
              <Projects/>
            </v-window-item>
          </v-window>
        </v-card-text>
      </v-card>
      <v-row class="tabs-container">
        <v-col class="d-flex justify-center" style="position: absolute; bottom: 0; width: 100%;">
          <v-tabs v-model="tab" style="background: transparent;">
            <v-tab value="experience">// Experien ce.</v-tab>
            <v-tab value="about">// About.</v-tab>
            <v-tab value="projects">// Projects.
            </v-tab>
          </v-tabs>
        </v-col>
      </v-row>
    </v-responsive>
  </v-container>
</template>
  
<script lang="ts">
import About from "@/components/About.vue";
import Experience from "@/components/Experience.vue";
import Projects from "@/components/Projects.vue";

export default {
  data: () => ({
    tab: 'about',
  }),
  components: {
    About,
    Experience,
    Projects,
  },
}
</script>

<style scoped>
.page {
  background: transparent;
  height: 100%;
  box-shadow: none;
}

.experience,
.about,
.projects {
  background: transparent;
  box-shadow: none !important;
  height: 80vh;
  margin-bottom: 50px;
}

.tabs-container {
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
}

.content-wrapper {
  display: flex;
  align-items: center;
  margin-top: 25px;
}

.contact-details {
  text-align: center;
  margin-top: 25px;
}

.social-icons {
  margin-left: 5px;
}

.about-me-content {
  text-align: center;
  font-size: 18px;
}

.larger-font {
  font-size: 20px !important;
  margin-left: 10px;
  color: transparent;
}

.about-me {
  margin-top: 20px;
}

.work-showcase {
  margin-top: 20px;
}

.work-images {
  display: flex;
  justify-content: center;
  align-items: center;
}

.work-images img {
  max-width: 100%;
  height: auto;
  margin: 0 10px;
}
</style>