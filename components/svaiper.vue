<script setup>
 let m = 0 ;
    function Slide (){
        m +=360;
        const first = document.getElementById("first");
        first.style.transform = `translateX(-${m}px)`;
        console.log(m);
    }
    function slideDown(){
        m-=360
        const first = document.getElementById("first");
        first.style.transform = `translateX(-${m}px)`;
    }
</script>

<template>
    <div class="main-img">
        <div class="slides" id="first">
            <div class="slide">
                <img src="/img/slaider.png" alt="Image" class="img" width="360px" height="130px"/>
            </div>
           <div class="slide">
            <img src="/img/slaider2.png" alt="Image" class="img" width="360px" height="130px"/>
           </div>
        </div>
        <div class="buts">
            <div class="but-click" @click="Slide"></div>
            <div class="but-click" @click="slideDown"></div>
        </div>
    </div>

    
</template>

<style scoped>
    #first{
        transform: translateX(0px);
        transition: all 0.1s ease-in-out;
    }
    .buts{
        display: flex;
        justify-content: space-between;
        width: 360px;
        align-items: center;
        position: absolute;
        top: -1px;

    }
    .but-click{
        cursor: pointer;
        padding: 10px;
        border: none;
        width: 60px;
        height: 130px;
    }
    .main-img{
        position: relative;
        display: flex;
        width: 360px;
        overflow: hidden;

    }
    .slides{
        display: flex;
        position: relative;
    }
    .Image{
        padding: 10px;
    }

</style>