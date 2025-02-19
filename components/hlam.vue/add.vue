<script setup>
import { ref } from 'vue';
defineProps({
    addName: {
        type: String,
        required: true
  }
 
})
const count = ref(0)
</script>

<template>
    <div class="add-button">
        <button  class="add-but" @click="count--">-</button>
        <p  class="add-text">{{ count }}</p>
        <button class="add-but" @click="count++" color="#3BA9EC">+</button>
    </div>
    
</template>

<style scoped>
    .add-button{
        display: flex;
    }
    .add-but:hover{
        border: 1px;
        color:#3BA9EC;
    }
    .add-but{
        width: 27px;
        height: 27px;
        border: 2px;
        cursor: pointer;
        color: black;
        background-color: white;
    }
    .add-text{
        text-align: center;
        background-color: white;
        font-weight: 600;
        
    }
</style>