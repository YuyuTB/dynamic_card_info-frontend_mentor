<script setup>
import CardBack from '../components/CardBack.vue';
import CardFront from '../components/CardFront.vue';
</script>

<template>
    <div class="card-wrapper">
        <CardBack class="card-back" />
        <CardFront class="card-front" />
    </div>
</template>

<style scoped>
.card-wrapper {
    padding: 40px 20px 0 20px;
    width: 280px;
}
.card-back {
    transform: translate(10%, -5%);
}
.card-front {
    transform: translate(-10%, -50%);
}
</style>
