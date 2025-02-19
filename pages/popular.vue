<script setup>
    const route = useRoute();
    const { data } = await useFetch(`https://jsonplaceholder.org/posts`)
</script>

<template>
    <div class="popular-main">
        <headerTitle
            slug="Популярное"
        />
        <div class="popular-list">
            <div class="card-main">
                <div class="card-section">
                    <div v-for="n in 2"><Card :itemData=data[n] image="/img/monitor.png"/></div>
                </div>
                <div class="card-section">
                    <div v-for="n in 2"><Card :itemData=data[n] image="/img/Iphone13promax.png"/></div>
                </div>
                 <div class="card-section">
                    <div v-for="n in 2"><Card :itemData=data[n] image="/img/monitor.png"/></div>
                </div>
                <div class="card-section">
                    <div v-for="n in 2"><Card :itemData=data[n] image="/img/monitor.png"/></div>
                </div>
            </div>
        </div>
    </div>


</template>

<style scoped>  
    .popular-main{
        width: 360px;
        background-color: white;
    }
    .card-section{
      display: flex;
      border-bottom: 1px solid #00000059 ;
      
    }
    .card-main{
      display: flex;
      justify-content: space-between;
      flex-direction: column;
      border-bottom: 1px solid #00000059 ;
      width: 360px;
      
    }

</style>