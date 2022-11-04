<script setup>
  import {useRoute} from "vue-router";
  const route = useRoute();
</script>

<template>
  <section id="header">
    <!-- Logo -->
    <h1><a href="index.html">AmiiVue</a></h1>

    <!-- Nav -->
    <nav id="nav">
      <ul>
        <li :class="route.name==='home'?'current':''"><RouterLink to="/">Home</RouterLink></li>
        <!-- <li><a href="left-sidebar.html">Pokémons</a></li> -->
        <li :class="route.name==='list'?'current':''"><RouterLink to="/list">Liste Amiibo</RouterLink></li>
      </ul>
    </nav>
  </section>
</template>

<style scoped>

</style>