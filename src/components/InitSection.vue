<script setup>
    import frame from "../assets/Frame.png";
    import store from "../assets/imagem.png";
    import click from "./Button.vue";
</script>

<template>
    <section>
        <div>
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
        width: 100%;  

        div {
            width: 50%;
        }
        
        #store {
            width: 31.25rem;
        }
    }
</style>