<template>
    <section id="Habilidades">
        <h2 class="text-about">Habilidades</h2>

        <section class="skills">
            <article class="skill" v-for="skill in skills" :key="skill.name">
                <img :src="skill.url">
                <h3>{{skill.name}}</h3>
            </article>
        </section>
    </section>
</template>

<script>
    export default {
        name: 'skills',
        data() {
            return {
                skills: [
                    {
                        name: "JavaScript",
                        url: "/assets/javascript.jpeg"
                    },
                    {
                        name: "TypeScript",
                        url: "/assets/typescript.png"
                    },
                    {
                        name: "Node.js",
                        url: "/assets/nodejs.png"
                    },
                    {
                        name: "Vue.js",
                        url: "/assets/vue.png"
                    },
                    {
                        name: "HTML",
                        url: "/assets/html.png"
                    },
                    {
                        name: "CSS",
                        url: "/assets/css.png"
                    },                   
                    {
                        name: "Bootstrap",
                        url: "/assets/bootstrap.jpg"
                    }
                ]
            }
        }
    }
</script>

<style>
    .skills{
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        margin-top: 60px;
    }

    .skill{
        background-color: #262936;
        height: 190px;
        width: 150px;
        margin: 20px;
        border-radius: 20px;
        text-align: center;
        padding: 20px 10px;
    }

    .skill:hover{
        transform: scale(105%);

        transition: 0.3s;
    }

    .skill img{
        width: 120px;
        height: 120px;
    }

    .skill h3{
        color: white;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-weight: 200;
    }

    #Habilidades{
        margin-bottom: 80px;
    }
</style>