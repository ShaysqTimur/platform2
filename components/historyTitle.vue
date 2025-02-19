<script setup>
    defineProps({
        slug:String,
        status:String,
        category:String,
})
</script>

<template>
    <div class="set-main">
        <div class="set-box">
            <p class="set-title">{{ slug }}</p>
            <h1 class="set-name">{{ status }}</h1>
        </div>
        <button class="set-but">{{ category }}</button>
    </div>
</template>

<style scoped>
    .set-but{
        font-weight: 600;
        font-size: 12px;
        color: #3BA9EC;
        border: none;
    }
    .set-main{
        padding: 10px;
        display: flex;
        width: 360px;
        background-color: white;
        justify-content: space-between;
    }
    .set-title{
        font-weight:  600;
        font-size: 12px;
        color: black;
    }
    .set-name{
        font-weight: 600;
        font-size:10px;
        color: #868686;
    }
</style>