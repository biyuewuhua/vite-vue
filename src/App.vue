<script setup>
    import { reactive } from "vue";
    import Header from "./components/header.vue";
    import Footer from "./components/footer.vue";

    const propsWeb = reactive({
        user: 10,
        url: "www.dengruicode.com"
    });

    const userAdd = () => {
        propsWeb.user++;
        console.log(propsWeb.user);
    };
</script>

<template>
    <Header
        propsName="邓瑞编程"
        propsUrl="dengruicode.com"
    />

    dengruicode.com

    <button @click="userAdd">添加用户</button>

    <!-- <Footer v-bind="propsWeb"/> -->
    <Footer :="propsWeb" />
</template>

<style scoped></style>
