<script setup>
    import frame from "../assets/Frame.png"; 
    import twitter from "../assets/logo-twitter.png";
    import whats from "../assets/logo-whatsapp.png";
    import insta from "../assets/logo-instagram.png";
    import face from "../assets/logo-facebook.png";
    import google from "../assets/logo-google.png";
</script>

<template>
    <section>
        <h4><img :src="frame" alt="Animação do rosto do papai noel">Feliz Natal</h4>
        <div>
            <img :src="twitter" alt="Logo do twitter">
            <img :src="whats" alt="logo do whatsapp">
            <img :src="insta" alt="logo do instagram">
            <img :src="face" alt="logo do facebook">
            <img :src="google" alt="logo do google">
        </div>
    </section>
</template>

<style lang="scss" scoped>
    section {
        display: flex;
        justify-content: space-between;
        width: 100%;
        
        div {
            
        }

        img {
            width: 2.5rem;
            height: 2.5rem;
        }
    }
</style>