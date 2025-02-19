<script setup>
    defineProps({
        slug:String,
        status:String,
});
</script>

<template>
    <div class="money-main">
        <div class="money">
            <p class="money-number">{{ slug }}<svg xmlns="http://www.w3.org/2000/svg" class="money-icons" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M4 7v10c0 2.21 3.582 4 8 4s8-1.79 8-4V7M4 7c0 2.21 3.582 4 8 4s8-1.79 8-4M4 7c0-2.21 3.582-4 8-4s8 1.79 8 4m0 5c0 2.21-3.582 4-8 4s-8-1.79-8-4" />
                </svg>
            </p>
        </div>
        <div class="quest">
          <button class="money-question">{{ status }}</button>
        </div>
    </div>
</template>

<style scoped>
    .quest{
      display: flex;
      justify-content: center;
    }
    .money-main{
      display: flex;
      flex-direction: column;
      justify-content: center;
      background-color: white;
      width: 360px;
    }
    .money{
      display: flex;
      justify-content: center;
    }
    .money-number{
      color: #3BA9EC;
      font-weight: 600;
      font-size: 32px;
    }
    .money-icons{
      color:#3BA9EC ;
      width: 24px;
      height: 24px;
    }

    .money-question{
      color: #517DA2;
      font-weight: 600;
      font-size: 12px;
      cursor: pointer;
      border: none;
    }
    .money-question:hover{
      color: #868686;
    }
</style>