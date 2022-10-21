<template>
  <section class="row">
    <div class="col-lg-3 col-md-4 col-sm-6" v-for="(photo, i) in photos" :key="i">
      <div class="card">
        <img :src='photo.url' alt="">
        <p>{{photo.title}}</p>
      </div>
    </div>
  </section>
</template>

<script>
import api from '@/services/api';
import { defineComponent, onMounted, ref } from 'vue';

export default defineComponent({
  name: 'post-cards',
  setup(){
    const photos = ref([])

    const fecthPhotos = ()=> api.get("/photos")
    .then((response)=> photos.value = response.data)

    onMounted(fecthPhotos)

    return{photos}
  }
});
</script>

<style scoped>

</style>