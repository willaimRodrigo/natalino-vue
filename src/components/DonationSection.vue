<script setup>
    import hands from "../assets/illustration2.png";
    import click from "../components/Button.vue";
</script>

<template>
    <section>
        <div class="container">
            <img :src="hands" class="store" alt="Ilustração de mãos segurando enfeite de arvore de natal">
            <div class="info-donation">
                <h2>Conectando generosidade ao redor do mundos</h2>
                <p>Celebre a magia do Natal de uma maneira especial! Descubra a plataforma que permite a doação de presentes significativos para aqueles que mais precisam. Faça parte do movimento e compartilhe o verdadeiro espírito da generosidade.</p>
                <click/>
            </div> 
        </div>
    </section>
</template>

<style lang="scss" scoped>
        section {
        display: flex;  
        justify-content: center; 
        width: 100%; 

        @media (max-width: 820px) {
            height: 80vh;
        }

        @media (max-width: 428px) {
                width: 100%;
                height: 52rem;
                gap: 2rem;
        }

        .container {
            width: 80%;
            height: 34.5rem;
            display: flex;
            justify-content: space-between;
            align-items: center;

            @media (max-width: 820px) {
                flex-direction: column;
                margin-block: 3rem;
            }
            
            @media (max-width: 428px) {
                width: 28rem;
                height: 40rem;
                gap: 2rem;
            }
            
        }

        .info-donation {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            width: 45%;
            height: 24.625rem;

            @media (max-width: 820px) {
                width: 80%;
                align-items: center;
                gap: 2rem;
            }

            @media (max-width: 428px) {
                height: 46rem;
            }
        }
        
        h2 {
           font-weight: 600;
           font-size: 2.5rem;
           line-height: 3rem; 

           @media (max-width: 820px) {
                text-align: center;
            }

            @media (max-width: 428px) {
                font-size: 2rem;
                line-height: 2.4rem;
            }
        }

        p {
            font-weight: 400;
            font-size: 1.35rem;
            line-height: 2rem;

            @media (max-width: 820px) {
                text-align: center;
            }

            @media (max-width: 428px) {
                font-size: 1.125rem;
                line-height: 1.7rem;
            }
        }

        .store {

            @media (max-width: 428px) {
                width: 20.41rem;
            }
        }
    }
</style>