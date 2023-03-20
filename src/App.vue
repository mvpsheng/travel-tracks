<script setup>

import ImageGallery from './components/ImageGallery.vue'
import ImageUploader from './components/ImageUploader.vue'
import axios from 'axios'
</script>
<script>
export default {
  data() {
    return {
      gallery: true,
      upload: false,
    }
  },
  components: {
    ImageGallery,
    ImageUploader
  },
  methods: {
    onChildEvent(data) {
      this.upload = data
      console.log('已经触发了上传事件');
      console.log(data);
      if (this.upload === true) {
        this.gallery = false
      }
    }
  }
}
</script>
<template>
<div v-if="gallery">
  <ImageGallery @doUpload="onChildEvent"></ImageGallery>
</div>
<div v-else>
  <ImageUploader></ImageUploader>
</div>
</template>

<style scoped>

</style>
