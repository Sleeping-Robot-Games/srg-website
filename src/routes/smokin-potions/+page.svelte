<script>
	import IconArrowLeft from 'lucide-svelte/icons/arrow-left';
	import IconUsers from 'lucide-svelte/icons/users';
	import IconMonitor from 'lucide-svelte/icons/monitor';
	import IconGhost from 'lucide-svelte/icons/ghost';
	import IconSwords from 'lucide-svelte/icons/swords';
	import IconFlame from 'lucide-svelte/icons/flame';
	import IconWandSparkles from 'lucide-svelte/icons/wand-sparkles';
	import IconShirt from 'lucide-svelte/icons/shirt';
	import IconMap from 'lucide-svelte/icons/map';
	import IconZap from 'lucide-svelte/icons/zap';
	import IconExternalLink from 'lucide-svelte/icons/external-link';
	import IconMail from 'lucide-svelte/icons/mail';

	const badges = [
		{ icon: IconUsers, label: '2-4 Players' },
		{ icon: IconMonitor, label: 'Local Multiplayer + Remote Play' },
		{ icon: IconGhost, label: 'Come Back as a Ghost' }
	];

	const features = [
		{
			icon: IconUsers,
			title: 'Local multiplayer mayhem',
			body: '2-4 players battle it out on one screen, or play online with friends via Steam Remote Play Together.'
		},
		{
			icon: IconFlame,
			title: 'Explosive potion combat',
			body: 'Mix and match elemental potions into bombs, then lob them across the arena to blast your rivals.'
		},
		{
			icon: IconSwords,
			title: 'Bomberman 64-inspired',
			body: 'Fast, chaotic battle-mode action inspired by the arena brawlers that started it all.'
		},
		{
			icon: IconWandSparkles,
			title: 'Unique magical affinities',
			body: 'Every wizard has their own affinity, changing how they interact with the elements on the field.'
		},
		{
			icon: IconMap,
			title: 'Battle across unique arenas',
			body: "Fight through a wizard's tower, a rock garden, a casino, and more, each with its own hazards and sudden-death mechanics."
		},
		{
			icon: IconZap,
			title: 'Grab wild pickups',
			body: 'Snag random scrolls mid-match for wild effects like Humungo potions, a Potion Party, or a clutch revive.'
		},
		{
			icon: IconGhost,
			title: 'Haunt as a ghost',
			body: "Defeat doesn't end the match for you. Come back as a ghost to sabotage rivals and claw for a second chance."
		},
		{
			icon: IconShirt,
			title: 'Customize your wizard',
			body: 'Unlock hats, hairstyles, and colors to make your wizard yours before the next match starts.'
		}
	];

	const elements = [
		{ name: 'Fire', icon: '/images/smokin-potions/potions/fire.png', color: 'var(--sp-fire)' },
		{ name: 'Ice', icon: '/images/smokin-potions/potions/ice.png', color: 'var(--sp-ice)' },
		{ name: 'Earth', icon: '/images/smokin-potions/potions/earth.png', color: 'var(--sp-earth)' },
		{
			name: 'Arcane',
			icon: '/images/smokin-potions/potions/arcane.png',
			color: 'var(--sp-arcane)'
		}
	];

	const combos = [
		{ label: 'Fire + Ice', icon: '/images/smokin-potions/potions/fire_ice.png' },
		{ label: 'Fire + Earth', icon: '/images/smokin-potions/potions/fire_earth.png' },
		{ label: 'Fire + Arcane', icon: '/images/smokin-potions/potions/fire_arcane.png' },
		{ label: 'Ice + Earth', icon: '/images/smokin-potions/potions/ice_earth.png' },
		{ label: 'Ice + Arcane', icon: '/images/smokin-potions/potions/ice_arcane.png' },
		{ label: 'Earth + Arcane', icon: '/images/smokin-potions/potions/earth_arcane.png' }
	];

	const screenshots = [
		{
			src: '/images/smokin-potions/screenshots/arena-elements.webp',
			alt: 'Wizards battling with fire, ice, and earth potion clouds in the dungeon arena'
		},
		{
			src: '/images/smokin-potions/screenshots/arena-library.webp',
			alt: 'A four-way battle in the library arena, surrounded by elemental potion crates'
		},
		{
			src: '/images/smokin-potions/screenshots/overtime.webp',
			alt: 'An OVERTIME banner during a tense final showdown on the rocky arena'
		},
		{
			src: '/images/smokin-potions/screenshots/winner.webp',
			alt: 'Post-match results screen crowning the winning wizard'
		},
		{
			src: '/images/smokin-potions/screenshots/character-select.webp',
			alt: 'Character customization screen with hats, hair, and color options'
		}
	];
</script>

<svelte:head>
	<title>Smokin Potions | Sleeping Robot Games</title>
	<meta
		name="description"
		content="Explosive local-multiplayer potion battles for 2-4 players. Mix elements, craft bombs, and haunt your rivals as a ghost."
	/>
	<meta property="og:type" content="website" />
	<meta property="og:title" content="Smokin Potions" />
	<meta
		property="og:description"
		content="Explosive local-multiplayer potion battles for 2-4 players. Mix elements, craft bombs, and haunt your rivals as a ghost."
	/>
	<meta
		property="og:image"
		content="https://sleepingrobotgames.com/images/smokin-potions-capsule.png"
	/>
</svelte:head>

<div class="sp-page">
	<nav class="sp-nav">
		<a href="/" class="sp-nav-back">
			<IconArrowLeft class="h-4 w-4" />
			<span>Sleeping Robot Games</span>
		</a>
		<a
			href="https://store.steampowered.com/app/3433720/Smokin_Potions/"
			target="_blank"
			class="sp-nav-badge"
		>
			Out now on Steam
			<IconExternalLink class="h-3.5 w-3.5" />
		</a>
	</nav>

	<header class="sp-hero">
		<img src="/images/smokin-potions-capsule.png" alt="" class="sp-hero-bg" aria-hidden="true" />
		<div class="sp-hero-scrim"></div>
		<div class="sp-hero-content">
			<p class="sp-hero-tagline">
				Chaos reigns as up to 4 friends battle in a magical, explosive local-multiplayer showdown.
			</p>
			<div class="sp-hero-ctas">
				<a
					href="https://store.steampowered.com/app/3433720/Smokin_Potions/"
					target="_blank"
					class="sp-btn sp-btn-primary"
				>
					Play on Steam
				</a>
				<a
					href="https://drive.google.com/drive/folders/1T6g3YvxNZPVg05GcS8T8fUUWRDiH3b3c"
					target="_blank"
					class="sp-btn sp-btn-ghost"
				>
					Press Kit
				</a>
			</div>
			<div class="sp-badge-row">
				{#each badges as b}
					<span class="sp-badge">
						<b.icon class="h-3.5 w-3.5" />
						{b.label}
					</span>
				{/each}
			</div>
		</div>
	</header>

	<main>
		<section class="sp-section sp-about">
			<p class="sp-about-text">
				Create your wizard, choose your magical affinity, mix elements, and craft explosive potion
				bombs to dominate the arena. Even in defeat, haunt and sabotage rivals as a ghost, seizing a
				second chance at glory.
			</p>
		</section>

		<section class="sp-section sp-trailer-section">
			<h2 class="sp-h2">Launch trailer</h2>
			<div class="sp-trailer">
				<!-- svelte-ignore a11y_missing_attribute -->
				<iframe
					src="https://www.youtube.com/embed/z61VGaWREvg?si=ha_4ulGgZbQPwqWW&playsinline=1&controls=0&showinfo=0&modestbranding=1&iv_load_policy=3&fs=1&hl=en&autohide=1&widgetid=1&rel=0"
					frameborder="0"
					allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
					allowfullscreen
					class="sp-trailer-iframe"
				></iframe>
			</div>
		</section>

		<section class="sp-section">
			<h2 class="sp-h2">Key Features</h2>
			<div class="sp-features">
				{#each features as f}
					<div class="sp-feature-card">
						<div class="sp-feature-icon">
							<f.icon class="h-6 w-6" />
						</div>
						<h3 class="sp-feature-title">{f.title}</h3>
						<p class="sp-feature-body">{f.body}</p>
					</div>
				{/each}
			</div>
		</section>

		<section class="sp-section sp-elements-section">
			<h2 class="sp-h2">Mix your magic</h2>
			<p class="sp-elements-sub">
				Four base elements, real potions straight from the game. Combine any two for a whole new
				blast.
			</p>
			<div class="sp-elements-row">
				{#each elements as el}
					<div class="sp-element-chip" style="--el-color: {el.color};">
						<div class="sp-element-icon">
							<img src={el.icon} alt="{el.name} potion" />
						</div>
						<span class="sp-element-name">{el.name}</span>
					</div>
				{/each}
			</div>
			<div class="sp-combo-row">
				{#each combos as c}
					<div class="sp-combo-chip">
						<div class="sp-combo-icon">
							<img src={c.icon} alt="{c.label} combo potion" />
						</div>
						<span class="sp-combo-name">{c.label}</span>
					</div>
				{/each}
			</div>
		</section>

		<section class="sp-section sp-gallery-section">
			<h2 class="sp-h2">A peek inside</h2>
			<div class="sp-gallery">
				{#each screenshots as s}
					<div class="sp-gallery-item">
						<img src={s.src} alt={s.alt} loading="lazy" />
					</div>
				{/each}
			</div>
		</section>

		<section class="sp-section sp-cta-section">
			<h2 class="sp-h2">Ready to battle?</h2>
			<p class="sp-cta-sub">Available now on Windows, SteamOS, macOS, and Linux.</p>
			<div class="sp-hero-ctas">
				<a
					href="https://store.steampowered.com/app/3433720/Smokin_Potions/"
					target="_blank"
					class="sp-btn sp-btn-primary"
				>
					Play on Steam
				</a>
				<a href="mailto:support@sleepingrobotgames.com" class="sp-btn sp-btn-ghost">
					<IconMail class="h-4 w-4" />
					Email us
				</a>
			</div>
		</section>
	</main>

	<footer class="sp-footer">
		<p>
			<a href="/" class="sp-footer-link">← Back to Sleeping Robot Games</a>
		</p>
		<p>
			Also check out our other game, <a href="/mini-me-mao" class="sp-footer-link">Mini Me-Mao</a>
		</p>
		<p>
			Follow on <a
				href="https://bsky.app/profile/bronskydev.bsky.social"
				target="_blank"
				class="sp-footer-link">Bluesky</a
			>
			· Visit our
			<a href="https://linktr.ee/SleepingRobotGames" target="_blank" class="sp-footer-link"
				>Linktree</a
			> for more links!
		</p>
		<p class="sp-footer-copyright">
			© 2026 Sleeping Robot Games · Pixel font m6x11 by Daniel Linssen
		</p>
	</footer>
</div>

<style>
	:global(html),
	:global(body) {
		margin: 0;
		background: #131c2e;
	}

	@font-face {
		font-family: 'm6x11';
		src: url('/fonts/m6x11.ttf') format('truetype');
		font-display: swap;
	}

	.sp-page {
		--brand-bg: #131c2e;
		--brand-panel: #1f2c42;
		--brand-accent: #f5a623;
		--brand-accent-soft: #ffcf7a;
		--brand-cream: #fdf3e3;
		--brand-cream-dim: #c3cbda;
		--brand-gold: #f5a623;
		--sp-fire: #ff6a3d;
		--sp-ice: #5fd2e8;
		--sp-earth: #c98a4b;
		--sp-arcane: #ff4fd8;

		background: var(--brand-bg);
		color: var(--brand-cream);
		font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
		line-height: 1.6;
		overflow-x: hidden;
	}

	.sp-h2,
	.sp-hero-tagline,
	.sp-nav-back span,
	.sp-nav-badge,
	:global(.sp-btn) {
		font-family: 'Baloo 2 Variable', sans-serif;
	}

	/* Nav */
	.sp-nav {
		position: sticky;
		top: 0;
		z-index: 20;
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 1rem;
		padding: 0.85rem 1.25rem;
		background: rgba(32, 19, 32, 0.75);
		backdrop-filter: blur(8px);
		border-bottom: 1px solid rgba(255, 255, 255, 0.08);
	}

	.sp-nav-back {
		display: flex;
		align-items: center;
		gap: 0.4rem;
		color: var(--brand-cream);
		font-weight: 600;
		font-size: 0.95rem;
		text-decoration: none;
		opacity: 0.9;
	}
	.sp-nav-back:hover {
		opacity: 1;
		color: var(--brand-accent-soft);
	}

	.sp-nav-badge {
		display: inline-flex;
		align-items: center;
		gap: 0.4rem;
		font-size: 0.75rem;
		font-weight: 700;
		letter-spacing: 0.02em;
		color: var(--brand-bg);
		background: var(--brand-gold);
		padding: 0.35rem 0.7rem;
		border-radius: 999px;
		white-space: nowrap;
		text-decoration: none;
		flex-shrink: 0;
	}
	.sp-nav-badge:hover {
		background: #ffd685;
	}

	@media (max-width: 480px) {
		.sp-nav {
			padding: 0.65rem 0.85rem;
		}
		.sp-nav-back {
			font-size: 0.8rem;
		}
		.sp-nav-badge {
			font-size: 0.68rem;
			padding: 0.3rem 0.55rem;
		}
	}

	/* Hero */
	.sp-hero {
		position: relative;
		display: flex;
		align-items: flex-end;
		min-height: min(88vh, 780px);
		overflow: hidden;
	}

	.sp-hero-bg {
		position: absolute;
		inset: 0;
		width: 100%;
		height: 100%;
		object-fit: cover;
		object-position: 30% 15%;
	}

	@media (max-width: 640px) {
		.sp-hero {
			min-height: min(52vh, 480px);
		}
	}

	.sp-hero-scrim {
		position: absolute;
		inset: 0;
		background: linear-gradient(
				180deg,
				rgba(19, 28, 46, 0.1) 0%,
				rgba(19, 28, 46, 0.6) 60%,
				rgba(15, 22, 36, 0.95) 100%
			),
			linear-gradient(90deg, rgba(15, 22, 36, 0.55) 0%, rgba(15, 22, 36, 0.1) 55%);
	}

	.sp-hero-content {
		position: relative;
		z-index: 1;
		width: 100%;
		max-width: 900px;
		margin: 0 auto;
		text-align: center;
		padding: 2rem 1.5rem 2.75rem;
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.sp-hero-tagline {
		margin: 0 0 1.25rem;
		font-size: clamp(1.1rem, 2.6vw, 1.6rem);
		font-weight: 700;
		color: var(--brand-cream);
		text-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
	}

	.sp-hero-ctas {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 0.9rem;
	}

	:global(.sp-btn) {
		display: inline-flex;
		align-items: center;
		gap: 0.5rem;
		font-weight: 700;
		font-size: 0.95rem;
		padding: 0.75rem 1.3rem;
		border-radius: 999px;
		text-decoration: none;
		line-height: 1;
		border: 2px solid transparent;
	}

	:global(.sp-btn-primary) {
		background: var(--brand-accent);
		color: #fff;
		box-shadow: 0 6px 18px rgba(255, 63, 174, 0.35);
	}
	:global(a.sp-btn-primary:hover) {
		background: #44a61f;
	}

	:global(.sp-btn-ghost) {
		background: transparent;
		color: var(--brand-cream);
		border-color: rgba(255, 255, 255, 0.35);
	}
	:global(a.sp-btn-ghost:hover) {
		border-color: var(--brand-accent-soft);
		color: var(--brand-accent-soft);
	}

	.sp-badge-row {
		margin-top: 1.75rem;
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 0.6rem;
	}

	.sp-badge {
		display: inline-flex;
		align-items: center;
		gap: 0.4rem;
		font-family: 'm6x11', 'Baloo 2 Variable', sans-serif;
		font-size: 0.95rem;
		letter-spacing: 0.02em;
		color: var(--brand-cream-dim);
		background: rgba(255, 255, 255, 0.06);
		border: 1px solid rgba(255, 255, 255, 0.1);
		padding: 0.4rem 0.8rem;
		border-radius: 999px;
	}

	/* Sections */
	.sp-section {
		max-width: 1100px;
		margin: 0 auto;
		padding: 3rem 1.5rem;
	}

	.sp-h2 {
		font-size: clamp(1.6rem, 3vw, 2.1rem);
		font-weight: 700;
		text-align: center;
		margin: 0 0 0.5rem;
		color: var(--brand-cream);
	}

	.sp-about {
		text-align: center;
	}
	.sp-about-text {
		max-width: 62ch;
		margin: 0 auto;
		font-size: clamp(1.05rem, 2vw, 1.25rem);
	}

	/* Features */
	.sp-features {
		margin-top: 2rem;
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
		gap: 1.25rem;
	}

	.sp-feature-card {
		background: var(--brand-panel);
		border: 1px solid rgba(255, 255, 255, 0.06);
		border-radius: 20px;
		padding: 1.5rem;
	}

	.sp-feature-icon {
		display: inline-flex;
		align-items: center;
		justify-content: center;
		width: 44px;
		height: 44px;
		border-radius: 14px;
		background: rgba(255, 106, 61, 0.16);
		color: #ffb08c;
		margin-bottom: 0.9rem;
	}

	.sp-feature-title {
		font-family: 'Baloo 2 Variable', sans-serif;
		font-size: 1.15rem;
		font-weight: 700;
		margin: 0 0 0.4rem;
	}

	.sp-feature-body {
		font-size: 0.95rem;
		color: var(--brand-cream-dim);
		margin: 0;
	}

	/* Elements */
	.sp-elements-section {
		text-align: center;
	}

	.sp-elements-sub {
		max-width: 56ch;
		margin: 0 auto;
		color: var(--brand-cream-dim);
	}

	.sp-elements-row {
		margin-top: 2rem;
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 1.5rem;
	}

	.sp-element-chip {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 0.6rem;
	}

	.sp-element-icon {
		background: var(--brand-panel);
		border: 2px solid var(--el-color);
		box-shadow: 0 0 16px -2px var(--el-color);
		border-radius: 16px;
		padding: 0.8rem 1rem;
	}

	.sp-element-icon img {
		image-rendering: pixelated;
		height: 48px;
		width: auto;
		display: block;
	}

	.sp-element-name {
		font-family: 'm6x11', 'Baloo 2 Variable', sans-serif;
		font-size: 1.1rem;
		letter-spacing: 0.02em;
		color: var(--el-color);
	}

	.sp-combo-row {
		margin-top: 2.5rem;
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 1.1rem;
	}

	.sp-combo-chip {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 0.5rem;
	}

	.sp-combo-icon {
		background: var(--brand-panel);
		border: 1px solid rgba(255, 255, 255, 0.1);
		border-radius: 14px;
		padding: 0.6rem 0.8rem;
	}

	.sp-combo-icon img {
		image-rendering: pixelated;
		height: 36px;
		width: auto;
		display: block;
	}

	.sp-combo-name {
		font-family: 'm6x11', 'Baloo 2 Variable', sans-serif;
		font-size: 0.85rem;
		color: var(--brand-cream-dim);
	}

	/* Gallery */
	.sp-gallery-section {
		text-align: center;
	}

	.sp-gallery {
		margin-top: 1.75rem;
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
		gap: 1rem;
	}

	.sp-gallery-item {
		border-radius: 16px;
		overflow: hidden;
		box-shadow: 0 10px 30px rgba(0, 0, 0, 0.35);
	}

	.sp-gallery-item img {
		display: block;
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

	/* Trailer */
	.sp-trailer-section {
		text-align: center;
	}

	.sp-trailer {
		margin: 1.75rem auto 0;
		max-width: 800px;
		aspect-ratio: 16 / 9;
		border-radius: 16px;
		overflow: hidden;
		box-shadow: 0 20px 50px rgba(0, 0, 0, 0.4);
	}

	.sp-trailer-iframe {
		width: 100%;
		height: 100%;
		border: none;
	}

	/* CTA */
	.sp-cta-section {
		text-align: center;
		background: linear-gradient(180deg, transparent, rgba(255, 106, 61, 0.08));
		border-radius: 28px;
	}

	.sp-cta-sub {
		max-width: 50ch;
		margin: 0 auto 1.75rem;
		color: var(--brand-cream-dim);
	}

	/* Footer */
	.sp-footer {
		text-align: center;
		padding: 2.5rem 1.5rem 3rem;
		color: var(--brand-cream-dim);
		font-size: 0.9rem;
	}

	.sp-footer-link {
		color: var(--brand-accent-soft);
		text-decoration: none;
	}
	.sp-footer-link:hover {
		text-decoration: underline;
	}

	.sp-footer-copyright {
		margin-top: 1rem;
		opacity: 0.7;
		font-size: 0.8rem;
	}
</style>
