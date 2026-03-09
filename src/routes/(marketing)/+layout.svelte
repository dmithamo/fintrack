<script lang="ts">
	import AppLogo from '$lib/components/app-logo.svelte';

	import { hLink } from '$lib/components/app-header.svelte';
	import { Info } from '@lucide/svelte';
	let { children } = $props();
</script>

<section class="flex h-full w-full flex-col">
	<header class="flex h-16 w-full items-center justify-between border-b px-3">
		<a href="/">
			<AppLogo />
		</a>
		<div>
			{@render hLink({
				label: 'About',
				icon: Info,
				href: '/about'
			})}
		</div>
	</header>

	<div class="flex-1 p-3">
		{@render children()}
	</div>
</section>
