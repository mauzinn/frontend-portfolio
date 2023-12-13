<template>
    <section id="Contate-me" class="form-background">
        <h2 class="text-about">Contact-me</h2>

        <form class="form" @submit="SEND_EMAIL">
            <messageVue :message="alert" v-show="alert" />

            <div>
                <input type="text" class="input" v-model="name" placeholder="Name" required>
                <input type="email" class="input" v-model="email" placeholder="Seu email de contato" required>
            </div>
            <textarea class="input textarea" v-model="message" placeholder="Mensagem"></textarea>

            <button class="send-button">Enviar</button>
        </form>
    </section>
</template>

<script>
    import messageVue from './message.vue'

    export default {
        name: 'contact',
        data() {
            return {
                name: '',
                email: '',
                message: '',
                alert: ''
            }
        },
        components: {
            messageVue
        },
        methods: {
            async SEND_EMAIL(e) {
                e.preventDefault()

                const URL = 'https://backend-portfolio-psi.vercel.app/email/send'

                const request = await fetch(URL, {
                    method: 'POST',
                    body: JSON.stringify({
                        name: this.name,
                        email: this.email,
                        message: this.message
                    }),
                    headers: {
                        "Content-Type": "application/json"
                    }
                }).then(async(res) => {
                    const response = await res.json()

                    if (response.result) {
                        this.name = ''
                        this.email = ''
                        this.message = ''

                        this.alert = "Mensagem enviada!"
                        setTimeout(() => {
                            this.alert = ''
                        }, 1500)
                    } else {
                        this.alert = response.error
                        setTimeout(() => {
                            this.alert = ''
                        }, 1500)
                    }
                })
            }
        }
    }
</script>

<style>
    .form-background {
        background-color: #40424A;
        width: 700px;
        border-radius: 16px;
        padding: 30px 10px;
    }

    .form{
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        margin-top: 30px;
    }

    .send-button{
        padding: 14px 26px;
        border-radius: 10px;
        border: none;
        font-size: 15px;
        background-color: var(--colorVue);
        color: white;
        cursor: pointer;
    }

    .send-button:hover{
        transform: scale(105%);

        background-color: #2d9e6b;

        transition: 0.3s;
    }

    .input{
        width: 95%;
        margin: 10px;
        padding: 12px;
        outline: none;
        border-radius: 8px;
        border: none;
        font-size: 15px;
    }

    .form div{
        display: flex;
        width: 100%;
    }

    .textarea{
        resize: none;
        height: 140px;
        width: 93%;
    }

    @media (max-width: 740px) {
        .form-background{
            width: 100%;
            border-radius: 0;
            padding: 20px 0px;
        }
    }

    @media (max-width: 390px) {
        .form div{
            flex-direction: column;
        }

        .form div input {
            width: 85%;
        }

        .textarea{
            width: 85%;
        }
    }
</style>