<script module lang="ts">
	import type { Component } from 'svelte';
	import { BookOpenText, BellRing, type IconProps } from '@lucide/svelte';
	import Button from './ui/button/button.svelte';

	const hLinks: Array<{
		href: string;
		label: string;
		icon: Component<IconProps>;
	}> = [
		{
			href: '/guides',
			label: 'Guides',
			icon: BookOpenText
		},

		{
			href: '/notifications',
			label: 'Notifications',
			icon: BellRing
		}
	];
	export { hLink };
</script>

<header class="flex h-16 w-full items-center justify-end gap-8 border-b px-8 text-sm">
	{#each hLinks as link (link.href)}
		{@render hLink(link)}
	{/each}
</header>

{#snippet hLink(link: (typeof hLinks)[0])}
	<a title={link.label} href={link.href}>
		<Button variant="ghost" size="icon">
			<link.icon />
		</Button>
	</a>
{/snippet}
