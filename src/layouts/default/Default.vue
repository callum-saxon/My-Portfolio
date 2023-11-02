<template>
  <v-app>
    <default-bar />

    <default-view class="html"/>
  </v-app>
</template>

<script lang="ts" setup>
  import DefaultBar from './AppBar.vue'
  import DefaultView from './View.vue'
</script>

<style>
.html {
  --s: 40px;
  --c1: #121212;
  --c2: #989898;

  --l: repeating-linear-gradient(
    var(--c1) 0,
    var(--c1) 1px,
    transparent 0,
    transparent calc(var(--s) - 1px)
  );

  background:
    radial-gradient(var(--c1) 95%, var(--c2) 99%) 0 0/var(--s) var(--s);
}
</style>