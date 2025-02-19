<script setup>
defineProps({
   slug:String,
   updatedAt:String,
   userId:String,
})
</script>

<template>
    <div class="order-main">
        <div class="order-box">
            <p class="order-text">{{ slug }}</p>
            <h1 class="order-text2">{{ updatedAt }}</h1>
        </div>
        <button class="order-but">{{ userId }}</button>
    </div>
</template>

<style scoped>
    .order-boxP{
        display: flex;
    }
    .order-text2{
        font-weight:600 ;
        font-size: 10px;
        color: #868686;
    }
    .order-main{
        padding: 10px;
        display: flex;
        justify-content: space-between;
        background-color: white;
        width: 360px;
        align-items: center;
        
    }
    .order-text{
        font-weight: 600;
        font-size: 20px;
        color: black;
    }
    .order-but{
        font-weight: 600;
        font-size: 10px;
        border: 1px solid #47A938;
        color: #47A938;
        width: 64px;
        height: 14px;
    }
</style>