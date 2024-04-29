<script setup>
import { ref } from 'vue';
const number = ref('0000 0000 0000 0000');
const name = ref('JANE APPLESEED');
const date = ref('00/00');
</script>

<template>
    <div>
        <img
            src="/images/bg-card-front.png"
            alt="Front of the credit card"
            class="card" />
        <section>
            <img
                src="/images/card-logo.svg"
                alt="card logo"
                class="absolute logo" />
            <p class="absolute number">{{ number }}</p>
            <p class="absolute name">{{ name }}</p>
            <p class="absolute date">{{ date }}</p>
        </section>
    </div>
</template>

<style scoped>
.absolute {
    position: absolute;
}
.logo {
    width: 50px;
    top: 20px;
    left: 20px;
}
.number {
    width: 100%;
    top: 60px;
    text-align: center;
}
.name {
    width: 200px;
    bottom: 5px;
    left: 20px;
}
.date {
    width: 50px;
    bottom: 5px;
    right: 20px;
}
p,
h2 {
    color: hsl(270, 3%, 87%);
}
</style>
