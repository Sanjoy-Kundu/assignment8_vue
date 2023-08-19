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
	  <h1 class="text-center">Parent Component</h1>
    <p>Child Component Message: <span>{{ emittedMessage }}</span></p> <br>
	  <ChildComponent :message="parentMessage" @messageEmitted="handleMessageEmitted" />
	 
	</div>
  </template>



  <style scoped>
  h1{
    font-size: 30px;
    font-weight: bolder;
    text-align: c;
  }
  span{
    text-align: center;
    font-weight: bolder;
    font-size: 20px;
    color: green;
  }
  p{
    padding-left: 20px;
  }
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