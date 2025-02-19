<script setup >
    const route = useRoute();
    const { data } = await useFetch(`https://jsonplaceholder.org/posts`)

</script>

<template>
    <div class="category-main">
        <headerTitle
            slug="Посмотреть"
        />
        <div class="category-list">
            <div class="category-column" v-for="n in 3 "><HeaderPaging slug="Электроника" image="/img/kovrik.png"/> </div>
        </div>
        <div class="category-list">
            <div class="category-column" v-for="n in 3 "><HeaderPaging slug="Аксессуары" image="/img/naushnikipng.png"/> </div>
        </div>
        <div class="category-list">
            <div class="category-column" v-for="n in 3 "><HeaderPaging  slug="Электроника" image="/img/mouse.png"/> </div>
        </div>
    </div>


</template>

<style scoped>
    .category-column{
        display: flex;
        flex-direction: column;
    }
    .category-main{
        width: 360px;
        gap: 10px;
        background-color: white;
    }
    .category-list{
        display: flex;
        justify-content: space-between;
        align-items: center;
        background-color: white;
        width: 340px;
    }
</style>