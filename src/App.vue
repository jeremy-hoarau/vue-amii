<script setup>
import { RouterView } from 'vue-router'
import HeaderAmii from "@/components/HeaderAmii.vue";
import FooterAmii from "@/components/FooterAmii.vue";
</script>

<template>
  <div id="page-wrapper">
    <HeaderAmii/>
    <RouterView />
    <FooterAmii/>
  </div>
</template>

<style scoped>
</style>
