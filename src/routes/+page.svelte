<script lang="ts">
	import profile from '$lib/assets/images/profile.webp';

	import { navLink } from '$lib/navLinks';
</script>

<svelte:head>
	<title>Carlos Gomez — Frontend / Web Developer / Belizean</title>
	<meta
		name="description"
		content="Carlos Gomez is a passionate Frontend & Web Developer from Belize. Explore selected work, experiments, code repositories, and get in touch."
	/>
	<meta
		name="keywords"
		content="Carlos Gomez, Frontend Developer, Web Developer, Belize, Portfolio, Projects, GitHub, Contact"
	/>
	<meta name="author" content="Carlos Gomez" />
	<meta property="og:title" content="Carlos Gomez — Frontend / Web Developer / Belizean" />
	<meta
		property="og:description"
		content="Explore the portfolio and projects of Carlos Gomez, a Frontend / Web Developer based in Belize."
	/>
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://ezlos.vercel.app/" />
	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:title" content="Carlos Gomez — Frontend / Web Developer / Belizean" />
	<meta
		name="twitter:description"
		content="Portfolio of Carlos Gomez, Frontend & Web Developer from Belize. Explore projects and get in touch."
	/>
</svelte:head>

<div class="group/card relative">
	<!-- Top right square -->
	<div
		class="absolute -top-10 -right-10 size-40 rotate-12 bg-bold-orange opacity-20 transition-transform duration-700 group-hover/card:rotate-0"
	></div>

	<header class="relative mb-12 border-b-6 border-dark pb-4">
		<div
			class="absolute -top-4 -left-4 bg-dark px-2 py-1 text-xs font-bold tracking-widest text-light-muted uppercase"
		>
			Ver: 0.0.1a
		</div>

		<div class="relative float-right mb-4 ml-4">
			<div class="absolute inset-0 -z-10 translate-x-2 translate-y-2 bg-bold-orange"></div>
			<div class="size-32 overflow-hidden border-3 border-dark-muted bg-gray-300 md:h-40 md:w-40">
				<img
					loading="eager"
					fetchpriority="high"
					width="160"
					height="160"
					decoding="async"
					src={profile}
					class="size-full object-cover contrast-125 grayscale transition-all duration-700 group-hover/card:grayscale-25"
					alt="Carlos Gomez Profile"
				/>
			</div>
			<div
				class="absolute -bottom-2 -left-2 bg-dark-muted px-2 py-0.5 text-xs font-bold tracking-widest text-light-muted uppercase"
			>
				ID: R2D2
			</div>
		</div>

		<h1 class="text-6xl leading-none font-black wrap-break-word md:text-8xl">
			Carlos <span class="text-bold-orange">_</span>
			<br />
			Gomez
		</h1>

		<p class="clear-both mt-4 text-xl font-bold uppercase italic md:text-2xl">
			Frontend / Web Developer / Belizean
		</p>
	</header>

	<section class="mb-12 grid grid-cols-1 gap-4 md:grid-cols-2">
		{#each navLink as link}
			<a
				href={link.href}
				class="glitch group/link relative block cursor-pointer border-3 border-dark bg-light-muted p-6 shadow-hard-sm transition-transform last:bg-dark-muted last:text-light-muted last:shadow-hard-accent"
			>
				<span
					class="absolute top-0 right-0 bg-dark-muted px-2 py-1 text-xs text-light-muted uppercase group-last:text-light-muted group-last/link:bg-bold-orange"
					>{link.id}</span
				>
				<h2 class="text-2xl font-black transition-colors group-hover/link:text-bold-orange">
					{link.label}
				</h2>
				<p class="mt-1 text-sm font-bold text-dim-400 uppercase group-last/link:text-dim-200">
					{link.description}
				</p>
			</a>
		{/each}
	</section>

	<footer class="relative">
		<div
			class="overflow-hidden border-y-3 border-dark-muted bg-bold-orange py-2 text-sm font-black whitespace-nowrap text-dark uppercase italic"
		>
			<div class="inline-block animate-banner">
				AVAILABLE FOR HIRE - HELLO - BUILDING THE NEW WEB - RAW CSS ONLY - MINIMALISM IS KEY -
				AVAILABLE FOR HIRE - HELLO - BUILDING THE NEW WEB - RAW CSS ONLY - MINIMALISM IS KEY -
			</div>
		</div>

		<div class="mt-8 flex flex-wrap items-end justify-between gap-4 lg:mt-16">
			<div class="max-w-50 border-3 border-dark-muted p-2">
				<p class="text-xs leading-tight font-bold uppercase">Status: Active</p>
			</div>

			<div class="text-right">
				<p class="mb-1 text-xs font-black uppercase">Stay Connected</p>

				<div class="flex justify-end gap-2">
					<div class="size-4 bg-dark-muted"></div>
					<div class="size-4 bg-dim-400"></div>
					<div class="size-4 bg-bold-orange"></div>
				</div>
			</div>
		</div>
	</footer>

	<!-- Below the banner -->
	<div
		class="pointer-events-none absolute -right-4 bottom-[6%] h-8 w-20 skew-x-12 bg-dark-muted lg:bottom-[9%]"
	></div>

	<!-- Floating square left -->
	<div
		class="pointer-events-none absolute top-[20%] -left-8 h-24 w-12 -rotate-12 border-3 border-dark bg-white transition-transform duration-700 group-hover/card:rotate-12 group-hover/card:bg-bold-orange md:-left-12"
	></div>
</div>

<style>
	.glitch:hover {
		transform: translate(-2px, -2px);
		box-shadow: 8px 8px 0 0 var(--color-bold-orange);
	}
</style>
