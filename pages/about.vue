<template>
    <div class="flex flex-col"> 
        <div class="text-6xl font-bold underline">ABOUT</div>

        <section>
            <img src = "../assets/img/oit_logo.png" alt="OIT logo" width="200" v-on:mousemove="onImgMouseMove" >
            <p>ポインターの位置： <font color=blue>x={{ mousePointerX }};</font> <font color=red>y={{ mousePointerY }}</font></p>
        </section>
    </div>
</template>

<script setup lang="ts">
import {ref} from "vue";
const mousePointerX = ref(0);
const mousePointerY = ref(0);
const onImgMouseMove = (event: MouseEvent): void => {
    mousePointerX.value = event.offsetX;
    mousePointerY.value = event.offsetY;
};
</script>