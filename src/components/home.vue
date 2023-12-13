<template>
    <section id="Home">
        <div class="text">
            <h1>Mauricio Rufino</h1>
            <h3>Desenvolvedor Full-Stack</h3>
        </div>

        <img class="perfil" src="/assets/mauzin.webp">
    </section>
</template>

<script>
    export default {
        name: 'home'
    }
</script>

<style>
    :root {
        --colorVue: #41B883;
    }

    .text h1{
        font-size: 36px;
        color: white;
        font-weight: 600;
    }

    .text{
        margin-right: 20px;
    }

    .text h3{
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-size: 24px;
        font-weight: 100;
        color: var(--colorVue);
        text-align: end;
    }

    #Home{
        height: 800px;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    
    .perfil{
        width: 200px;
        border-radius: 50%;
    }

    @media (max-width: 511px) {
        #Home{
            flex-direction: column;
        }

        .text{
            margin: 0;
        }
    }
</style>