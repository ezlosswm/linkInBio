<script lang="ts">
	import './layout.css';

	let { children } = $props();
</script>

<main
	class="w-full max-w-2xl overflow-hidden border-6 border-dark-muted bg-light-muted p-4 shadow-hard md:p-8"
>
	{@render children()}
</main>
