<script setup>
    import gifts from "../assets/illustration.png";
    import { ref, onMounted } from "vue";

    const targetDate = new Date(new Date().getFullYear(), 11, 24);
    const timeRemaning = ref({
        days: 0,
        hours: 0,
        minutes: 0,
        seconds: 0
    });

    const calculateTimeRemaining = () => {
        const now = new Date();
        const difference = targetDate - now;

        if (difference > 0) {
            timeRemaning.value = {
                days: Math.floor(difference / (1000 * 60 * 60 * 24)),
                hours: Math.floor((difference/ (1000 * 60 * 60)) % 24),
                minutes: Math.floor((difference / (1000 * 60)) % 60),
                seconds: Math.floor((difference / 1000) % 60),
            }
        } else {
            timeRemaning.value = { days: 0, hours: 0, minutes: 0, seconds: 0}
        }
    }

    onMounted(() => {
        calculateTimeRemaining();
        setInterval(calculateTimeRemaining, 1000);
    })
</script>

<template>
    <section>
        <div>
            <h3>Tempo limitado</h3>
            <p>Nessas festas de fim de ano mande um presente para a pessoa amada e compartilhe a alegria do Natal.</p>
        </div>
        <div class="date">
            <h5>
                {{ timeRemaning.days }}d -
                {{ timeRemaning.hours }}h -
                {{ timeRemaning.minutes }}m -
                {{ timeRemaning.seconds }}s
            </h5>
        </div>

        <img :src="gifts" alt="Ilustração de presentes">
    </section>
</template>

<style lang="scss" scoped>
    section {
        display: flex;  
        justify-content: center; 
        flex-direction: column;
        align-items: center;
        width: 100%;  
        margin-block: 4rem;


        div {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            width: 29.875rem;
            height: 8rem;

            @media (max-width: 428px) {
                width: 20.41rem;
            }
        }

        h3 {
            text-align: center;
            font-weight: 600;
            font-size: 2.5rem;
            line-height: 2.7rem;

            @media (max-width: 428px) {
                font-size: 2.5rem;
                line-height: 2.15rem;
            }
        }

        p {
            text-align: center;
            font-weight: 400;
            font-size: 1.25rem;
            line-height: 2rem;

            @media (max-width: 428px) {
                font-size: 1.25rem;
                line-height: 1.75rem;
            }
        }

        .date {
            margin: 1rem;
            width: 37.5rem;
            height: 4.37rem;
            text-align: center;
            font-weight: 600;
            font-size: 4rem;
            line-height: 4.25rem;
            color: red;

            @media (max-width: 428px) {
                height: 2.2rem;
                font-size: 3rem;
                line-height: 2.15rem;
            }
        }

        img {
            width: 29.875rem;

            @media (max-width: 428px) {
                width: 20.41rem;
            }
        }
    }
</style>