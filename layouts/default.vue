<script setup lang="ts">
import { NuxtLink } from '#components';

definePageMeta({
  layout: 'default'
})
</script>


<template class="width-main">
<div class="template">
<slot/>

 <div class="main">
    <div class="conts">
      <NuxtLink class="conts-svg" to="/cart"><svg xmlns="http://www.w3.org/2000/svg" class="icon-main" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
        <path stroke-linecap="round" stroke-linejoin="round" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z" />
        </svg>
      </NuxtLink>
      <p class="text-cont">Корзина</p>
    </div>

    <div class="conts">
      <NuxtLink class="conts-svg" to="">
        <svg xmlns="http://www.w3.org/2000/svg" class="icon-main" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
        <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
        </svg>
      </NuxtLink>
      <p class="text-cont">Поиск</p>
    </div>
    <div class="conts">
        <NuxtLink class="conts-svg" to="#"><svg xmlns="http://www.w3.org/2000/svg" class="icon-main" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
        <path stroke-linecap="round" stroke-linejoin="round" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
        </svg></NuxtLink>
      <p class="text-cont">Профиль</p>
    </div>
    <div class="conts">
      <NuxtLink class="conts-svg" to="/settings">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="icon-main">
        <path stroke-linecap="round" stroke-linejoin="round" d="M10.343 3.94c.09-.542.56-.94 1.11-.94h1.093c.55 0 1.02.398 1.11.94l.149.894c.07.424.384.764.78.93.398.164.855.142 1.205-.108l.737-.527a1.125 1.125 0 0 1 1.45.12l.773.774c.39.389.44 1.002.12 1.45l-.527.737c-.25.35-.272.806-.107 1.204.165.397.505.71.93.78l.893.15c.543.09.94.559.94 1.109v1.094c0 .55-.397 1.02-.94 1.11l-.894.149c-.424.07-.764.383-.929.78-.165.398-.143.854.107 1.204l.527.738c.32.447.269 1.06-.12 1.45l-.774.773a1.125 1.125 0 0 1-1.449.12l-.738-.527c-.35-.25-.806-.272-1.203-.107-.398.165-.71.505-.781.929l-.149.894c-.09.542-.56.94-1.11.94h-1.094c-.55 0-1.019-.398-1.11-.94l-.148-.894c-.071-.424-.384-.764-.781-.93-.398-.164-.854-.142-1.204.108l-.738.527c-.447.32-1.06.269-1.45-.12l-.773-.774a1.125 1.125 0 0 1-.12-1.45l.527-.737c.25-.35.272-.806.108-1.204-.165-.397-.506-.71-.93-.78l-.894-.15c-.542-.09-.94-.56-.94-1.109v-1.094c0-.55.398-1.02.94-1.11l.894-.149c.424-.07.765-.383.93-.78.165-.398.143-.854-.108-1.204l-.526-.738a1.125 1.125 0 0 1 .12-1.45l.773-.773a1.125 1.125 0 0 1 1.45-.12l.737.527c.35.25.807.272 1.204.107.397-.165.71-.505.78-.929l.15-.894Z" />
        <path stroke-linecap="round" stroke-linejoin="round" d="M15 12a3 3 0 1 1-6 0 3 3 0 0 1 6 0Z" />
        </svg>
      </NuxtLink>
      <p class="text-cont">Настройки</p>
    </div>
  </div>
</div>
</template>

<style scoped>

.width-main{
    width: 100%;
    padding-bottom: 120px;
    background-color: white;
    
  }
  .main{
    display: flex;
    width: 360px;
    gap: 10px;
    background-color: #fff;
    position: fixed;
    bottom:0 ;
  
  }
  .conts-svg{
    width: 32px;
    height: 32px;
    border-radius: 25px;
    display: flex;
    justify-content: center;
    align-items: center;
    border: none;
    cursor: pointer;


  }
  .icon-main{
       color:#3BA9EC ;
       width: 18px;
       height: 18px;
  }
  .text-cont{
    font-weight: 400;
    color:#3BA9EC;
    font-size: 8px;
    text-align: center;
  }
  .conts{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width:77px;
    background-color: white;
    height: 35px;
  }
</style>