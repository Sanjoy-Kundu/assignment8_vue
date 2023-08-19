<script setup>
import {ref, reactive} from 'vue'
import ParentComponent from './components/ParentComponent.vue';
</script>

<template>
<div class="parent shadow-lg">
	<h1 class="text-center">This is app Component</h1>
	<ParentComponent/>
</div>
</template>

<style scoped>
.parent{
	width: 75%;
	margin: 0 auto;
	border: 1px solid rgb(168, 160, 160);
	padding: 2px;
	background-color: #b0f5c0;
}
h1{
	font-size: 30px;
	font-weight: bolder;
}
</style>
