<script lang="ts">
	import AppFooter from '$lib/components/app-footer.svelte';
	import AppLogo from '$lib/components/app-logo.svelte';
	import Button from '$lib/components/ui/button/button.svelte';
	import { Send } from '@lucide/svelte';
</script>

<div class="flex h-full flex-col items-center justify-center gap-1 p-6">
	<h1 class="text-2xl font-bold">Welcome to{' '}<AppLogo isNameOnly={true} />!</h1>
	<p class="text-center text-sm">
		Your privacy-preserving fin-health app (with AI&trade; and stuff!)
	</p>
	<div class="mt-2 flex items-center gap-8 p-4">
		<a href="/login">
			<Button variant="ghost" size="sm">Login</Button>
		</a>
		<a href="/sign-up"
			><Button size="sm">
				<Send />
				Sign up
			</Button>
		</a>
	</div>
</div>
<AppFooter />
