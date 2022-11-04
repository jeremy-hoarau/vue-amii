<script setup>
  import AmiiboCard from "@/components/AmiiboCard.vue";
  import axios from 'axios';
  import {onMounted, ref} from "vue";
  import HeaderAmii from "@/App.vue";
  import FooterAmii from "@/App.vue";
</script>

<template>
    <!-- Banner -->
    <section id="banner">
      <header>
        <h2>Hey.Bienvenue sur ma collection</h2>
      </header>
    </section>
    <!-- Intro -->
    <section id="intro" class="container">
      <div class="row">
        <AmiiboCard tail="023e0302"/>
        <AmiiboCard tail="034d0902"/>
        <AmiiboCard tail="00450502"/>
      </div>
      <footer>
        <ul class="actions">
          <li><RouterLink to="/list" class="button large">Liste complète</RouterLink></li>
        </ul>
      </footer>
    </section>
</template>
