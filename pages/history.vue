<script setup>


</script>

<template>
    <div class="main-his">
       <orderTitle  
            slug="Заказ #1234567890"
            updatedAt ="12 сентября 2024 год"
            userId="Доставлен"
       />
        <div class="info">
            <headerTitle
                slug = "Самовывоз" 
            />
            <infoGeo 
                slug = "Время работы склада:"
                status = "9:00 - 19:00"
            />
            <infoGeo 
                slug = "Время прибытие товара:"
                status = "21 сетября, 13:12"
            />
            <infoGeo 
                slug = "Адрес склада:"
                status  = "Ул.Пушкина 24/2" 
                isBlue = "true"
            />
        </div>
        <div class="info">
            <headerTitle
                 slug = "Оплата" 
             />
            <infoGeo
                slug = "Вид оплаты:"
                status = "При получении"
            />
            <infoGeo
                slug = "Товары:"
                status = "49 000₸"
            />
            <infoGeo
                slug = "Доставка:"
                status= "Бесплатно"
            />
            <infoGeo
                slug = "Итого:"
                status = "49 000₸"
            />
        </div>
        <headerTwo
            two-name="Товары"
            two-title="Выбрать все"
         />
         <div class="box">
            <div class="box-cont1">
                <div class="checbox">
                    <checkbox/>
                </div>
                <container
                    slug="Монитор XTREON XT2453DE"
                    status="Электроника"
                    id="(228)"
                    image="/img/monitor.png"
                />
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="icons-box">
                <path stroke-linecap="round" stroke-linejoin="round" d="m14.74 9-.346 9m-4.788 0L9.26 9m9.968-3.21c.342.052.682.107 1.022.166m-1.022-.165L18.16 19.673a2.25 2.25 0 0 1-2.244 2.077H8.084a2.25 2.25 0 0 1-2.244-2.077L4.772 5.79m14.456 0a48.108 48.108 0 0 0-3.478-.397m-12 .562c.34-.059.68-.114 1.022-.165m0 0a48.11 48.11 0 0 1 3.478-.397m7.5 0v-.916c0-1.18-.91-2.164-2.09-2.201a51.964 51.964 0 0 0-3.32 0c-1.18.037-2.09 1.022-2.09 2.201v.916m7.5 0a48.667 48.667 0 0 0-7.5 0" />
                </svg>

            </div>
            <div class="box-cont2">
                <titleTitle
                    slug="50 999₸"
                    status="С 999шт * 999₸/шт"
                />
                <add
                    count="1 шт"
                />
            </div>
        </div>
    </div>
</template>

<style scoped>
    .main-his{
        width: 360px;
        background-color: white;
    }
    .checbox{
      display: flex;
      justify-content: center;
      align-items: center
    }
     .info{
      
      display: flex;
      flex-direction: column;
      width: 340px;
      background: white;
    }
    .icons-box{
      width: 20px;
      height: 20px;
      color:#B7B7B7 ;
      border: 1.5px;
    }
    .box-cont2{
      padding: 5px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      width: 340px;
    } 
    .box-cont1{
      width: 340px;
      padding: 5px;
      display: flex;
      justify-content: space-between;
  
    }
    .box{
      width: 360px;
      height: 168px;
      background-color: white;
      display:flex;
      align-items: center;
      flex-direction: column;
    }
</style>