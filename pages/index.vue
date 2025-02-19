<script setup>
    const route = useRoute();
    const { data } = await useFetch(`https://jsonplaceholder.org/posts`)
</script>


<template>
    <div class="template-home">
        <svaiper/>
        <div class="main-scroll">
            <headerTitle
                slug="Категории"
                status="Посмотреть"
            />
            <div class="menu-scroll">
                <HeaderPaging
                    v-for="item in data" :key="item.id" :pagingData="item"
                    slug="Электроника"
                />

            </div>
        </div>
        <headerTitle   
                   slug="Категории"
                   status="Посмотреть"
        />
        <div class="card-main">
            <div class="card-section">
                <div v-for="n in 2"><Card :itemData=data[n] image="/img/monitor.png"/></div>
            </div>
            <div class="card-section">
                <div v-for="n in 2"><Card :itemData=data[n] image="/img/Iphone13promax.png"/></div>
            </div>
            <div class="card-section">
                <div v-for="n in 2"><Card :itemData=data[n] image="/img/Iphone13promax.png"/></div>
            </div>
        </div>
    </div>
</template>

<style scoped>
  
    .main-scroll{
      border-bottom: 1px solid #00000059 ;
      padding-bottom:5px ;
      width: 360px;
    }
    .menu-scroll{
      display: flex;
      overflow: scroll;
      background-color: white;
      width: 360px;
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