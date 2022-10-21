<template>
  <section class="row">
    
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