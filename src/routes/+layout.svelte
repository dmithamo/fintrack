<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';
	import { ModeWatcher } from 'mode-watcher';
	import AppThemeToggler from '$lib/components/app-theme-toggler.svelte';
	let { children } = $props();
</script>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>

<ModeWatcher />
<AppThemeToggler />

<main class="h-screen w-full">
	{@render children()}
</main>
