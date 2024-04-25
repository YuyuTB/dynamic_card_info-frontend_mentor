<script setup>
import CardBack from '../components/CardBack.vue';
import CardFront from '../components/CardFront.vue';
</script>

<template>
    <div id="card-wrapper">
        <CardBack id="card-back" />
        <CardFront id="card-front" />
    </div>
</template>

<style scoped>
#card-wrapper {
    padding: 40px 20px 0 20px;
    width: 400px;
}
/* #card-back {
}
#card-front {
} */
</style>
