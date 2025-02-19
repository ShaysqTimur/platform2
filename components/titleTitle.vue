<script setup>
defineProps({
  slug:String,
  status:String,

})
</script>

<template>
    <div class="title">
        <p class="title-name">{{ slug }}</p>
        <h1 class="title-title"> {{ status }}</h1>
    </div>
</template>

<style scoped>
    .title{
        width: 73px;
        height: 28px;
        background-color: white;
        display: flex;
        flex-direction: column;
       
    }
    .title-name{
        font-weight: 600;
        font-size: 10px;
    }
    .title-title{
        font-weight: 400;
        font-size: 8px;
        color: #868686;
    }
</style>