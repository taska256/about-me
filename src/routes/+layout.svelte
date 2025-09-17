<script>
	import "../app.css";
	import Icon from "@iconify/svelte";
	import { GITHUB_USER, NAME, SITE_DOMAIN } from "../lib/constant";
	const avatarUrl = `https://github.com/${GITHUB_USER}.png?size=240`;
</script>

<svelte:head>
	<title>{NAME}</title>
</svelte:head>

<header
	class="sticky top-0 z-50 border-b-2 border-stone-800 bg-yellow-50/80 backdrop-blur"
>
	<nav class="mx-auto flex max-w-5xl items-center justify-between px-4 py-3">
		<div class="flex items-center gap-3">
			<a
				href={`https://github.com/${GITHUB_USER}`}
				target="_blank"
				rel="noopener noreferrer"
				aria-label="GitHub"
				class="hover:opacity-80"
			>
				<Icon
					icon="tabler:brand-github"
					class="size-8 text-stone-800"
					aria-hidden="true"
				/>
			</a>
			<span class="font-semibold text-stone-800">{SITE_DOMAIN}</span>
		</div>
	</nav>
</header>

<main class="mx-auto max-w-5xl px-4">
	<slot />
</main>

<footer class="mt-16 bg-yellow-50 w-full">
	<div class="mx-auto max-w-5xl px-4 py-5 text-sm text-stone-600 text-center">
		© 2025 {NAME}
	</div>
</footer>
