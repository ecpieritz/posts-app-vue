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

    const fecthPhotos = ()=> api.get("/photos?albumId=1")
    .then((response)=> photos.value = response.data)

    onMounted(fecthPhotos)

    return{photos}
  }
});
</script>

<style scoped>
.row{
  margin-top: 60px;
}
.col-lg-3.col-md-4.col-sm-6{
  margin-bottom: 30px;
}
  .card{
    max-width: 95%;
    height: 100%;
    background-color: var(--light-blue);
    border: none;
    border-radius: 8px;
  }
  
  .card img{
    border-top-left-radius: 8px;
    border-top-right-radius: 8px;
  }

  .card p{
    margin: 10px;
    color: var(--white);
    text-transform:capitalize;
    text-align: center;
  }
</style>