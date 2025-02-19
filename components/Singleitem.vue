<script setup lang="ts">
const props = defineProps({
    itemData: Object,
});

</script>

<template>
    <div class="item">
        <p>Предмет номер {{ itemData?.id }}</p>
        <NuxtLink :to="{name:'items-id', params:{id:itemData?.id}}"><h1>{{ itemData?.title }}</h1></NuxtLink>
        <p>{{ itemData?.title }}</p>
    </div>
</template>

<style scoped>
.item{
    border: 1px solid red;
    width: 300px;
    height: 400px;
}
</style>