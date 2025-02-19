<script setup>


</script>

<template>
    <div>
        <money
            slug="1,23"
            status="Как получить бонусы?"
        />
        <div class="input-main">
            <headerTitle
                slug = "Данные аккаунта" 
                status = "Посмотреть"
            />
            <inputs
                slug = "Введите номер телефона"
                status = "Номер телефона"
            />
            <inputs
                slug = "Введите ФИО"
                status = "Имя пользователя"
            />
            <inputs
                slug = "Введите адрес доставки"
                status = "Адрес доставки"
            />
        </div>
        <headerTitle
                slug = "История Заказов" 
        />
        <historyTitle
                slug = "Заказ#123567890"
                status = "12 сентября 2024 год"
                category = "Детали заказа"
        />
    </div>


</template>

<style scoped>
.input-main{
        background: white;
        display: flex;
        width: 360px;
        height: 248px ;
        flex-direction: column ;
}
</style>