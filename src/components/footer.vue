<script setup>
    const props = defineProps({
        user: Number,
        url: {
            type: String,
            required: false,
            default: "dengruicode.com",
        },
    });
    console.log(props);
</script>

<template>
    <h3>Footer</h3>
    {{ props.user }}
</template>

<style scoped></style>
