<template>
    <h3>App.vue-Top组件</h3>

    user: {{ user }}

    <!-- 子组件 -->
    <Header />
</template>

<script setup>
    import { ref, provide } from "vue";

    //导入子组件
    import Header from "./components/header.vue";

    const web = {
        name: "邓瑞",
        url: "www.dengruicode.com",
    };

    provide("provideWeb", web);

    const user = ref(0);
    provide("provideUser", user);

    const userAdd = () =>{
        user.value++;
    }
    provide("provideFuncUserAdd",userAdd);
</script>

<style scoped></style>
