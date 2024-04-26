<script setup>
import Attribution from '../components/Attribution.vue';
import CardFull from '../components/CardFull.vue';

import { ref, onBeforeMount, computed, onMounted } from 'vue';

const cardBackground = ref('');

const updateScreenSize = () => {
    const screenWidth = window.innerWidth;
    cardBackground.value =
        screenWidth <= 1440
            ? '/images/bg-main-mobile.png'
            : '/images/bg-main-desktop.png';
};
onMounted(() => {
    window.addEventListener('resize', updateScreenSize);
    updateScreenSize();
});
onBeforeMount(() => {
    window.removeEventListener('resize', updateScreenSize);
});
</script>
<template>
    <section
        :style="`background-image: url(${cardBackground})`"
        id="card-background">
        <CardFull />
    </section>

    <Attribution />
</template>
<style scoped>
#card-background {
    background-color: purple;
    background-repeat: no-repeat;
    background-size: cover;
    height: 220px;
    display: flex;
    justify-content: center;
}
</style>
