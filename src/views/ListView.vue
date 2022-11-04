<script setup>
import axios from 'axios';
import {onMounted, ref} from "vue";
import {useRouter} from "vue-router";
const allAmiibo = ref([]);
onMounted(async () => {
  const res = await axios.get('https://www.amiiboapi.com/api/amiibo/');
  allAmiibo.value = res.data.amiibo;
});
const router = useRouter();
const onSeeAmiiboDetails = (tail) => {
  router.push({
    name: "details",
    params: {
      tail: tail
    }
  });
}
</script>

<template>
  <section id="main">
    <div class="container">

      <!-- Content -->
      <article class="box post">

        <header>
          <h2>Ma Collection</h2>
          <p>{{allAmiibo.length}}</p>
        </header>

        <table>
          <tr v-for="amiibo in allAmiibo" :key="amiibo.tail">
            <th>{{amiibo.character}}</th>
            <th>{{amiibo.gameSeries}}</th>
            <th><button @click="onSeeAmiiboDetails(amiibo.tail)">voir</button></th>
          </tr>
        </table>

      </article>

    </div>
  </section>
</template>
