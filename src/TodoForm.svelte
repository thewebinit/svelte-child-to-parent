<script lang="ts">
	import { createEventDispatcher } from 'svelte';

	const dispatch = createEventDispatcher();

	let todoContent = '';

	const handleSubmit = () => {
		dispatch('todoCreate', { todoContent });
	};
</script>

<form on:submit|preventDefault={handleSubmit}>
	<input type="text" bind:value={todoContent} />
	<button>Add todo</button>
</form>
