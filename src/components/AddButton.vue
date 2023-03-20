<script>

</script>
<template>
    <div class="addButton">
        <div class="buttonName">Add a photo</div>
        <button class="buttonItem"></button>
    </div>
</template>

<style>
.addButton {
    
    position: fixed;
    width: 137px;
    height: 55px;
    /* left: 604.87px;
    top: -300px; */

    background: #3DB46D;
    box-shadow: 0px 1px 6px rgba(0, 0, 0, 0.1);
    border-radius: 12px;
}
.buttonName {
    position: absolute;
    width: 97px;
    height: 22px;
    left: 18px;
    top: 15px;

    font-family: 'Noto Sans';
    font-style: normal;
    font-weight: 700;
    font-size: 15px;
    line-height: 22px;
    /* identical to box height */


    /* color: #FFFFFF; */
}
.buttonItem {
    position: absolute;
    width: 137px;
    height: 55px;
    opacity: 0;

    font-family: 'Noto Sans';
    font-style: normal;
    font-weight: 700;
    font-size: 16px;
    line-height: 22px;
    /* identical to box height */

    border-radius: 12px;
    color: #FFFFFF;
}
</style>