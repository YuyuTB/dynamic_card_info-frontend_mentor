<script setup>
import Attribution from '../components/Attribution.vue';
import CardFull from '../components/CardFull.vue';
import { ref, onBeforeMount, computed, onMounted } from 'vue';
import CardForm from '../components/CardForm.vue';

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
        class="card-background">
        <CardFull />
    </section>
    <CardForm />

    <Attribution class="attribution" />
</template>
<style scoped>
.card-background {
    background-color: purple;
    background-repeat: no-repeat;
    background-size: cover;
    height: 230px;
    display: flex;
    justify-content: center;
}
.attribution {
    position: relative;
    bottom: 10px;
    left: 0;
    width: 100%;
    height: 100px;
}
</style>
