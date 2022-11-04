<script setup>
const props = defineProps({
  tail: String
})
import axios from 'axios';
import {onMounted, ref} from "vue";
const amiibo = ref([]);
onMounted(async () => {
  const res = await axios.get('https://www.amiiboapi.com/api/amiibo?tail='+props.tail);
  amiibo.value = res.data.amiibo[0];
});
</script>

<template>
  <div class="col-4 col-12-medium">
    <section class="middle">
      <img :src="amiibo.image" />
      <header>
        <h2>{{ amiibo.character }}</h2>
      </header>
      <p>{{ amiibo.gameSeries }}</p>
    </section>
  </div>
</template>

<style scoped>

</style>