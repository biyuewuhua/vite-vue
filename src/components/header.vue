<template>
    <h3>header.vue-Middle组件</h3>

    <!-- 子组件 -->
     <Nav/>
</template>

<script setup>
    //导入子组件
    import Nav from "./nav.vue"

    import { inject } from "vue";

    const user = inject("provideUser");
    console.log("provideUser:",user);
</script>

<style scoped>

</style>