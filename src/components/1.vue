<script setup>
import { ref } from 'vue';
const zhang = ref(['张恺哲', '张哲恺', '哲张恺', '恺张哲', '恺哲张', '哲恺张']);
const shabi = () => {
    alert(`${zhang.value[k.value]}是傻逼`);
};
const k = ref(0);
const changename = () => {
    k.value = (k.value + 1) % zhang.value.length;
};
</script>

<template>
    <div>
        <h1>hello world</h1>
        <span class="ss">{{ zhang[k] }}</span>
        <br>
        <button @click="shabi">shabi</button>
        <button @click="changename">修改变量</button>
    </div>
</template>

<style>
    div{
        background-color: pink;
        margin: 20px;
        align-items: center;
    }
    .ss{
        color: rgb(76, 0, 255);
        font-size: 30px;
        margin: 50px;
    }
    button{
        align-self: center;
        color: orange;
        font-family: 'Times New Roman', Times, serif;
        font-size: 30px;
        width: 150px;
        height: 90px;
        margin: 30px;
        background-color: green;
        border-radius: 15px;
        border-color: aqua;
        border-width: 3px;
    }
    button:hover{
        background-color: yellow;
        color: blue;
    }
</style>