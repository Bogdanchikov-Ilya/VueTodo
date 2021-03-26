<template>
	<div class="todo__wrapper">
		<div class="todo__body">
			<ul>
				<li v-for="(task, index) in tasks" :key="index" @click="deleteTask(index)">Индекс - {{index}},  Задача - {{ task }}</li>
			</ul>
			<h2>{{text}}</h2>
		</div>
	</div>
</template>

<script>
	export default {
		props: ['tasks', 'text'],
		methods: {
			deleteTask(index){this.$emit('delete-task', index)}}
	}
</script>