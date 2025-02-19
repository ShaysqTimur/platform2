<script setup lang="ts">
const props = defineProps({
    itemData: Object,
});

</script>

<template>
    <div class="item">
        <h1>Предмет номер {{ itemData?.id }}</h1>
        <NuxtLink :to="{name:'items-id', params:{id:itemData?.id}}"><h1>{{ itemData?.title }}</h1></NuxtLink>
        <h1>{{ itemData?.title }}</h1>
    </div>
</template>

<style scoped>
.item{
    border: 1px solid red;
    width: 300px;
    height: 400px;
}
</style>