<script setup>
import { ref, reactive } from 'vue';
import ChildComponent from './ChildComponent.vue';
const message = ref('Hello World')
</script>

<template>
    <p>Parent Component</p>
    <p class="my-5 text-xl">Message: <span class="text-green-600">{{ message }}</span></p>
    <hr>
    <ChildComponent v-model:message="message" />
</template>

<style scoped></style>