<script setup>
    const route = useRoute();
    console.log(route.params.id)
    //const { data } = await useFetch(`https://jsonplaceholder.org/posts/${route.params.id}`)
    const { data } = await useFetch(`https://jsonplaceholder.org/posts`)
</script>

<template>
    <div>
        <box/>
        <cardTabs
            slug="Подробнее"
            status="Характеристики"
            title="Отзывы"
            category="Xtreon XT2453DE - это высококачественный монитор, разработанный для удовлетворения потребностей как профессиональных пользователей, так и геймеров."
        />
        <headerTitle
                slug="Похожие товары"
                status="Посмотреть"
        />
        <div class="card-main">
            <div class="card-section">
                <div v-for="n in 2"><Card :itemData=data[n] /> </div>
            </div>
            <div class="card-section">
                <div v-for="n in 2"><Card :itemData=data[n] /> </div>
            </div>
            <div class="card-section">
                <div v-for="n in 2"><Card :itemData=data[n] /> </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
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