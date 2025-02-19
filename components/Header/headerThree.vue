<script setup>
    defineProps({
        slug:String,
        status:String,
        userId:String,
});
</script>

<template>
    <div class="main">
        <div class="header">
            <p class="header-text">{{ slug }}</p>
        </div>
        <div class="but-box">
            <div class="header-but">
                <button class="cart1">{{ status}}</button>
            </div>
            <div class="header-but">
                <button class="cart">{{ userId}}</button>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .but-box{
        display: flex;
    }
    .header-but{
        display: flex;
        justify-content: center;
    }
    .cart{
        text-align: center;
        border-radius:12px ;
        background-color: #3BA9EC;
        color: white;
        border: none;
        cursor: pointer;
        font-size: 10px;
        font-weight: 600;
    }
    .cart1{
        text-align: center;
        border-radius:12px ;
        color:#DE3A3A;
        cursor: pointer;
        font-size: 10px;
        font-weight: 600;
        border-color:  #DE3A3A ;
    }
    .main{
        display: flex;
        background-color: white;
        justify-content: space-between;
        width: 360px;
    }
    .header{
        display: flex;
       
    }
    .header-text{
        font-weight:600 ;
        font-size: 20px;
        color: black;
    }
    .Two-icons{
        width: 15px;
        height: 15px;
        color:#3BA9EC ;
    }

</style>