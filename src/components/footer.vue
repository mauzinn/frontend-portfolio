<template>
    <footer class="footer">
        <contactVue />

        <p class="copyright">Made by mauzin</p>
    </footer>
</template>

<script>
    import contactVue from './contact.vue'

    export default {
        name: 'footer',
        components: {
            contactVue
        }
    }
</script>

<style>
    .footer{
        width: 100%;
        background-color: #2C2C37;
        display: flex;
        justify-content: center;
        flex-direction: column;
        align-items: center;
        padding: 60px 0px;
        margin-top: 100px;
    }

    .copyright{
        color: white;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-weight: 100;
        font-size: 18px;
        margin-top: 60px;
    }
</style>