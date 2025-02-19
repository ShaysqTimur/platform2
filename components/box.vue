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
    <div class="b-main">
        <div class="b-js-s">
            <div class="img-main" id="first">
                <div class="cont-img">
                    <img src="/img/monitor.png" alt="" class="conts-img">
                </div>
                <div class="cont-img">
                    <img src="/img/monitor.png" alt="" class="conts-img">
                </div>
                <div class="cont-img">
                    <img src="/img/monitor.png" alt="" class="conts-img">
                </div>
            </div>
           
            <div class="box-container">
                <containerTitle
                    slug="Монитор XTREON XT2453DE"
                    status="Электроника"
                    id="(228)"
                />
                <div class="icons">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="box-icons">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 3h1.386c.51 0 .955.343 1.087.835l.383 1.437M7.5 14.25a3 3 0 0 0-3 3h15.75m-12.75-3h11.218c1.121-2.3 2.1-4.684 2.924-7.138a60.114 60.114 0 0 0-16.536-1.84M7.5 14.25 5.106 5.272M6 20.25a.75.75 0 1 1-1.5 0 .75.75 0 0 1 1.5 0Zm12.75 0a.75.75 0 1 1-1.5 0 .75.75 0 0 1 1.5 0Z" />
                    </svg>
                </div>
            </div>
        </div>
        <div class="buts">
                <div class="but-click" @click="Slide"></div>
                <div class="but-click" @click="slideDown"></div>
        </div>
    </div>
   
</template>

<style scoped>
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
        height: 220px;
    }
    .img-main{
        position: relative;
        display: flex;
    }
    #first{
        transform: translateX(0px);
        transition: all 0.1s ease-in-out;
    }
    .box-container{
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .icons{
        display: flex;
        background-color: #3BA9EC;
        width: 32px;
        height: 32px;
        justify-content: center;
        align-items: center;
        border-radius: 25px;
    }

    .box-icons{
        width: 20px;
        height: 20px;
        color: white;
    }
    .cont-img{
        display: flex; 
        justify-content: center;
        width: 360px;
        min-width: 360px;
    }
    .conts-img{
        width: 280px;
        height: 220px;
    }
    .b-main{
        display: flex;
        flex-direction: column;
        width: 360px;
        background-color: white;
        position: relative;
        border-top: 1px solid #00000059 ;
        border-bottom: 1px solid #00000059 ;
        
    }
    .b-js-s{
        display: flex;
        justify-content: space-between;
        padding: 10px;
        flex-direction: column;
        overflow: hidden;
    }
    
    .b-but{
        width: 32px;
        height: 32px;
        border-radius: 25px;
        background-color: white;
        border: none;
        cursor: pointer;
        display: flex;
        justify-content: center;
    }
    .b-icon{
        color: #3BA9EC;
        width: 18px;
        height: 18px;
        text-align: center;
        display: flex;
        justify-content: center;
        align-items: center;
    }

</style>