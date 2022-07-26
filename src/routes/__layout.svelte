<script>
	import { session } from '$app/stores';
	import { supabaseClient } from '$lib/sb';
	import { SupaAuthHelper } from '@supabase/auth-helpers-svelte';
</script>

<svelte:head>
	<title>Email and Password Demo - Supabase Auth Helpers</title>
</svelte:head>

<SupaAuthHelper {supabaseClient} {session}>
	<main>
		<div>
			<h2>
				<a href="/">Supabase Auth Helpers Demo</a>
			</h2>

			<slot />

			<div>
				{#if $session?.user?.id}
					<a href="/api/auth/logout">Sign out</a>
				{/if}
			</div>
		</div>
	</main>
</SupaAuthHelper>
