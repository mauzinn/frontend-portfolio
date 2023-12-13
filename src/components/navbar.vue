<template>
    <header class="header">
        <section class="navbar fixed-top">
            <nav>
                <ul class="nav">
                    <li v-for="link in navLinks" :key="link"><a class="link" :href="'#' + link">{{link}}</a></li>
                </ul>
            </nav>

            <section>
                <a href="https://github.com/mauzinn"><img class="icon" src="/assets/github.png"></a>
            </section>
        </section>
    </header>
</template>

<script>
    export default {
        name: 'navbar',
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
    .fixed-top {
        position: fixed;
        top: 0;
        width: 100%;
    }
</style>

<style>
    .navbar{
        display: flex;
        justify-content: space-around;
        align-items: center;
        padding: 20px;
        backdrop-filter: blur(3px);
        z-index: 3;
    }

    .nav{
        list-style-type: none;
        display: flex;
        width: 500px;
        justify-content: space-between;
        margin: 0;
        padding: 0;
    }

    .link{
        color: white;
        text-decoration: none;
    }

    li:hover{
        transform: scale(1.1);

        transition: 0.3s;
    }

    .icon{
        width: 50px;
    }

    .icon:hover{
        transform: scale(105%);
        
        transition: 0.3s;
    }

    .header{
        height: 90px;
    }

    @media (max-width: 624px) {
        nav {
            display: none;
        }
    }
</style>