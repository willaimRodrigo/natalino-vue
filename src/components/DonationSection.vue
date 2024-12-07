<script setup>
    import hands from "../assets/illustration2.png";
    import click from "../components/Button.vue";
</script>

<template>
    <section>
        <img :src="hands" class="store" alt="Ilustração de mãos segurando enfeite de arvore de natal">
        <div>
            <h2>Conectando generosidade ao redor do mundos</h2>
            <p>Celebre a magia do Natal de uma maneira especial! Descubra a plataforma que permite a doação de presentes significativos para aqueles que mais precisam. Faça parte do movimento e compartilhe o verdadeiro espírito da generosidade.</p>
            <click/>
        </div>
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