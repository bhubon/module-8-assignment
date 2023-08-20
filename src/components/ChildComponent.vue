<script setup>
defineProps(['message'])
const emits = defineEmits('update:message')

function messageEmitted() {
    emits('update:message', 'Hello World From Child Emit')
}

</script>

<template>
    <div>
        <p class="mt-8">Child Component</p>
        <h2 class="text-xl my-3">Message: <span class="text-green-600">{{ message }}</span></h2>
        <button @click="messageEmitted()"
            class="bg-blue-500 hover:bg-blue-700 text-white font-bold my-8 py-2 px-4 rounded">Change Message</button>
    </div>
</template>

<style scoped></style>