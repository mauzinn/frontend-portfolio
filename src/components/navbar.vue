<template>
    <header class="header">
        <menuVue v-show="MENU_OPENED" />
        <section class="navbar fixed-top">
            <button @click="MENU" class="menu-button" :id="button">Menu</button>

            <nav>
                <ul class="nav">
                    <li v-for="link in navLinks" :key="link"><a class="link" :href="'#' + link">{{link}}</a></li>
                </ul>
            </nav>

            <a href="https://github.com/mauzinn"><img class="icon" src="/assets/github.png"></a>
        </section>
    </header>
</template>

<script>
    import menuVue from './menu.vue'

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
                ],
                MENU_OPENED: false
            }
        },
        components: {
            menuVue
        },
        methods: {
            MENU() {
                this.MENU_OPENED = !this.MENU_OPENED
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

    @media (max-width: 624px) {
        nav {
            display: none;
        }

        .menu-button{
            display: block;
        }
    }
</style>

<style>
    .navbar{
        display: flex;
        justify-content: space-around;
        align-items: center;
        padding: 20px 0px;
        backdrop-filter: blur(3px);
        z-index: 3;
    }

    .menu-button{
        color: var(--colorVue);
        padding: 20px 14px;
        border-radius: 50%;
        background: none;
        border: 1px solid currentColor;
        display: none;
    }

    .menu-button:hover{
        transform: scale(105%);

        transition: 0.3s;
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
</style>