<template>
        <button :class="classes">{{ name }}</button>
</template>

<script>
export default {
    name: "ButtonComponent",
    props: {
        name: {
            type: String,
            required: true
        },
        classes: {
            type: String,
            required: true
        }
    }
};
</script>

<style>
    button{
        font-family: "Raleway";
        font-weight: 600;
        font-size: 16px;
    }
</style>
