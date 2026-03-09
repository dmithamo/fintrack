<script lang="ts">
	import * as Sidebar from '$lib/components/ui/sidebar/index';
	import AppSidebar from '$lib/components/app-sidebar.svelte';
	import AppHeader from '$lib/components/app-header.svelte';
	let { children } = $props();
</script>

<Sidebar.Provider>
	<AppSidebar />
	<section class="w-full">
		<AppHeader />
		<section class="p-3">
			{@render children()}
		</section>
	</section>
</Sidebar.Provider>
