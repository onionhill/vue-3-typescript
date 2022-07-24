<script setup lang="ts">
import {reactive} from 'vue'
import Counter from './components/Counter.vue'

interface AppInfo {
	name: string;
	slogan: string;
}

const appInfo:AppInfo = reactive({
	name: 'vegard',
	slogan: 'yolo!'
})


</script>


<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <div>
  <h1>{{ appInfo.name }}</h1>
  <h2>{{appInfo.slogan}}</h2>
  <Counter
	:limit="10"
  ></Counter>
  
  </div>
</template>