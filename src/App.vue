<template>
    <h3>App.vue</h3>

    <Header>
        <a href="dengruicode.com">邓瑞编程</a>
    </Header>

    <Footer>
        <!-- template,v-slot:url -->
        <!-- <template v-slot:url> -->
        <!-- <template #url="data">
            {{ data.title }}
            {{ data.user }} -->
        <template #url="{title, user}">
            {{ title }}
            {{ user }}
            <a href="www.dengruicode.com">网址</a>
        </template>
    </Footer>
</template>

<script setup>
    //导入子组件
    import Header from "./components/header.vue";
    import Footer from "./components/footer.vue";
</script>

<style scoped>

</style>