<script>
	import IconMail from 'lucide-svelte/icons/mail';
</script>

<svelte:head>
	<title>SRG - Home</title>
</svelte:head>

<!-- For best results, preview this in either the full-width or full-screen preview modes. -->

<div class="grid grid-rows-[auto_1fr_auto]">
	<!-- Header -->
	<header class="flex items-center justify-center bg-gray-700 p-4">
		<img src="/images/srglogo.png" alt="Sleeping Robot Games logo" class="mr-4 h-12" />
		<span class="text-3xl font-bold text-white" style="font-family: 'Orbitron Variable', sans-serif"
			>Sleeping Robot Games</span
		>
	</header>
	<!-- Page -->
	<div class="container mx-auto grid grid-cols-1 xl:grid-cols-[200px_minmax(0px,_1fr)_200px]">
		<!-- Sidebar (Left) -->
		<!-- NOTE: hidden in smaller screen sizes -->
		<aside class="sticky top-0 col-span-1 hidden xl:block">
			<img
				src="/images/Steam_Broadcast_Panel_1_big.png"
				class="h-full w-auto object-cover"
				alt="Smokin Potions promo art (Wizard running with Potion overhead)"
			/>
		</aside>
		<!-- Main -->
		<main class="col-span-1 space-y-4 bg-gray-800 p-4 text-white">
			<div class="min- space-y-2 bg-gray-900 p-4">
				<h1 class="text-5xl font-bold">Smokin Potions</h1>
				<p class="text-lg">
					PressKit: <a
						href="https://drive.google.com/drive/folders/1T6g3YvxNZPVg05GcS8T8fUUWRDiH3b3c"
						class="text-blue-400 hover:underline"
						target="_blank">Download</a
					>
				</p>
				<p class="text-lg">
					Steam: <a
						href="https://store.steampowered.com/app/3433720/Smokin_Potions/"
						class="text-blue-400 hover:underline"
						target="_blank">Store Page</a
					>
				</p>
				<p class="text-lg">
					Demo Available: <a
						href="https://store.steampowered.com/app/3498340/Smokin_Potions_Demo/"
						class="text-blue-400 hover:underline"
						target="_blank">Download</a
					>
				</p>
				<p class="text-lg">Platforms: Windows, SteamOS, MacOS, Linux</p>
				<p class="text-lg">Highlights:</p>
				<ul class="list-disc pl-6">
					<li>Local-multiplayer for 2-4 players, online via Steam Remote Play Together</li>
					<li>Explosive pvp combat with mix-and-match elemental potion bombs</li>
					<li>Inspired by games like <b>Bomberman 64</b> battle mode</li>
					<li>
						Each wizard has a unique magical affinity, changing how they interact with the elements
					</li>
					<li>Haunt and sabotage rivals as a ghost, seeking a second chance at victory</li>
				</ul>
				<p class="text-lg">Short Description:</p>
				<p>
					Chaos reigns as up to 4 friends battle in a magical, explosive local-multiplayer showdown.
					Create your wizard, choose your magical affinity, mix elements, and craft explosive potion
					bombs to dominate the arena. Even in defeat, haunt and sabotage rivals as a ghost, seizing
					a second chance at glory.
				</p>
				<div class="mx-auto aspect-video max-w-[800px]">
					<!-- svelte-ignore a11y_missing_attribute -->
					<iframe
						src="https://www.youtube.com/embed/yh45XaDy0eA?si=ocQCSZOG-4Ph30Cv&playsinline=1&controls=0&showinfo=0&modestbranding=1&iv_load_policy=3&fs=1&hl=en&autohide=1&widgetid=1&rel=0"
						frameborder="0"
						allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
						allowfullscreen
						class="h-full w-full"
					></iframe>
				</div>
				<div class="mx-auto max-w-[800px] pt-4">
					<a
						href="mailto:support@sleepingrobotgames.com"
						class="btn flex w-full items-center justify-center gap-2 preset-outlined-primary-500"
					>
						<IconMail class="btn-icon" />
						<span>Email Us</span>
					</a>
				</div>
			</div>
		</main>
		<!-- Sidebar (Right) -->
		<!-- NOTE: hidden in smaller screen sizes -->
		<aside class="sticky top-0 col-span-1 hidden xl:block">
			<img
				src="/images/Steam_Broadcast_Panel_2_big.png"
				class="h-full w-auto object-cover"
				alt="Smokin Potions promo art (Wizard placing sneaky Potion)"
			/>
		</aside>
	</div>
	<!-- Footer -->
	<footer class="bg-gray-700 p-4 text-center text-white">
		<p>
			Follow on <a
				href="https://bsky.app/profile/bronskydev.bsky.social"
				class="text-blue-400 hover:underline"
				target="_blank">Bluesky</a
			>
		</p>
		<p>© 2025 Sleeping Robot Games</p>
	</footer>
</div>
