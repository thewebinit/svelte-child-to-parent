<script lang="ts">
	import TodoForm from './TodoForm.svelte';

	let todos = [];

	const addTodo = (event) => {
		todos = [...todos, event.detail.todoContent];
	};
</script>

<main>
	Welcome to dummy todo app!

	{#each todos as todo}
		<p>{todo}</p>
	{/each}

	<TodoForm on:todoCreate={addTodo} />
</main>
