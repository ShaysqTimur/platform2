<script setup>
defineProps({
 slug:String,
 status:String,
 isBlue:Boolean,
})
</script>

<template>
    <div class="info-main">
        <div class="info-cont">
            <h1 class="info-name">{{ slug }}</h1>
            <h1  v-if="isBlue" class="info-title" style="color: #3BA9EC;">{{ status }}</h1>
            <h1  v-else class="info-title" >{{ status }}</h1>
        </div>    
    </div>
</template>
<style scoped>
    .info-main{
        display: flex;
        width: 340px;
    }
    .info-cont{
        display: flex;
        justify-content: space-between;
        margin: 5px;
    }
    .info-name{
        width: 170px;
        color: #868686;
    }
    .info-title{
        width: 170px;
    }
    h1{
        font-weight: 400;
        font-size: 10px;
    }
</style>