<script>
export default {
    data: () => ({
    fileLabel:'',
    imageFile: '',
    return: {
        imageFile: ''
    }
  }),
  methods: {
    getImage() {
      console.log("开始发送,找图：");
    //   console.log(this.fileLabel);
  const url = `http://localhost:8080/api/upload/getImages`;

  fetch(url)
  .then(response => response.json())
  .then(data => {
    this.imageFile = data;
    console.log('收到图了');
    console.log(this.imageFile[0]);
    // Do something with the image data
  })
  .catch(error => console.error(error));
    }
  }
}
</script>
<template>
    <div class="searchPanel">
        <img src="./images/searchIcon.png" alt="" class="searchIcon">
        <input type="search" class="searchInput" v-model="this.fileLabel">
        <button class="searchSubmit" @click="getImage">找图</button>
    </div>
</template>

<style>
.searchPanel {
    box-sizing: border-box;

    position: fixed;
    width: 300px;
    height: 55px;
    /* left: -291px;
    top: -275px; */

    border: 1px solid #BDBDBD;
    filter: drop-shadow(0px 1px 6px rgba(0, 0, 0, 0.1));
    border-radius: 12px;
}
.searchIcon {

    position: absolute;
    width: 50px;
    height: 50px;
    left: 0px;
    top: px;
    border-radius: 50%;

    background: #373333;
}
.searchInput {
    position: absolute;
    width: 236px;
    height: 50px;
    left: 60px;
    top: 2.5px;
    /* opacity: 0; */
    border: 1px solid #BDBDBD;
    border-color:aliceblue;
    border-radius: 12px;
}
.searchSubmit {
  width: 55px;
  height: 55px;
  border-radius: 50%;
  opacity: 0;
}
</style>