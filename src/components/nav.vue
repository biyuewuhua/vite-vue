<template>
    <h3>nav-vue-Bottom组件</h3>
    <button @click="userAdd">添加用户</button>
</template>

<script setup>
import { inject } from "vue";

    const web = inject("provideWeb");
    console.log("provideWeb:",web);

    const userAdd = inject("provideFuncUserAdd");
    console.log(userAdd);
</script>

<style scoped>

</style>