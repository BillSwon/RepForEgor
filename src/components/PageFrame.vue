<template>
    <div class="page-frame">
        <slot></slot>
        <div class="page-frame__count">{{ countPage }}</div>
    </div>
</template>
<script setup>

import { defineProps, computed } from 'vue'

const props = defineProps({
    page: Number,
})

const countPage = computed(()=> props.page)

</script>
<style>
.page-frame {
    box-shadow: 0px 10px 12px rgb(23, 23, 23, 0.5);
    position: relative;

    background-color: #fff;
    padding: 20px 30px;
}

.page-frame__count {
    position: absolute;
    bottom: 30px;
    right: 30px;

    background-color: bisque;
    padding: 2px 6px;
}
</style>