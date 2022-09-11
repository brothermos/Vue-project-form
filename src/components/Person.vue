<template>
    <card>
        <template v-slot:card-header>
            <h1>{{ name }}</h1>
        </template>

        <template v-slot:card-content>
            <p>เพศ : {{ gender }}</p>
            <p>เงินเดือน : {{ salary }} บาท,</p>
            <p>ตำแหน่งงาน: {{ department }}</p>
            <p>ทักษะด้านภาษา : {{ skill }}</p>
        </template>
    </card>
</template>

<script>
import Card from "./Card.vue";
export default {
    name: "Person",
    components: {
        Card,
    },
    props: {
        name: {
            type: String,
            requried: true,
        },
        salary: {
            type: Number,
            default: 15000,
        },
        department: {
            type: String,
            required: true,
        },
        gender: {
            type: String,
        },
        skill: {
            type: Array,
        },
    },
};
</script>

<style scoped>
h1 {
    color: yellow;
}
button {
    font: inherit;
    cursor: pointer;
    border: 1px solid #ff0077;
    background: #ff0077;
    color: white;
    padding: 0.05rem 1rem;
    box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.26);
    margin: 5px;
    border-radius: 10px;
}
.fade-enter-from {
    opacity: 0;
}
.fade-enter-active {
    transition: all 0.5s linear;
}
</style>
