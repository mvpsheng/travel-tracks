<script setup>
import HomePageIcon from './components/HomePageIcon.vue'
import Search from './components/Search.vue'
import AddButton from './components/AddButton.vue'
import PhotoList from './components/PhotoList.vue'
import axios from 'axios'
</script>
<script>
  export default {
    data: () => ({
    imageurl: ''
  }),
  methods: {
    getrecipe() {
      
      const accessKey = '8mCad1eWgBRmEtXl8t1MRRSz3Z4tTlFD-xeqpSQZXis';
  const query = 'mountains';
  const url = `https://api.unsplash.com/search/photos?query=${query}&client_id=${accessKey}`;

  fetch(url)
  .then(response => response.json())
  .then(data => {
    this.imageurl = data.results[0].urls.full;
    console.log(data.results[0].urls.full);
    // Do something with the image data
  })
  .catch(error => console.error(error));
    }
  }
}
</script>
<template>
  <header>
      <HomePageIcon class="pageIcon" />
      <Search class="search"/>
      <AddButton class="addButton" />   
  </header>

  <main>
    <!-- bMeSc4hrHHdonbqH1GqDD1bxa9AKYPe8dehPguPB6OSsQo9QPcrurs6Y -->
    <PhotoList />
    
    <button @click="getrecipe"></button>
  </main>
</template>

<style scoped>
.imagefetch {
  width: 900px;
  height: 600px;
}
header {
  position: absolute;
  width: 680px;
  height: 55px;
  top: -280px;
  /* left: -300px; */
}

header .pageIcon {
  position: absolute;
  top: 10px;
  left: -600px;
}

header .search {
  position: absolute;
  
  left: -400px;
}

header .addButton {
  position: absolute;
  
  left: 450px;
}
</style>
