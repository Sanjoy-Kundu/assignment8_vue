<script setup>
import {ref, reactive, defineProps, defineEmits} from 'vue'
defineProps(['parent'])
//calculation emit
const emit = defineEmits();

const emitMessage = () => {
  emit('messageEmitted', 'This message form Child Component');
};
</script>
<template>
	<div class="shadow-xl">
		<h2 class="text-center">This is child component</h2>
		<button class="py-5 bg-green-300 mt-5" @click="emitMessage">SHOW MESSAGE</button>
	</div>
</template>
<style scoped>
button{
	margin-left: 25px;
}
</style>