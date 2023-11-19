<template>
    <button @click="name_change()">
        {{num}}
    </button>
</template>

<script setup>
import { ref } from "vue";

var idx = -1;
var name_class = ref(['王部长', '曾总监', '庸庸学长', 'pkq学长', 'dk学长']);
var num = ref('点我看学长们');
function name_change()
{
    idx = (idx + 1) % 5;
    console.log(num.value);
    num.value = name_class.value[idx];
}
</script>

<style>
button
{
    width: 100px;
    height: 40px;
    background-color: bisque;
    border: 0;
    border-radius: 3px;
}
button:active
{
    background-color: azure;
}
</style>