<script>
	import IconArrowRight from 'lucide-svelte/icons/arrow-right';
</script>

<svelte:head>
	<title>Sleeping Robot Games</title>
</svelte:head>

<div class="hub-page">
	<header class="hub-hero">
		<img src="/images/full-logo-SRG.png" alt="Sleeping Robot Games" class="hub-hero-logo" />
		<h1 class="hub-hero-title">Sleeping Robot Games</h1>
		<p class="hub-hero-tagline">A small studio making games we want to play.</p>
		<div class="hub-hero-links">
			<a href="https://bsky.app/profile/bronskydev.bsky.social" target="_blank">Bluesky</a>
			<span aria-hidden="true">·</span>
			<a href="https://linktr.ee/SleepingRobotGames" target="_blank">Linktree</a>
		</div>
	</header>

	<main>
		<section class="hub-grid">
			<a href="/mini-me-mao" class="hub-card" style="--card-accent: #ff3fae;">
				<div class="hub-card-img">
					<img src="/images/mini-memao-capsule.png" alt="Mini Me-Mao" />
				</div>
				<div class="hub-card-body">
					<div class="hub-card-title-row">
						<h2>Mini Me-Mao</h2>
						<span class="hub-badge">Coming Soon</span>
					</div>
					<p>A cozy desktop dollhouse where your mini paints, sells art, and decorates.</p>
					<span class="hub-card-cta">
						View game <IconArrowRight class="h-4 w-4" />
					</span>
				</div>
			</a>

			<a href="/smokin-potions" class="hub-card" style="--card-accent: #f5a623;">
				<div class="hub-card-img">
					<img src="/images/smokin-potions-capsule.png" alt="Smokin Potions" />
				</div>
				<div class="hub-card-body">
					<div class="hub-card-title-row">
						<h2>Smokin Potions</h2>
						<span class="hub-badge hub-badge-live">Out Now</span>
					</div>
					<p>Explosive local-multiplayer potion battles for 2-4 players.</p>
					<span class="hub-card-cta">
						View game <IconArrowRight class="h-4 w-4" />
					</span>
				</div>
			</a>
		</section>
	</main>

	<footer class="hub-footer">
		<p class="hub-footer-copyright">© 2026 Sleeping Robot Games</p>
	</footer>
</div>

<style>
	:global(html),
	:global(body) {
		margin: 0;
	}

	.hub-page {
		--hub-bg: #171b21;
		--hub-bg-2: #20262f;
		--hub-panel: #262d38;
		--hub-red: #c0392b;
		--hub-red-soft: #e2857a;
		--hub-gold: #d4a13d;
		--hub-teal: #7fb8ad;
		--hub-cream: #f2ede4;
		--hub-cream-dim: #b9c0c9;

		min-height: 100vh;
		display: flex;
		flex-direction: column;
		background: var(--hub-bg);
		color: var(--hub-cream);
		font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
	}

	.hub-hero {
		position: relative;
		display: flex;
		flex-direction: column;
		align-items: center;
		text-align: center;
		padding: 3.5rem 1.5rem 3rem;
		background: radial-gradient(circle at 50% 0%, rgba(192, 57, 43, 0.16), transparent 60%),
			radial-gradient(circle at 20% 100%, rgba(127, 184, 173, 0.1), transparent 55%),
			var(--hub-bg-2);
		border-bottom: 1px solid rgba(255, 255, 255, 0.06);
	}

	.hub-hero-logo {
		width: 132px;
		height: 132px;
		filter: drop-shadow(0 10px 24px rgba(0, 0, 0, 0.45));
	}

	.hub-hero-title {
		font-family: 'Baloo 2 Variable', sans-serif;
		font-size: clamp(1.8rem, 4vw, 2.5rem);
		font-weight: 700;
		margin: 1.1rem 0 0.4rem;
	}

	.hub-hero-tagline {
		color: var(--hub-cream-dim);
		margin: 0;
	}

	.hub-hero-links {
		margin-top: 1.25rem;
		display: flex;
		align-items: center;
		gap: 0.5rem;
		font-size: 0.9rem;
	}

	.hub-hero-links a {
		color: var(--hub-red-soft);
		text-decoration: none;
	}
	.hub-hero-links a:hover {
		text-decoration: underline;
	}
	.hub-hero-links span {
		color: var(--hub-cream-dim);
		opacity: 0.6;
	}

	main {
		flex: 1;
		max-width: 1100px;
		margin: 0 auto;
		width: 100%;
		padding: 3rem 1.5rem 3.5rem;
	}

	.hub-grid {
		display: grid;
		grid-template-columns: 1fr;
		gap: 1.5rem;
	}
	@media (min-width: 640px) {
		.hub-grid {
			grid-template-columns: 1fr 1fr;
		}
	}

	.hub-card {
		display: flex;
		flex-direction: column;
		background: var(--hub-panel);
		border-radius: 20px;
		overflow: hidden;
		text-decoration: none;
		color: inherit;
		border: 1px solid rgba(255, 255, 255, 0.08);
		transition:
			transform 0.2s ease,
			box-shadow 0.2s ease;
	}

	.hub-card:hover {
		transform: translateY(-4px);
		box-shadow: 0 12px 30px -8px color-mix(in srgb, var(--card-accent) 55%, transparent);
	}

	.hub-card-img {
		aspect-ratio: 16 / 9;
		overflow: hidden;
	}

	.hub-card-img img {
		width: 100%;
		height: 100%;
		object-fit: cover;
		display: block;
		transition: transform 0.3s ease;
	}

	.hub-card:hover .hub-card-img img {
		transform: scale(1.05);
	}

	.hub-card-body {
		padding: 1.35rem;
		display: flex;
		flex-direction: column;
		gap: 0.5rem;
		flex: 1;
	}

	.hub-card-title-row {
		display: flex;
		align-items: center;
		gap: 0.6rem;
	}

	.hub-card-title-row h2 {
		font-family: 'Baloo 2 Variable', sans-serif;
		font-size: 1.3rem;
		font-weight: 700;
		margin: 0;
	}

	.hub-badge {
		font-size: 0.7rem;
		font-weight: 700;
		padding: 0.2rem 0.55rem;
		border-radius: 999px;
		background: rgba(255, 63, 174, 0.18);
		color: #ff3fae;
		white-space: nowrap;
	}

	.hub-badge-live {
		background: rgba(245, 166, 35, 0.18);
		color: var(--hub-gold);
	}

	.hub-card-body p {
		font-size: 0.9rem;
		color: var(--hub-cream-dim);
		margin: 0;
	}

	.hub-card-cta {
		margin-top: auto;
		padding-top: 0.5rem;
		display: inline-flex;
		align-items: center;
		gap: 0.35rem;
		font-family: 'Baloo 2 Variable', sans-serif;
		font-weight: 700;
		font-size: 0.9rem;
		color: var(--card-accent);
	}

	.hub-footer {
		text-align: center;
		padding: 1.5rem 1.5rem 2.5rem;
		font-size: 0.85rem;
		color: var(--hub-cream-dim);
		opacity: 0.7;
	}
</style>
