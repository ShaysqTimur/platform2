<script setup>

defineProps({
  slug:String,
  image:String,
  
});
</script>

<template>
        <div class="scroll-menu">
            <img src="/img/mouse.png"  alt="Image" class="scroll-img"/>
            <p class="scroll-name">{{slug}}</p>
        </div>
</template>

<style scoped>
    .scroll-img{
        width: 100px;
        height: 88px;
        overflow: hidden;
        object-fit: contain;
    }
    .scroll-menu{
        display: flex;
        flex-direction: column;
        justify-content: center;
        width: 97px;
    }
    .scroll-name{
        font-weight: 600;
        font-size:10px;
        color: black;
        text-align: center;
        padding: 10px;
    }
</style>