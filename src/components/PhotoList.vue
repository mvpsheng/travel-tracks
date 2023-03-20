<script setup>
import axios from 'axios'
</script>
<script>
export default {
    data() {
        return {
            images: []
        }
    },
    created() {
    this.loading = true
    axios.get('http://localhost:8080/api/upload')
      .then(response => {
        this.loading = false
        this.data = response.data
        
        this.images = this.data
        // console.log(this.images[0]);
      })
      .catch(error => {
        this.loading = false
        this.error = true
      })
  }
}
</script>
<template>

    <div v-for="image in images">
        <h3 :value="image.label"></h3>
        <img :src="image.url" alt="">
    </div>
</template>

<style>

</style>