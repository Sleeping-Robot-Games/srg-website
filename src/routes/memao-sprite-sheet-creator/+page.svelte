<script>
	import IconArrowLeft from 'lucide-svelte/icons/arrow-left';
	import IconExternalLink from 'lucide-svelte/icons/external-link';
	import IconMail from 'lucide-svelte/icons/mail';
	import IconInfinity from 'lucide-svelte/icons/infinity';
	import IconMonitor from 'lucide-svelte/icons/monitor';
	import IconPalette from 'lucide-svelte/icons/palette';
	import IconDices from 'lucide-svelte/icons/dices';
	import IconImages from 'lucide-svelte/icons/images';
	import IconSave from 'lucide-svelte/icons/save';
	import IconScroll from 'lucide-svelte/icons/scroll';
	import IconRefreshCw from 'lucide-svelte/icons/refresh-cw';
	import IconShapes from 'lucide-svelte/icons/shapes';
	import IconChevronLeft from 'lucide-svelte/icons/chevron-left';
	import IconChevronRight from 'lucide-svelte/icons/chevron-right';

	const ITCH_URL = 'https://sleeping-robot-games.itch.io/sprite-sheet-creator';

	let carouselEl;
	function scrollCarousel(dir) {
		if (!carouselEl) return;
		const maxScroll = carouselEl.scrollWidth - carouselEl.clientWidth;
		const atEnd = carouselEl.scrollLeft >= maxScroll - 4;
		const atStart = carouselEl.scrollLeft <= 4;
		if (dir > 0 && atEnd) {
			carouselEl.scrollTo({ left: 0, behavior: 'smooth' });
			return;
		}
		if (dir < 0 && atStart) {
			carouselEl.scrollTo({ left: maxScroll, behavior: 'smooth' });
			return;
		}
		const amount = carouselEl.clientWidth * 0.8 * dir;
		carouselEl.scrollBy({ left: amount, behavior: 'smooth' });
	}

	const badges = [
		{ label: '$12.99 or more' },
		{ label: 'Windows, macOS, Linux, HTML5' },
		{ label: '135 Trillion+ Combinations' }
	];

	const features = [
		{
			icon: IconShapes,
			title: 'No drawing required',
			body: 'Mix and match a paper-doll system of hair, faces, clothes, and more. Built-in animated pixel art means no art skills needed.'
		},
		{
			icon: IconInfinity,
			title: '135 trillion combinations',
			body: 'Layer up hairstyles, outfits, and accessories for a cast of characters that never look the same twice.'
		},
		{
			icon: IconImages,
			title: 'Export full sprite sheets',
			body: 'Ready-to-import PNGs for Unity, Godot, GameMaker, RPG Maker, and anywhere else your project lives.'
		},
		{
			icon: IconScroll,
			title: 'TTRPG tokens and portraits',
			body: 'Export top-down tokens and portraits for Roll20, Foundry VTT, and other tabletop platforms.'
		},
		{
			icon: IconDices,
			title: 'Real-time animation preview',
			body: 'Watch Idle, Walk, Run, Strike, Chop, and more play out live as you build your character.'
		},
		{
			icon: IconPalette,
			title: 'Custom color palettes',
			body: 'Pick from built-in palettes or bring your own colors to match your project.'
		},
		{
			icon: IconSave,
			title: 'Save and re-edit',
			body: 'Save characters to come back to later. Nothing is locked in once you export.'
		},
		{
			icon: IconRefreshCw,
			title: 'Lifetime updates',
			body: 'A one-time purchase gets you every future update and content expansion, free.'
		}
	];

	const animations = [
		{ name: 'Idle', src: '/images/sprite-creator/animations/idle.gif' },
		{ name: 'Walk', src: '/images/sprite-creator/animations/walk.gif' },
		{ name: 'Run', src: '/images/sprite-creator/animations/run.gif' },
		{ name: 'Reap', src: '/images/sprite-creator/animations/reap.gif' },
		{ name: 'Chop', src: '/images/sprite-creator/animations/chop.gif' },
		{ name: 'Water', src: '/images/sprite-creator/animations/water.gif' },
		{ name: 'Strike', src: '/images/sprite-creator/animations/strike.gif' },
		{ name: 'Pick Up', src: '/images/sprite-creator/animations/pickup.gif' },
		{ name: 'Seed', src: '/images/sprite-creator/animations/seed.gif' },
		{ name: 'Slash', src: '/images/sprite-creator/animations/slash.gif' },
		{ name: 'Hurt', src: '/images/sprite-creator/animations/hurt.gif' },
		{ name: 'Downed', src: '/images/sprite-creator/animations/downed.gif' },
		{ name: 'Death', src: '/images/sprite-creator/animations/death.gif' }
	];
</script>

<svelte:head>
	<title>Memao Sprite Sheet Creator | Sleeping Robot Games</title>
	<meta
		name="description"
		content="Design ready-to-use pixel characters in minutes and export them as fully animated sprite sheets for your games. No drawing required."
	/>
	<meta property="og:type" content="website" />
	<meta property="og:title" content="Memao Sprite Sheet Creator" />
	<meta
		property="og:description"
		content="Design ready-to-use pixel characters in minutes and export them as fully animated sprite sheets for your games. No drawing required."
	/>
	<meta property="og:image" content="https://sleepingrobotgames.com/images/tool_preview.gif" />
</svelte:head>

<div class="tc-page">
	<nav class="tc-nav">
		<a href="/" class="tc-nav-back">
			<IconArrowLeft class="h-4 w-4" />
			<span>Sleeping Robot Games</span>
		</a>
		<a href={ITCH_URL} target="_blank" class="tc-nav-badge">
			Get it on itch.io
			<IconExternalLink class="h-3.5 w-3.5" />
		</a>
	</nav>

	<header class="tc-hero">
		<img
			src="/images/memao-sprite-sheet-creator-capsule.png"
			alt=""
			class="tc-hero-bg"
			aria-hidden="true"
		/>
		<div class="tc-hero-scrim"></div>
		<div class="tc-hero-content">
			<p class="tc-hero-tagline">
				Design ready-to-use pixel characters in minutes and export them as fully animated sprite
				sheets. No drawing required.
			</p>
			<div class="tc-hero-ctas">
				<a href={ITCH_URL} target="_blank" class="tc-btn tc-btn-primary"> Get it on itch.io </a>
				<!-- <a href="#gallery" class="tc-btn tc-btn-ghost"> Demo Video </a> -->
			</div>
			<div class="tc-badge-row">
				{#each badges as b}
					<span class="tc-badge">{b.label}</span>
				{/each}
			</div>
		</div>
	</header>

	<main>
		<section class="tc-section tc-about">
			<p class="tc-about-text">
				A tool for designing and customizing 2D pixel art characters using a paper-doll system, then
				exporting them as sprite sheets, no drawing skills required. Built for game developers and
				tabletop game masters alike.
			</p>
		</section>

		<!-- <section class="tc-section tc-preview-section"> -->
		<div class="tc-preview">
			<img
				src="/images/sprite-creator/idle-memao-characters.gif"
				alt="Five character sprites walking forward"
			/>
		</div>
		<!-- </section> -->

		<section class="tc-section tc-trailer-section" id="gallery">
			<h2 class="tc-h2">Demo Video</h2>
			<div class="tc-trailer">
				<!-- svelte-ignore a11y_missing_attribute -->
				<iframe
					src="https://www.youtube.com/embed/7v6MCRCsz9g"
					frameborder="0"
					allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
					allowfullscreen
					class="tc-trailer-iframe"
				></iframe>
			</div>
		</section>

		<div class="tc-preview">
			<img
				src="/images/sprite-creator/walking-memao-characters.gif"
				alt="Five character sprites walking forward"
			/>
		</div>

		<section class="tc-section">
			<h2 class="tc-h2">Key Features</h2>
			<div class="tc-features">
				{#each features as f}
					<div class="tc-feature-card">
						<div class="tc-feature-icon">
							<f.icon class="h-6 w-6" />
						</div>
						<h3 class="tc-feature-title">{f.title}</h3>
						<p class="tc-feature-body">{f.body}</p>
					</div>
				{/each}
			</div>
		</section>

		<section class="tc-section tc-gallery-section">
			<h2 class="tc-h2">Built-in animations</h2>
			<p class="tc-gallery-sub">
				Ready-made animations exported straight from the tool, on a character built entirely from
				its paper-doll parts.
			</p>
			<div class="tc-carousel-wrap">
				<button
					type="button"
					class="tc-carousel-btn tc-carousel-btn-prev"
					aria-label="Scroll to previous animation"
					onclick={() => scrollCarousel(-1)}
				>
					<IconChevronLeft class="h-5 w-5" />
				</button>
				<div class="tc-gallery" bind:this={carouselEl}>
					{#each animations as a}
						<div class="tc-gallery-item">
							<img src={a.src} alt="{a.name} animation preview" />
							<span class="tc-gallery-name">{a.name}</span>
						</div>
					{/each}
				</div>
				<button
					type="button"
					class="tc-carousel-btn tc-carousel-btn-next"
					aria-label="Scroll to next animation"
					onclick={() => scrollCarousel(1)}
				>
					<IconChevronRight class="h-5 w-5" />
				</button>
			</div>
		</section>

		<section class="tc-section tc-cta-section">
			<h2 class="tc-h2">Build your cast</h2>
			<p class="tc-cta-sub">
				One-time purchase, lifetime access to every future update and content expansion.
			</p>
			<div class="tc-hero-ctas">
				<a href={ITCH_URL} target="_blank" class="tc-btn tc-btn-primary"> Get it on itch.io </a>
				<a href="mailto:support@sleepingrobotgames.com" class="tc-btn tc-btn-ghost">
					<IconMail class="h-4 w-4" />
					Email us
				</a>
			</div>
		</section>
	</main>

	<footer class="tc-footer">
		<p>
			<a href="/" class="tc-footer-link">← Back to Sleeping Robot Games</a>
		</p>
		<p>
			Also check out our games, <a href="/mini-me-mao" class="tc-footer-link">Mini Me-Mao</a>
			and <a href="/smokin-potions" class="tc-footer-link">Smokin Potions</a>
		</p>
		<p>
			Follow on <a
				href="https://bsky.app/profile/bronskydev.bsky.social"
				target="_blank"
				class="tc-footer-link">Bluesky</a
			>
			· Visit our
			<a href="https://linktr.ee/SleepingRobotGames" target="_blank" class="tc-footer-link"
				>Linktree</a
			> for more links!
		</p>
		<p class="tc-footer-copyright">© 2026 Sleeping Robot Games</p>
	</footer>
</div>

<style>
	:global(html),
	:global(body) {
		margin: 0;
		background: #1a1220;
	}

	.tc-page {
		--brand-bg: #1a1220;
		--brand-panel: #2c2038;
		--brand-pink: #ff3fae;
		--brand-pink-soft: #ffa8dc;
		--brand-teal: #5fd2c4;
		--brand-cream: #fbf1e6;
		--brand-cream-dim: #d3c8d8;

		background: var(--brand-bg);
		color: var(--brand-cream);
		font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
		line-height: 1.6;
		overflow-x: hidden;
	}

	.tc-h2,
	.tc-hero-tagline,
	.tc-nav-back span,
	.tc-nav-badge,
	:global(.tc-btn) {
		font-family: 'Baloo 2 Variable', sans-serif;
	}

	/* Nav */
	.tc-nav {
		position: sticky;
		top: 0;
		z-index: 20;
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 1rem;
		padding: 0.85rem 1.25rem;
		background: rgba(26, 18, 32, 0.75);
		backdrop-filter: blur(8px);
		border-bottom: 1px solid rgba(255, 255, 255, 0.08);
	}

	.tc-nav-back {
		display: flex;
		align-items: center;
		gap: 0.4rem;
		color: var(--brand-cream);
		font-weight: 600;
		font-size: 0.95rem;
		text-decoration: none;
		opacity: 0.9;
	}
	.tc-nav-back:hover {
		opacity: 1;
		color: var(--brand-pink-soft);
	}

	.tc-nav-badge {
		display: inline-flex;
		align-items: center;
		gap: 0.4rem;
		font-size: 0.75rem;
		font-weight: 700;
		letter-spacing: 0.02em;
		color: var(--brand-bg);
		background: var(--brand-teal);
		padding: 0.35rem 0.7rem;
		border-radius: 999px;
		white-space: nowrap;
		text-decoration: none;
		flex-shrink: 0;
	}
	.tc-nav-badge:hover {
		background: #7fe0d4;
	}

	@media (max-width: 480px) {
		.tc-nav {
			padding: 0.65rem 0.85rem;
		}
		.tc-nav-back {
			font-size: 0.8rem;
		}
		.tc-nav-badge {
			font-size: 0.68rem;
			padding: 0.3rem 0.55rem;
		}
	}

	/* Hero */
	.tc-hero {
		position: relative;
		display: flex;
		align-items: flex-end;
		min-height: min(88vh, 780px);
		overflow: hidden;
	}

	@media (max-width: 640px) {
		.tc-hero {
			min-height: min(52vh, 480px);
		}
	}

	.tc-hero-bg {
		position: absolute;
		inset: 0;
		width: 100%;
		height: 100%;
		object-fit: cover;
		object-position: 32% 20%;
	}

	.tc-hero-scrim {
		position: absolute;
		inset: 0;
		background: linear-gradient(
				180deg,
				rgba(26, 18, 32, 0.1) 0%,
				rgba(26, 18, 32, 0.6) 60%,
				rgba(20, 14, 26, 0.95) 100%
			),
			linear-gradient(90deg, rgba(20, 14, 26, 0.5) 0%, rgba(20, 14, 26, 0.1) 55%);
	}

	.tc-hero-content {
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

	.tc-hero-tagline {
		margin: 0 0 1.5rem;
		font-size: clamp(1.05rem, 2.4vw, 1.4rem);
		font-weight: 600;
		color: var(--brand-cream);
		max-width: 46ch;
		text-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
	}

	.tc-hero-ctas {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 0.9rem;
	}

	:global(.tc-btn) {
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

	:global(.tc-btn-primary) {
		background: var(--brand-pink);
		color: #fff;
		box-shadow: 0 6px 18px rgba(255, 63, 174, 0.35);
	}
	:global(a.tc-btn-primary:hover) {
		background: #ff5cbb;
	}

	:global(.tc-btn-ghost) {
		background: transparent;
		color: var(--brand-cream);
		border-color: rgba(255, 255, 255, 0.35);
	}
	:global(a.tc-btn-ghost:hover) {
		border-color: var(--brand-pink-soft);
		color: var(--brand-pink-soft);
	}

	.tc-badge-row {
		margin-top: 1.75rem;
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 0.6rem;
	}

	.tc-badge {
		display: inline-flex;
		align-items: center;
		font-size: 0.8rem;
		font-weight: 600;
		color: var(--brand-cream-dim);
		background: rgba(255, 255, 255, 0.06);
		border: 1px solid rgba(255, 255, 255, 0.1);
		padding: 0.4rem 0.8rem;
		border-radius: 999px;
	}

	/* Sections */
	.tc-section {
		max-width: 1100px;
		margin: 0 auto;
		padding: 3rem 1.5rem;
	}

	.tc-h2 {
		font-size: clamp(1.6rem, 3vw, 2.1rem);
		font-weight: 700;
		text-align: center;
		margin: 0 0 0.5rem;
		color: var(--brand-cream);
	}

	.tc-about {
		text-align: center;
	}
	.tc-about-text {
		max-width: 62ch;
		margin: 0 auto;
		font-size: clamp(1.05rem, 2vw, 1.25rem);
	}

	/* Preview */
	.tc-preview-section {
		text-align: center;
	}

	.tc-preview {
		/* border-radius: 20px; */
		overflow: hidden;
		/* box-shadow: 0 20px 50px rgba(0, 0, 0, 0.4); */
		max-width: 480px;
		margin: 0 auto;
	}

	.tc-preview img {
		display: block;
		width: 100%;
		height: auto;
	}

	/* Trailer */
	.tc-trailer-section {
		text-align: center;
	}

	.tc-trailer {
		margin: 1.75rem auto 0;
		max-width: 800px;
		aspect-ratio: 16 / 9;
		border-radius: 16px;
		overflow: hidden;
		box-shadow: 0 20px 50px rgba(0, 0, 0, 0.4);
	}

	.tc-trailer-iframe {
		width: 100%;
		height: 100%;
		border: none;
	}

	/* Features */
	.tc-features {
		margin-top: 2rem;
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
		gap: 1.25rem;
	}

	.tc-feature-card {
		background: var(--brand-panel);
		border: 1px solid rgba(255, 255, 255, 0.06);
		border-radius: 20px;
		padding: 1.5rem;
	}

	.tc-feature-icon {
		display: inline-flex;
		align-items: center;
		justify-content: center;
		width: 44px;
		height: 44px;
		border-radius: 14px;
		background: rgba(255, 63, 174, 0.16);
		color: var(--brand-pink-soft);
		margin-bottom: 0.9rem;
	}

	.tc-feature-title {
		font-family: 'Baloo 2 Variable', sans-serif;
		font-size: 1.15rem;
		font-weight: 700;
		margin: 0 0 0.4rem;
	}

	.tc-feature-body {
		font-size: 0.95rem;
		color: var(--brand-cream-dim);
		margin: 0;
	}

	/* Gallery */
	.tc-gallery-section {
		text-align: center;
	}

	.tc-gallery-sub {
		max-width: 56ch;
		margin: 0 auto;
		color: var(--brand-cream-dim);
	}

	.tc-carousel-wrap {
		position: relative;
		margin-top: 2rem;
		display: flex;
		align-items: center;
		gap: 0.75rem;
	}

	.tc-gallery {
		flex: 1;
		display: flex;
		overflow-x: auto;
		scroll-snap-type: x mandatory;
		gap: 1.25rem;
		padding: 0.25rem 0.25rem 1rem;
		scrollbar-width: none;
	}
	.tc-gallery::-webkit-scrollbar {
		display: none;
	}

	.tc-gallery-item {
		flex: 0 0 auto;
		scroll-snap-align: center;
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 0.6rem;
		background: var(--brand-panel);
		border: 1px solid rgba(255, 255, 255, 0.08);
		border-radius: 16px;
		padding: 0.75rem 1rem 1rem;
	}

	.tc-gallery-item img {
		height: 160px;
		width: auto;
		display: block;
		border-radius: 8px;
	}

	.tc-gallery-name {
		font-family: 'Baloo 2 Variable', sans-serif;
		font-weight: 600;
		font-size: 0.9rem;
		color: var(--brand-cream-dim);
	}

	.tc-carousel-btn {
		flex-shrink: 0;
		display: flex;
		align-items: center;
		justify-content: center;
		width: 40px;
		height: 40px;
		border-radius: 999px;
		background: var(--brand-panel);
		border: 1px solid rgba(255, 255, 255, 0.12);
		color: var(--brand-cream);
		cursor: pointer;
	}
	.tc-carousel-btn:hover {
		border-color: var(--brand-pink-soft);
		color: var(--brand-pink-soft);
	}

	@media (max-width: 640px) {
		.tc-carousel-btn {
			display: none;
		}
	}

	/* CTA */
	.tc-cta-section {
		text-align: center;
		background: linear-gradient(180deg, transparent, rgba(255, 63, 174, 0.08));
		border-radius: 28px;
	}

	.tc-cta-sub {
		max-width: 50ch;
		margin: 0 auto 1.75rem;
		color: var(--brand-cream-dim);
	}

	/* Footer */
	.tc-footer {
		text-align: center;
		padding: 2.5rem 1.5rem 3rem;
		color: var(--brand-cream-dim);
		font-size: 0.9rem;
	}

	.tc-footer-link {
		color: var(--brand-pink-soft);
		text-decoration: none;
	}
	.tc-footer-link:hover {
		text-decoration: underline;
	}

	.tc-footer-copyright {
		margin-top: 1rem;
		opacity: 0.7;
	}
</style>
