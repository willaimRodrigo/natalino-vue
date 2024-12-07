<script setup>
    import gifts from "../assets/illustration.png";
</script>

<template>
    <section>
        <div>
            <h3>Tempo limitado</h3>
            <p>Nessas festas de fim de ano mande um presente para a pessoa amada e compartilhe a alegria do Natal.</p>
            <p>Timer</p>
        </div>
        <img :src="gifts" alt="Ilustração de presentes">
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