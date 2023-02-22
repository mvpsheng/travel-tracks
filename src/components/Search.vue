<script>

</script>
<template>
    <div class="searchPanel">
        <img src="./images/searchIcon.png" alt="" class="searchIcon">
        <input type="search" class="searchInput">
    </div>
</template>

<style>
.searchPanel {
    box-sizing: border-box;

    position: absolute;
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
</style>