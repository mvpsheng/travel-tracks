<script setup>
import HomePageIcon from './components/HomePageIcon.vue'
import Search from './components/Search.vue'
import AddButton from './components/AddButton.vue'
import PhotoList from './components/PhotoList.vue'
</script>

<template>
  <header>
      <HomePageIcon class="pageIcon" />
      <Search class="search"/>
      <AddButton class="addButton" />   
  </header>

  <main>
    <PhotoList />
  </main>
</template>

<style scoped>
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
