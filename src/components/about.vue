<template>
    <section id="Sobre">
        <h2 class="text-about">Sobre</h2>

        <section class="body-about">
            <img class="perfil-about" src="/assets/fullstack.gif">
            <p class="text">Oi, sou o Mauricio, com 15 anos, explorando o mundo do 
            desenvolvimento Full Stack. Tenho me aventurado em tecnologias como <b>Node.js</b>, <b>Vue.js</b>, <b>HTML</b>, <b>CSS</b>, <b>JavaScript</b>, <b>TypeScript</b> e <b>Bootstrap</b>.
            Estou trabalhando para entender essas ferramentas e criar coisas legais.
            Embora eu ainda esteja aprendendo, tenho lidado com projetos que envolvem essas tecnologias.
            Estou aberto a desafios e oportunidades para expandir meu conhecimento. Ainda não sou um expert,
            mas estou progredindo e pronto para colaborar em projetos interessantes. Vamos criar algo juntos!</p>
        </section>
    </section>
</template>

<script>
    export default {
        name: 'about'
    }
</script>

<style scoped>
    .text{
        color: white;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-size: 18px;
        font-weight: 200;
    }
</style>

<style>
    .text-about{
        color: var(--colorVue);
        font-size: 33px;
        text-align: center;
    }

    b{
        color: var(--colorVue);
    }

    .body-about{
        display: flex;
        width: 900px;
        margin-top: 30px;
        align-items: center;
    }

    .perfil-about{
        margin-right: 30px;
        height: 300px;
        width: 250px;
    }

    #Sobre{
        display: flex;
        align-items: center;
        flex-direction: column;
        margin-bottom: 100px;
    }

    @media (max-width: 948px) {
        .body-about{
            width: 100%;
        }
    }

    @media (max-width: 506px) {
        .body-about{
            flex-direction: column;
            justify-content: center;
        }
        .perfil-about{
            margin: 0;
        }
    }
</style>