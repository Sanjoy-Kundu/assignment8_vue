<script setup>
  import ChildComponent from './ChildComponent.vue';
  import { ref } from 'vue';
  
  const parentMessage = ref('Hello from Parent Component');
  const emittedMessage = ref('');
  
  const handleMessageEmitted = (message) => {
	emittedMessage.value = message;
  };
  </script>



<template>
	<div class="parent">
	  <h1>Parent Component <b>{{ parentMessage}}</b></h1>
	  
	  <ChildComponent :message="parentMessage" @messageEmitted="handleMessageEmitted" />
	  <p><mark>Child Component Message:</mark> {{ emittedMessage }}</p>
	</div>
  </template>



  <style scoped>
  </style>
  


<!-- <script setup>
import {ref, reactive} from 'vue'
import ChildComponent from './ChildComponent.vue';

const parentMessage = ref('I am Parent Component');

function messageEmited(e){

}
</script>
<template>
	<h2>This is Parent  Component</h2>
	<ChildComponent :parent = "parentMessage" @messageEmited = "handelMessageEmited"/>
</template>
<style scoped></style> -->