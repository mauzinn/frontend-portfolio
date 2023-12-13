<template>
    <section class="fixed-top">
        <nav>
            <ul class="nav-mobile">
                <li v-for="link in navLinks" :key="link"><a class="link" :href="'#' + link">{{link}}</a></li>
            </ul>
        </nav>
    </section>
</template>

<script>
    export default {
        name: 'menu',
        data() {
            return {
                navLinks: [
                    'Home',
                    'Sobre',
                    'Habilidades',
                    'Projetos',
                    'Contate-me'
                ]
            }
        }
    }
</script>

<style scoped>
    .fixed-top{
        position: fixed;
        top: 0;
        width: 100%;
        height: 100vh;
        backdrop-filter: blur(7px);
        z-index: 3;
        display: flex;
        align-items: center;
    }
</style>

<style>
    .nav-mobile{
        display: flex;
        list-style: none;
        flex-direction: column;
    }
</style>