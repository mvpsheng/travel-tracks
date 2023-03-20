
<script>
import HomePageIcon from './HomePageIcon.vue'
import Search from './Search.vue'
import AddButton from './AddButton.vue'

import PhotoList from './PhotoList.vue';
export default {
  data() {
    return {
      upload: false,
    }
  },
  components: {
    PhotoList,
    HomePageIcon,
    Search,
    AddButton
  },
  methods: {
    onClick() {
      this.upload = true
      this.$emit('doUpload', this.upload)
    }
  }
}

</script>
<template>
    <div>
      <div class="header">
        <HomePageIcon class="icon"></HomePageIcon>
        <Search class="search"></Search>
        <AddButton class="addButton" @click="onClick"></AddButton>
      </div>
      <div class="gallery">
        <!-- Gallery content goes here -->
        <photo-list></photo-list>
      </div>
    </div>
  </template>
  
  <style>
  .header {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    height: 75px;
    background-color: #fff;
    padding: 10px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    z-index: 1;
  }
  .icon {
    left: 100px;
    top: 20px;
  }

  .search {
    left: 480px;
  }

  .addButton {
    left: 1260px;
  }
  .gallery {
    margin-top: 80px;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    grid-column: 1 / span 2;
    grid-gap: 15px;
  }

  @media screen and (max-width: 768px) {
  .grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media screen and (max-width: 480px) {
  .grid {
    grid-template-columns: 1fr;
  }
}
  </style>
  