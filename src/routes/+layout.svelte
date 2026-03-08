<script lang="ts">
	import './layout.css';
	import logo from '$lib/assets/profile.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" type="image/svg+xml" href={logo} />
</svelte:head>

<main
	class="w-full max-w-2xl overflow-hidden border-6 border-dark-muted bg-light-muted p-4 shadow-hard md:p-8"
>
	{@render children()}
</main>
