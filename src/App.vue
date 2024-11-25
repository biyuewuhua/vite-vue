<template>
    <Header @getWeb="emitsGetWeb" @userAdd="emitsUserAdd"/>
    {{ web.url }} - {{ user }}
</template>

<script setup>
    import { reactive, ref } from "vue";
    import Header from "./components/header.vue";

    const web = reactive({
        name: "邓瑞编程",
        url: "dengruicode.com",
    });

    const user = ref(0);

    const emitsGetWeb=(data) =>{
        console.log(data);
        web.url = data.url;
    }

    const emitsUserAdd = (data) =>{
        console.log(data);
        user.value +=data;
    }
</script>


<style scoped></style>
