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
        <div class="container">
            <h4><img :src="frame" alt="Animação do rosto do papai noel">Feliz Natal</h4>
            <div class="icons">
                <img :src="twitter" alt="Logo do twitter">
                <img :src="whats" alt="logo do whatsapp">
                <img :src="insta" alt="logo do instagram">
                <img :src="face" alt="logo do facebook">
                <img :src="google" alt="logo do google">
            </div> 
        </div>
        
    </section>
</template>

<style lang="scss" scoped>
    section {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        background-color: #ffe9e8;
        height: 5rem;

        @media (max-width: 820px) {
                height: 12rem;
                
            }
        
        .container {
            width: 80%;
            display: flex;
            justify-content: space-between;

            @media (max-width: 800px) {
                display: flex;
                flex-direction: column;
                align-items: center;
                justify-content: space-around;
                height: 90%;
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

        .icons {
            display: flex;
            justify-content: space-between;
            width: 30%;
            cursor: pointer;

            @media (max-width: 820px) {
                width: 55%;
            }
        }

        img {
            width: 2.5rem;
            height: 2.5rem;
        }
    }
</style>