<script setup>
import SubmitButton from './SubmitButton.vue';

const name = defineModel('name', { required: true });
const number = defineModel('number', { required: true });
const month = defineModel('month', { required: true });
const year = defineModel('year', { required: true });
const cvc = defineModel('cvc', { required: true });
</script>

<template>
    <form class="form">
        <label
            for="name"
            class="label"
            >CARDHOLDER NAME</label
        >
        <input
            type="text"
            v-model="name"
            placeholder="e.g. Jane Appleseed" />
        <label
            for="number"
            class="label"
            >CARD NUMBER</label
        >
        <input
            type="text"
            v-model="number"
            placeholder="e.g. 1234 5678 9123 0000" />
        <div>
            <div class="grid">
                <div>
                    <div class="label">
                        <label for="month">EXP. DATE </label>
                        <label for="year">(MM/YY)</label>
                    </div>
                    <div class="grid">
                        <input
                            type="text"
                            v-model="month"
                            placeholder="MM"
                            class="date" />
                        <input
                            type="text"
                            v-model="year"
                            placeholder="YY"
                            class="date" />
                    </div>
                </div>
                <div class="label">
                    <label for="cvc">CVC</label>
                    <input
                        type="text"
                        v-model="cvc"
                        placeholder="e.g. 123"
                        class="cvc" />
                </div>
            </div>
        </div>
        <SubmitButton />
    </form>
</template>

<style scoped>
.form {
    margin-top: 50px;
    display: flex;
    flex-direction: column;
    padding: 25px;
}
.label {
    margin: 20px 0 5px;
}
label {
    font-size: 0.8rem;
}
input {
    height: 40px;
    border-radius: 8px;
    border: 1px solid hsl(270, 3%, 87%);
    color: hsl(279, 6%, 55%);
    text-indent: 10px;
}
.grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
}
.date {
    width: 80%;
}
.cvc {
    margin-top: 5px;
}
</style>
