<script setup>
import {ref, reactive, defineProps, defineEmits} from 'vue'
defineProps(['parent'])
//calculation emit
const emit = defineEmits();

const emitMessage = () => {
  emit('messageEmitted', 'Message Show Form Child Component');
};
</script>
<template>
	<h2>This is child component</h2>
	<h2>Message From Parent Component : <b>{{ parent }}</b></h2>
	<button class="py-5 bg-orange-300 mt-5" @click="emitMessage">Child Component</button>
</template>
<style></style>