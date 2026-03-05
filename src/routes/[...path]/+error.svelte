<script lang="ts">
	import { page } from '$app/state';
	import AppFooter from '$lib/components/app-footer.svelte';
</script>

<section class="flex h-full w-full flex-col items-center justify-center gap-2">
	<h1 class="text-2xl text-shadow-destructive">Error</h1>
	<p class="text-destructive">{page.error?.message ?? 'Something went wrong'}</p>
</section>
<AppFooter />
