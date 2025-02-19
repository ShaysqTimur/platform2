<script setup lang = "ts">
    defineProps({
        slug:String,
        category:String,
        status:String,
        title:String,
    
})

    function Toggle(itemId){
        document.getElementById(itemId).classList.add('invisible');
        console.log("giiggg");
    }
    function toggleDelete(itemId){
         document.getElementById(itemId).classList.remove('invisible');
    }   
   
</script>

<template>
    <div class="tab-main">
        <div class="tab-header">
            <button class="tab-but" @click="Toggle('content2'),Toggle('content3'),toggleDelete('content1')">
                {{ slug }}
            </button>
            <button class="tab-but" @click="Toggle('content1'),Toggle('content3'),toggleDelete('content2')" >
                {{ status}}
            </button>
            <button class="tab-but" @click="Toggle('content1'),Toggle('content2'),toggleDelete('content3')">
                {{ title }}
            </button>
        </div>
        <div id="content1"   class="tab-text">{{category}}</div>
        <div id="content2" class="tab-text  tab-column invisible"> 
            <infoGeo
                slug = "Частота кадров:"
                 status = "144гц"
            />
            <infoGeo
                slug = "Пиксели:"
                status = "1920х1080"
            />
            <infoGeo
                slug = "Какая-то залупа:"
                status = "Точно такая-же залупа"
            />
        </div>
        <div id="content3" class=" tab-text tab-com invisible">
            <comm
                slug="Данил"
                status ="08.08.2008"
                title="Xtreon XT2453DE - это высококачественный монитор, разработанный для удовлетворения потребностей как профессиональных пользователей, так и геймеров."
            />
        </div>
    </div>

</template>

<style scoped>
    .tab-text{
        font-size: 10px !important;
        padding: 10px;
    }
    .tab-com{
        display: flex;
        flex-direction: column;
    }
    .tab-column{
        display: flex;
        flex-direction: column;
    }
    .invisible{
        display: none !important;
    }
    .tab-main{
        display: flex;
        flex-direction: column;
        width: 360px;
        background-color: white;
        padding-bottom: 10px;
        border-bottom: 1px solid #00000059 ;
    }
    .tab-header{
        display: flex;
        justify-content: space-evenly;
        width: 340px;
        height: 26px;
    }
    .tab-but.active {
        color: #3BA9EC;
        border-bottom: 2px solid #3BA9EC;
    }
    .tab-but{
        color:#868686 ;
        font-weight: 600;
        font-size: 12px;
        cursor: pointer;
        border: none;
    }
    .tab-but:hover{
        color: #3BA9EC;
        border-color:#3BA9EC ;
        border-bottom: 1px;
    }
</style>