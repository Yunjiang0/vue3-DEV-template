<script setup lang="ts">
import { useCounterStore } from '@/stores/counter';
const CountStore = useCounterStore();
</script>
<template>
	<div class="about">
		<h1>This is an about page</h1>
		<h2>Count:{{ CountStore.count }}</h2>
		<h2>2*count:{{ CountStore.doubleCount }}</h2>
		<button @click="CountStore.increment">点击按钮加1</button>
	</div>
</template>

<style>
@media (min-width: 1024px) {
	.about {
		min-height: 100vh;
		display: flex;
		justify-content: center;
		flex-direction: column;
		align-items: center;
	}
}
</style>
