<script setup>
    import frame from "../assets/Frame.png";
    import store from "../assets/imagem.png";
    import click from "./Button.vue";
</script>

<template>
    <section>
        <div class="presentation">
            <h4><img :src="frame" alt="Animação do rosto do papai noel">Feliz Natal</h4>
            <h1>Uma <span>plataforma de doação</span> para espalhar alegria</h1>
            <p>Nessas festas de fim de ano mande um presente
                para a pessoa amada e compartilhe a alegria do Natal.</p>

            <click/>
        </div>
        <img :src="store" class="store" alt="Ilustração fachada de oja com criança no frente e neve">
    </section>
</template>

<style lang="scss" scoped>
    section {
        display: flex;  
        justify-content: center; 
        align-items: center;
        width: 100%; 
        height: 32rem;
        gap: 9%;
        background-color: #ffe9e8; 

        @media (max-width: 800px) {
            flex-direction: column;
            height: 80vh;
        }

        @media (max-width: 428px) {
            width: 90%;
            height: 110vh;
            gap: .5rem;
        }
        

        .presentation {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            width: 40%;
            height: 21rem;

            @media (max-width: 800px) {
                width: 80%;
                align-items: center;
            }

            @media (max-width: 428px) {
                width: 80%;
            }
        }

        h4 {
            display: flex;
            align-items: center;
            justify-content: space-between;
            font-weight: 500;
            font-size: 24px;
            line-height: 1.6rem;
            width: 10rem;

            img {
                width: 2.1875rem;
                height: 2.37rem;
            }
        }

        h1 {
            font-weight: 600;
            font-size: 2.5rem;
            line-height: 3rem;

            span {
                color: red;
            }

            @media (max-width: 800px) {
                text-align: center;
            }

            @media (max-width: 428px) {
                font-size: 2rem;
                line-height: 2.4rem;
            }
        }

        p {
            font-weight: 400;
            font-size: 1.5rem;
            line-height: 2.25rem;

            @media (max-width: 800px) {
                text-align: center;
            }

            @media (max-width: 428px) {
                font-size: 1.12rem;
                line-height: 1.7rem;
            }
        }
        
        #store {
            width: 40%;

            @media (max-width: 428px) {
                width: 19.375rem;
            }
        }
    }
</style>