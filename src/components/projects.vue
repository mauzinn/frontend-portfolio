<template>
    <section id="Projetos">
        <h2 class="text-about">Projetos</h2>

        <section class="projects">


            <article class="project project-1">
                <section class="info-project">
                    <h3 class="project-name">Game collision 3D</h3>

                    <section class="project-icons">
                        <img src="/assets/javascript.jpeg">
                        <img src="/assets/html.png">
                    </section>

                    <a href="https://github.com/mauzinn/game-THREE-JS">Repository</a>
                </section>
            </article>

            <article class="project project-2">
                <section class="info-project">
                    <h3 class="project-name">To do vuex</h3>

                    <section class="project-icons">
                        <img src="/assets/vue.png">
                        <img src="/assets/javascript.jpeg">
                        <img src="/assets/html.png">
                    </section>

                    <a href="https://github.com/mauzinn/To-do-vuex">Repository</a>
                </section>
            </article>

            <article class="project project-3">
                <section class="info-project">
                    <h3 class="project-name">back-end DevsWeb</h3>

                    <section class="project-icons">
                        <img src="/assets/typescript.png">
                        <img src="/assets/nodejs.png">
                    </section>

                    <a href="https://github.com/mauzinn/backend-DevsWeb">Repository</a>
                </section>
            </article>


        </section>
    </section>
</template>

<script>
    export default {
        name: 'projects'
    }
</script>

<style scoped>
    .text-about{
        margin-bottom: 70px;
    }
</style>

<style>
    #Projetos {
        height: 500px;
    }

    .project{
        width: 300px;
        height: 300px;
        position: relative;
        overflow: hidden;
        border-radius: 20px;
        margin: 20px;
    }

    .projects{
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
    }

    .project-1 {
        background-image: url('../../public/assets/projectGame.png');
        background-size: cover;
        width: 300px;
        height: 300px;
        background-repeat: no-repeat;
    }

    .project-2 {
        background-image: url('../../public/assets/projectToDo.png');
        background-size: cover;
        width: 300px;
        height: 300px;
        background-repeat: no-repeat;
    }

    .project-3 {
        background-image: url('../../public/assets/projectBackend.png');
        background-size: cover;
        width: 300px;
        height: 300px;
        background-repeat: no-repeat;
    }

    .info-project{
        background-color: rgba(255, 255, 255, 0.76);
        height: 100%;
        width: 100%;
        position: absolute;
        bottom: 0;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        display: none;
    }

    .project:hover .info-project{
        display: block;
        display: flex;
        animation: infoProject 600ms linear;
    }

    .project-name {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-weight: 100;
        font-size: 22px;
        text-align: center;
    }

    .project-icons img {
        width: 40px;
        margin: 5px;
    }

    .project-icons {
        display: flex;
        justify-content: space-evenly;
        align-items: center;
    }

    .info-project a{
        text-decoration: none;
        color: #0E8BFF;
    }

    .info-project a:hover{
        text-decoration: underline;
    }

    @keyframes infoProject {
        from {
            bottom: -30%;
        }

        to {
            bottom: 0%;
        }
    }

    @media (max-width: 1005px) {
        #Projetos{
            height: 850px;
        }
    }

    @media (max-width: 698px) {
        #Projetos{
            height: 1200px;
        }
    }
</style>