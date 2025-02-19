<script setup>
    defineProps({
      slug:String,
      status:String,
    })
</script>

<template>
        <div class="input-names">
            <label class="input-label" for="phone">{{ slug }}</label>
            <input type="text" id="phone" class="input-field">
            <div class="input-description">
                <p>{{ status }}</p>
            </div>
        </div>
</template>

<style scoped>
    .input-names{
        width: 330px;
        height: 62px;
        display: flex;
        flex-direction: column;
        padding: 10px;
        margin: 2px;
    }
    input{
        border: none;
    }
    .input-label {
            font-size: 12px;
            display: block;
            margin-bottom: 5px;
            font-weight: 600;
        }
    .input-description {
            margin-top: 5px;
            font-size: 10px;             
            font-weight: 600;
            color: #868686;
        }
</style>