<template>
    <section class="alert">
        <p>{{message}}</p>
    </section>
</template>

<script>
    export default {
        name: 'message',
        props: {
            message: String
        }
    }
</script>

<style>
    .alert{
        background-color: rgba(0, 195, 255, 0.651);
        padding: 20px;
        color: rgb(0, 68, 255);
        border: 1px solid currentColor;
        border-radius: 10px;   
        width: 300px;
    }
</style>