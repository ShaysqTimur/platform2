<script setup>
defineProps({
    status:String,
    slug:String,

});
</script>

<template>
  <div class="header-main">
    <div class="header-names">
      <p class="header-text">{{slug}}</p>
    </div>
    <div class="header-titles">
      <button class="but-title">
        {{ status }}
      </button>
    </div>
  </div>
</template>

<style scoped>
.header-main {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 30px;
  background-color: white;
  width: 360px;
  overflow: hidden;
}
.header-names{
  padding: 10px;
}
.header-text {
  font-weight: 600;
  font-size: 20px;
  text-align: center;

}
.but-title {
  font-weight: 600;
  font-size: 10px;
  color: #3ba9ec;
  cursor: pointer;
  border: none;
  background-color: white;
}
</style>
