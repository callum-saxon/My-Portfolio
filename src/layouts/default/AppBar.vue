<template>
  <v-app-bar class="background" flat>
    <v-app-bar-title class="text">
        <v-btn rounded="xl" size="large" class="connect-button">
          <span class="connect-text">// Let's Connect</span>
          <span class="arrow">➜</span>
        </v-btn>
    </v-app-bar-title>
  </v-app-bar>
</template>

<script lang="ts" setup>
  //
</script>

<style>
.text {
  color: white;
}

.background {
  background: transparent !important;
  box-shadow: none !important;
  height: 70px;
}

.title-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}

.connect-button {
  display: flex;
  align-items: center;
  position: relative;
  cursor: pointer;
  font-size: 14px;
}

.connect-text {
  transition: transform 0.3s;
}

.connect-button:hover .arrow {
  transform: translateX(10px);
}

.connect-button:hover .connect-text {
  transform: translateX(0);
}

.arrow {
  margin-left: 5px;
  transition: transform 0.3s;
}


@media screen and (max-width: 600px) {
  .connect-button {
    font-size: 12px;
    padding: 8px 16px;
  }
}</style>