<script setup lang="ts">
const props = defineProps({
    itemData: Object,
    image:String,

});
</script>
<template>
    <div class="cardss">
        <div class="cards-image">
            <img :src="image" alt="Image" class="cards-img" width="109px" height="85px"/>
            <div class="card-d-icons heart-icons">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="cards-icons">
                <path stroke-linecap="round" stroke-linejoin="round" d="M21 8.25c0-2.485-2.099-4.5-4.688-4.5-1.935 0-3.597 1.126-4.312 2.733-.715-1.607-2.377-2.733-4.313-2.733C5.1 3.75 3 5.765 3 8.25c0 7.22 9 12 9 12s9-4.78 9-12Z" />
                </svg>
            </div>
        </div>
       <div class="cards-text">
            <NuxtLink :to="{name:'items-id', params:{id:itemData?.id}}"><h1 class="name-card">{{ itemData?.slug}}</h1></NuxtLink>
            <div class="card-title">
                <h1 class="card-description">{{itemData?.status}} 
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="cards-icons star-icons">
                         <path fill-rule="evenodd" d="M10.788 3.21c.448-1.077 1.976-1.077 2.424 0l2.082 5.006 5.404.434c1.164.093 1.636 1.545.749 2.305l-4.117 3.527 1.257 5.273c.271 1.136-.964 2.033-1.96 1.425L12 18.354 7.373 21.18c-.996.608-2.231-.29-1.96-1.425l1.257-5.273-4.117-3.527c-.887-.76-.415-2.212.749-2.305l5.404-.434 2.082-5.005Z" clip-rule="evenodd" />
                        </svg>
                        <h1 class="card-rank">
                            {{ itemData?.id }}
                        </h1>
                </h1>
                
            </div>
            <div class="card-price">
                <h1 class="name-card">{{ itemData?.updatedAt}}</h1>
                    <div class="card-d-icons">
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="cards-icons">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 3h1.386c.51 0 .955.343 1.087.835l.383 1.437M7.5 14.25a3 3 0 0 0-3 3h15.75m-12.75-3h11.218c1.121-2.3 2.1-4.684 2.924-7.138a60.114 60.114 0 0 0-16.536-1.84M7.5 14.25 5.106 5.272M6 20.25a.75.75 0 1 1-1.5 0 .75.75 0 0 1 1.5 0Zm12.75 0a.75.75 0 1 1-1.5 0 .75.75 0 0 1 1.5 0Z" />
                        </svg>

                    </div>
            </div>
            
       </div>
    </div>
        
           
    

     

</template>
<style scoped>
    template{
        color: white;
    }
    .name-card{
        font-weight: 600;
        font-size: 10px;
    }
    .card-rank{
        color:#3BA9EC ;
        font-weight: 600;
        font-size: 10px;
    }
    .cardss{
        box-sizing: border-box;
        display:flex;
        flex-direction: column;
        width: 180px;
        gap: 10PX;
        background-color: white;
        padding: 10px;
    }
    .cards-text{
        width: 100%;
    }
    .star-icons{
        color:#3BA9EC ;
        height: 8px!important;
    }
    .heart-icons{
        position: absolute;
        top: 0;
        right: 0;
    }
    
    .cards-image{
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        height: 90px;
        position: relative;
        object-fit: contain;
 
    }
   
    .card-description{
        display: flex;
        justify-content: space-between;
        align-items: center;
        font-weight: normal;
        font-size: 8px;
        color:#868686 ;
       
    }
    .card-d-icons{
        display: flex;
        justify-content: center;align-items: center;
        background-color: #3BA9EC;
        border-radius: 25px;
        width: 20px;
        height: 20px;
        color: white;

    }
    .card-i-icons{
        background-color:#3BA9EC;
    }
    .cards-icons{
        height: 7px;
        width: 9px;
        

    }
    .card-title{
        display: flex;
        justify-content: space-between;
    }
    .card-price{
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
</style>
