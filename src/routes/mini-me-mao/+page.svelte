<script>
	const PK = '/images/mini-me-mao/presskit';

	import IconArrowLeft from 'lucide-svelte/icons/arrow-left';
	import IconShirt from 'lucide-svelte/icons/shirt';
	import IconPaintbrush from 'lucide-svelte/icons/paintbrush';
	import IconCoins from 'lucide-svelte/icons/coins';
	import IconPalette from 'lucide-svelte/icons/palette';
	import IconGift from 'lucide-svelte/icons/gift';
	import IconSparkle from 'lucide-svelte/icons/sparkle';
	import IconPlay from 'lucide-svelte/icons/play';
	import IconNewspaper from 'lucide-svelte/icons/newspaper';
	import IconSparkles from 'lucide-svelte/icons/sparkles';
	import IconMail from 'lucide-svelte/icons/mail';
	import IconHeart from 'lucide-svelte/icons/heart';
	import IconAppWindow from 'lucide-svelte/icons/app-window';
	import IconStore from 'lucide-svelte/icons/store';
	import IconTimerOff from 'lucide-svelte/icons/timer-off';

	const features = [
		{
			icon: IconAppWindow,
			title: 'Desktop Dollhouse',
			body: 'A desktop companion that sits right on your screen. Drag it anywhere and it stays on top while you work, study, or play.'
		},
		{
			icon: IconStore,
			title: 'New stock twice a day',
			body: 'Browse a shop that rotates with deals twice a day across furniture, decor, apparel, and more.'
		},
		{
			icon: IconShirt,
			title: 'Dress up your mini',
			body: 'Give your tiny companion a look of their own, and watch it carry through everything they do, from painting at the easel to relaxing in their room.'
		},
		{
			icon: IconPaintbrush,
			title: 'An artist who works while you do',
			body: 'Your mini paints on their own in the background, even when you’re in another app entirely. Check in whenever you like and collect what they’ve finished.'
		},
		{
			icon: IconCoins,
			title: 'Sell for gold',
			body: 'Every finished canvas rolls a star rating and a price. Sell it in the gallery, then spend the gold on new furniture and decor.'
		},
		{
			icon: IconPalette,
			title: 'Unlock painting styles',
			body: 'Level up your mini’s skill to unlock new ways for them to paint, from simple Doodles to intricate Master works.'
		},
		{
			icon: IconGift,
			title: 'Collect decorations',
			body: 'Furniture and knick-knacks aren’t just cute. A well-decorated room keeps your mini inspired at the canvas.'
		},
		{
			icon: IconTimerOff,
			title: 'Play at your own pace',
			body: 'No timers, no pressure. Every menu is player-driven, so your dollhouse grows exactly as fast as you want it to.'
		}
	];

	const trailerId = 'c_9bRL9W9X4';

	// The embed only loads once the visitor clicks play.
	let playing = $state(false);

	const steamUrl = 'https://store.steampowered.com/app/4979870/Mini_MeMao/';

	const screenshots = [
		{
			src: `${PK}/screenshot1.png`,
			alt: 'A pixel art dollhouse room with a kitchen, bed, bonsai, and the mini painting at an easel'
		},
		{
			src: `${PK}/screenshot3.png`,
			alt: 'The in-game shop showing decorations for sale, including a grandfather clock and a fish bowl'
		},
		{
			src: `${PK}/screenshot4.png`,
			alt: 'A dollhouse room with finished paintings hung in gold frames along the wall'
		},
		{
			src: `${PK}/screenshot5.png`,
			alt: 'The character dress-up screen with hairstyle, outfit, and skin tone options'
		}
	];

	const paintingStyles = [
		{ name: 'Doodles', img: '/images/mini-me-mao/paintings/doodles.png' },
		{ name: 'Miniature', img: '/images/mini-me-mao/paintings/miniature.png' },
		{ name: 'Landscape', img: '/images/mini-me-mao/paintings/landscape.png' },
		{ name: 'Pop', img: '/images/mini-me-mao/paintings/pop.png' },
		{ name: 'Memao', img: '/images/mini-me-mao/paintings/memao.png' },
		{ name: 'Master', img: '/images/mini-me-mao/paintings/master.png' }
	];
</script>

<svelte:head>
	<title>Mini Me-Mao: a cozy desktop dollhouse | Sleeping Robot Games</title>
	<meta
		name="description"
		content="A tiny companion that lives right on your desktop! Unpack and decorate a cozy dollhouse, dress up your mini, and watch them paint while you work or play."
	/>
	<meta property="og:type" content="website" />
	<meta property="og:title" content="Mini Me-Mao: a cozy desktop dollhouse" />
	<meta
		property="og:description"
		content="A tiny companion that lives right on your desktop! Unpack and decorate a cozy dollhouse, dress up your mini, and watch them paint while you work or play."
	/>
	<meta
		property="og:image"
		content="https://sleepingrobotgames.com/images/mini-me-mao/presskit/maincapsule.jpg"
	/>
</svelte:head>

<div class="mm-page">
	<!-- Nav -->
	<nav class="mm-nav">
		<a href="/" class="mm-nav-back">
			<IconArrowLeft class="h-4 w-4" />
			<span>Sleeping Robot Games</span>
		</a>
		<a href={steamUrl} target="_blank" rel="noreferrer" class="mm-nav-badge">
			<IconSparkle class="h-3.5 w-3.5" />
			Wishlist on Steam
		</a>
	</nav>

	<!-- Hero -->
	<header class="mm-hero">
		<img
			src="/images/mini-me-mao/presskit/libraryhero.jpg"
			alt=""
			class="mm-hero-bg"
			aria-hidden="true"
		/>
		<div class="mm-hero-scrim"></div>
		<div class="mm-hero-content">
			<img
				src="/images/mini-me-mao/presskit/Mini_Memao_Title.png"
				alt="Mini Me-Mao"
				class="mm-hero-logo"
			/>
			<p class="mm-hero-tagline">A tiny companion that lives right on your desktop</p>
			<div class="mm-hero-ctas">
				<a href={steamUrl} target="_blank" rel="noreferrer" class="mm-btn mm-btn-primary">
					<IconSparkles class="h-4 w-4" />
					Wishlist on Steam
				</a>
				<a
					href="https://sleeping-robot-games.itch.io/mini-me-mao"
					target="_blank"
					rel="noreferrer"
					class="mm-btn mm-btn-ghost"
				>
					Play the demo
				</a>
				<a href="/mini-me-mao/press-kit" class="mm-btn mm-btn-ghost">
					<IconNewspaper class="h-4 w-4" />
					Press Kit
				</a>
			</div>
		</div>
	</header>

	<main>
		<!-- About -->
		<section class="mm-section mm-about">
			<p class="mm-about-text">
				Unpack and decorate a cozy dollhouse, dress up your mini, and watch them paint while you
				work or play. Sell their art for gold, unlock new painting styles, and cultivate the perfect
				mix of decorations and cozy details.
			</p>
		</section>

		<!-- Trailer -->
		<section class="mm-section mm-trailer-section" id="trailer">
			<h2 class="mm-h2">Watch the trailer</h2>
			<div class="mm-trailer">
				{#if playing}
					<iframe
						src="https://www.youtube-nocookie.com/embed/{trailerId}?autoplay=1&rel=0"
						title="Mini Me-Mao announcement trailer"
						allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
						allowfullscreen
					></iframe>
				{:else}
					<button type="button" class="mm-trailer-btn" onclick={() => (playing = true)}>
						<img
							src="{PK}/ytthumb_1280x720.png"
							alt=""
							aria-hidden="true"
							class="mm-trailer-poster"
						/>
						<span class="mm-trailer-overlay">
							<span class="mm-trailer-play"><IconPlay class="h-7 w-7" /></span>
						</span>
						<span class="mm-sr-only">Play the Mini Me-Mao announcement trailer</span>
					</button>
				{/if}
			</div>
		</section>

		<!-- Features -->
		<section class="mm-section">
			<h2 class="mm-h2">Key Features</h2>
			<div class="mm-features">
				{#each features as f}
					<div class="mm-feature-card">
						<div class="mm-feature-icon">
							<f.icon class="h-6 w-6" />
						</div>
						<h3 class="mm-feature-title">{f.title}</h3>
						<p class="mm-feature-body">{f.body}</p>
					</div>
				{/each}
			</div>
		</section>

		<!-- Painting styles -->
		<section class="mm-section mm-styles-section">
			<h2 class="mm-h2">Six painting styles to master</h2>
			<p class="mm-styles-sub">
				Your mini’s brushwork gets more ambitious as their painting skill grows.
			</p>
			<div class="mm-styles-row">
				{#each paintingStyles as s}
					<div class="mm-style-card">
						<div class="mm-style-frame">
							<img src={s.img} alt="{s.name} painting style preview" />
						</div>
						<span class="mm-style-name">{s.name}</span>
					</div>
				{/each}
			</div>
		</section>

		<!-- Gallery -->
		<section class="mm-section mm-gallery-section">
			<h2 class="mm-h2">Screenshots</h2>
			<div class="mm-gallery-grid">
				{#each screenshots as shot}
					<figure class="mm-shot">
						<div class="mm-shot-frame">
							<img src={shot.src} alt={shot.alt} />
						</div>
					</figure>
				{/each}
			</div>
		</section>

		<!-- Follow CTA -->
		<section class="mm-section mm-follow-section">
			<IconHeart class="mm-follow-icon h-7 w-7" />
			<h2 class="mm-h2">Be the first to know</h2>
			<p class="mm-follow-sub">
				We’re still finishing the trailer and Steam page. Follow along for progress, or say hi.
			</p>
			<div class="mm-hero-ctas">
				<a
					href="https://bsky.app/profile/bronskydev.bsky.social"
					target="_blank"
					class="mm-btn mm-btn-primary"
				>
					Follow on Bluesky
				</a>
				<a href="mailto:support@sleepingrobotgames.com" class="mm-btn mm-btn-ghost">
					<IconMail class="h-4 w-4" />
					Email us
				</a>
			</div>
		</section>
	</main>

	<!-- Footer -->
	<footer class="mm-footer">
		<p>
			<a href="/" class="mm-footer-link">← Back to Sleeping Robot Games</a>
		</p>
		<p>
			Press and creators: <a href="/mini-me-mao/press-kit" class="mm-footer-link">Press Kit</a>
		</p>
		<p>
			Also check out our other game, <a href="/smokin-potions" class="mm-footer-link"
				>Smokin Potions</a
			>
		</p>
		<p class="mm-footer-copyright">© 2026 Sleeping Robot Games</p>
	</footer>
</div>

<style>
	:global(html),
	:global(body) {
		margin: 0;
		background: #201320;
	}

	.mm-page {
		--mm-bg: #201320;
		--mm-bg-2: #2c1b2e;
		--mm-panel: #341f38;
		--mm-pink: #ff3fae;
		--mm-pink-soft: #ffa8dc;
		--mm-cream: #fbf1e6;
		--mm-cream-dim: #d8c9d4;
		--mm-gold: #ffc857;

		background: var(--mm-bg);
		color: var(--mm-cream);
		font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
		line-height: 1.6;
		overflow-x: hidden;
	}

	.mm-h2,
	.mm-hero-tagline,
	.mm-nav-back span,
	:global(.mm-btn) {
		font-family: 'Baloo 2 Variable', sans-serif;
	}

	/* Nav */
	.mm-nav {
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

	.mm-nav-back {
		display: flex;
		align-items: center;
		gap: 0.4rem;
		color: var(--mm-cream);
		font-weight: 600;
		font-size: 0.95rem;
		text-decoration: none;
		opacity: 0.9;
	}
	.mm-nav-back:hover {
		opacity: 1;
		color: var(--mm-pink-soft);
	}

	.mm-nav-badge {
		display: inline-flex;
		align-items: center;
		gap: 0.4rem;
		font-size: 0.75rem;
		font-weight: 600;
		letter-spacing: 0.02em;
		color: var(--mm-bg);
		background: var(--mm-gold);
		text-decoration: none;
		padding: 0.35rem 0.7rem;
		border-radius: 999px;
		white-space: nowrap;
		flex-shrink: 0;
	}

	@media (max-width: 480px) {
		.mm-nav {
			padding: 0.65rem 0.85rem;
		}
		.mm-nav-back {
			font-size: 0.8rem;
			white-space: nowrap;
			overflow: hidden;
			text-overflow: ellipsis;
		}
		.mm-nav-badge {
			font-size: 0.68rem;
			padding: 0.3rem 0.55rem;
		}
	}

	/* Hero */
	.mm-hero {
		position: relative;
		display: flex;
		align-items: flex-end;
		min-height: min(72vh, 620px);
		overflow: hidden;
	}

	.mm-hero-bg {
		position: absolute;
		inset: 0;
		width: 100%;
		height: 100%;
		object-fit: cover;
		object-position: 62% 38%;
	}

	.mm-hero-scrim {
		position: absolute;
		inset: 0;
		background: linear-gradient(
				180deg,
				rgba(20, 10, 20, 0.15) 0%,
				rgba(20, 10, 20, 0.55) 60%,
				rgba(18, 9, 18, 0.92) 100%
			),
			linear-gradient(90deg, rgba(18, 9, 18, 0.75) 0%, rgba(18, 9, 18, 0.15) 55%);
	}

	.mm-hero-content {
		position: relative;
		z-index: 1;
		width: 100%;
		max-width: 1100px;
		margin: 0 auto;
		padding: 2.5rem 1.5rem 3.5rem;
	}

	.mm-hero-logo {
		width: min(520px, 80vw);
		max-width: 100%;
		height: auto;
		display: block;
		filter: drop-shadow(0 8px 24px rgba(0, 0, 0, 0.45));
		animation: mm-float 5s ease-in-out infinite;
	}

	.mm-hero-tagline {
		margin: 1.1rem 0 1.6rem;
		font-size: clamp(1.05rem, 2.4vw, 1.5rem);
		font-weight: 600;
		color: var(--mm-cream);
		max-width: 40ch;
		text-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
	}

	.mm-hero-ctas {
		display: flex;
		flex-wrap: wrap;
		gap: 0.9rem;
	}

	:global(.mm-btn) {
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

	:global(.mm-btn-primary) {
		background: var(--mm-pink);
		color: #fff;
		box-shadow: 0 6px 18px rgba(255, 63, 174, 0.35);
	}
	:global(a.mm-btn-primary:hover) {
		background: #ff5cbb;
	}
	:global(.mm-btn-primary[aria-disabled='true']) {
		cursor: default;
		opacity: 0.92;
	}

	:global(.mm-btn-ghost) {
		background: transparent;
		color: var(--mm-cream);
		border-color: rgba(255, 255, 255, 0.35);
	}
	:global(a.mm-btn-ghost:hover) {
		border-color: var(--mm-pink-soft);
		color: var(--mm-pink-soft);
	}

	@keyframes mm-float {
		0%,
		100% {
			transform: translateY(0);
		}
		50% {
			transform: translateY(-8px);
		}
	}
	@media (prefers-reduced-motion: reduce) {
		.mm-hero-logo {
			animation: none;
		}
	}

	/* Sections */
	.mm-section {
		max-width: 1100px;
		margin: 0 auto;
		padding: 3.5rem 1.5rem;
	}

	.mm-h2 {
		font-size: clamp(1.6rem, 3vw, 2.1rem);
		font-weight: 700;
		text-align: center;
		margin: 0 0 0.5rem;
		color: var(--mm-cream);
	}

	.mm-about {
		text-align: center;
	}
	.mm-about-text {
		max-width: 62ch;
		margin: 0 auto;
		font-size: clamp(1.05rem, 2vw, 1.25rem);
		color: var(--mm-cream);
	}

	/* Features */
	.mm-features {
		margin-top: 2rem;
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
		gap: 1.25rem;
	}

	.mm-feature-card {
		background: var(--mm-panel);
		border: 1px solid rgba(255, 255, 255, 0.06);
		border-radius: 20px;
		padding: 1.5rem;
	}

	.mm-feature-icon {
		display: inline-flex;
		align-items: center;
		justify-content: center;
		width: 44px;
		height: 44px;
		border-radius: 14px;
		background: rgba(255, 63, 174, 0.16);
		color: var(--mm-pink-soft);
		margin-bottom: 0.9rem;
	}

	.mm-feature-title {
		font-family: 'Baloo 2 Variable', sans-serif;
		font-size: 1.15rem;
		font-weight: 700;
		margin: 0 0 0.4rem;
		color: var(--mm-cream);
	}

	.mm-feature-body {
		font-size: 0.95rem;
		color: var(--mm-cream-dim);
		margin: 0;
	}

	/* Painting styles */
	.mm-styles-section {
		text-align: center;
	}

	.mm-styles-sub {
		max-width: 56ch;
		margin: 0 auto;
		color: var(--mm-cream-dim);
	}

	.mm-styles-row {
		margin-top: 2rem;
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 1.5rem;
	}

	.mm-style-card {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 0.6rem;
	}

	.mm-style-frame {
		background: var(--mm-panel);
		border: 1px solid rgba(255, 255, 255, 0.08);
		border-radius: 16px;
		padding: 0.9rem 1.1rem;
		box-shadow: 0 6px 16px rgba(0, 0, 0, 0.25);
	}

	.mm-style-frame img {
		image-rendering: pixelated;
		height: 48px;
		width: auto;
		display: block;
	}

	.mm-style-name {
		font-family: 'Baloo 2 Variable', sans-serif;
		font-weight: 600;
		font-size: 0.85rem;
		color: var(--mm-cream-dim);
	}

	/* Trailer */
	.mm-trailer-section {
		text-align: center;
	}

	.mm-trailer {
		position: relative;
		display: block;
		margin: 1.75rem auto 0;
		max-width: 900px;
		aspect-ratio: 16 / 9;
		border-radius: 20px;
		overflow: hidden;
		background: var(--mm-panel);
		border: 1px solid rgba(255, 255, 255, 0.08);
		box-shadow: 0 20px 50px rgba(0, 0, 0, 0.4);
	}

	.mm-trailer iframe {
		width: 100%;
		height: 100%;
		border: 0;
		display: block;
	}

	.mm-trailer-btn {
		display: block;
		width: 100%;
		height: 100%;
		padding: 0;
		border: 0;
		background: none;
		cursor: pointer;
	}

	.mm-sr-only {
		position: absolute;
		width: 1px;
		height: 1px;
		padding: 0;
		margin: -1px;
		overflow: hidden;
		clip: rect(0, 0, 0, 0);
		white-space: nowrap;
		border: 0;
	}

	.mm-trailer-poster {
		width: 100%;
		height: 100%;
		object-fit: cover;
		display: block;
	}

	.mm-trailer-overlay {
		position: absolute;
		inset: 0;
		display: flex;
		align-items: center;
		justify-content: center;
		background: rgba(20, 10, 20, 0.4);
		transition: background 0.2s ease;
	}

	.mm-trailer-btn:hover .mm-trailer-overlay {
		background: rgba(20, 10, 20, 0.28);
	}

	.mm-trailer-play {
		display: inline-flex;
		align-items: center;
		justify-content: center;
		width: 74px;
		height: 74px;
		border-radius: 999px;
		background: var(--mm-pink);
		color: #fff;
		padding-left: 4px;
		box-shadow: 0 10px 30px rgba(255, 63, 174, 0.45);
	}

	/* Gallery */
	.mm-gallery-section {
		text-align: center;
	}

	.mm-gallery-grid {
		margin-top: 1.5rem;
		display: grid;
		grid-template-columns: 1fr;
		gap: 1.5rem;
		align-items: start;
	}

	@media (min-width: 760px) {
		.mm-gallery-grid {
			grid-template-columns: repeat(2, minmax(0, 1fr));
		}
	}

	.mm-shot {
		margin: 0;
	}

	.mm-shot-frame {
		display: flex;
		align-items: center;
		justify-content: center;
		background: var(--mm-panel);
		border: 1px solid rgba(255, 255, 255, 0.08);
		border-radius: 20px;
		overflow: hidden;
		box-shadow: 0 12px 30px rgba(0, 0, 0, 0.35);
		aspect-ratio: 16 / 9;
	}

	.mm-shot-frame img {
		display: block;
		max-width: 100%;
		max-height: 100%;
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

	/* Follow */
	.mm-follow-section {
		display: flex;
		flex-direction: column;
		align-items: center;
		text-align: center;
		background: linear-gradient(180deg, transparent, rgba(255, 63, 174, 0.08));
		border-radius: 28px;
	}

	.mm-follow-section .mm-hero-ctas {
		justify-content: center;
	}

	:global(.mm-follow-icon) {
		color: var(--mm-pink);
		margin-bottom: 0.5rem;
	}

	.mm-follow-sub {
		max-width: 50ch;
		margin: 0 auto 1.75rem;
		color: var(--mm-cream-dim);
	}

	/* Footer */
	.mm-footer {
		text-align: center;
		padding: 2.5rem 1.5rem 3rem;
		color: var(--mm-cream-dim);
		font-size: 0.9rem;
	}

	.mm-footer-link {
		color: var(--mm-pink-soft);
		text-decoration: none;
	}
	.mm-footer-link:hover {
		text-decoration: underline;
	}

	.mm-footer-copyright {
		margin-top: 1rem;
		opacity: 0.7;
	}
</style>
