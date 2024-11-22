<script setup>
    const emits = defineEmits(["getWeb"]);
    emits("getWeb", { name: "邓瑞", url: "www.dengruicode.com" });

    const add = ()=>{
        emits("userAdd",10);
    }
</script>

<template>
    <h3>Header</h3>

    <button @click="add">添加用户</button>
</template>

<style scoped></style>
