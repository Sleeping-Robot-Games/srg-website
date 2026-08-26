<script>
	import IconArrowLeft from 'lucide-svelte/icons/arrow-left';
	import IconMail from 'lucide-svelte/icons/mail';
	import IconDownload from 'lucide-svelte/icons/download';
	import IconInfo from 'lucide-svelte/icons/info';
	import IconFilm from 'lucide-svelte/icons/film';
	import IconNewspaper from 'lucide-svelte/icons/newspaper';

	const factsheet = [
		{ label: 'Developer', value: 'Sleeping Robot Games' },
		{ label: 'Location', value: '[City, Country]', todo: true },
		{ label: 'Genre', value: 'Cozy desktop companion / idle dollhouse' },
		{ label: 'Platform', value: 'PC via Steam' },
		{ label: 'Release window', value: '[Release window]', todo: true },
		{
			label: 'Press contact',
			value: 'support@sleepingrobotgames.com',
			href: 'mailto:support@sleepingrobotgames.com'
		},
		{
			label: 'Playtest',
			value: 'sleeping-robot-games.itch.io/mini-me-mao',
			href: 'https://sleeping-robot-games.itch.io/mini-me-mao'
		},
		{ label: 'Steam page', value: '[Steam page link]', todo: true }
	];

	const features = [
		'A desktop companion that sits right on your screen. Drag it anywhere and it stays on top while you work, study, or play.',
		'Your mini paints on their own in the background, even when you’re in another app entirely. Check in whenever you like and collect what they’ve finished.',
		'Every finished canvas rolls a star rating and a price. Sell it in the gallery, then spend the gold on new furniture and decor.',
		'Six painting styles to unlock, from simple Doodles to intricate Master works, as your mini’s skill grows.',
		'A shop that restocks daily with rotating deals on furniture, decor, and dress up styles.',
		'Dress up your mini and watch the look carry through everything they do, from the easel to their room.',
		'A well-decorated room keeps your mini inspired at the canvas, so collecting is more than just cute.',
		'No timers, no pressure. Every menu is player-driven, so your dollhouse grows exactly as fast as you want it to.'
	];

	const PK = '/images/mini-me-mao/presskit';

	const keyArt = [
		{
			name: 'Main capsule',
			file: `${PK}/maincapsule.jpg`,
			meta: 'JPG · 1232×706 · 878 KB',
			alt: 'Mini Me-Mao main capsule art: a young painter at her easel in a warm, lamp-lit studio full of plants and framed pictures, with the game logo at left'
		},
		{
			name: 'Vertical capsule',
			file: `${PK}/verticalcapsule2.jpg`,
			meta: 'JPG · 748×896 · 665 KB',
			alt: 'Vertical crop of the Mini Me-Mao capsule art with the logo across the lower half'
		},
		{
			name: 'Library capsule',
			file: `${PK}/librarycapsule2.jpg`,
			meta: 'JPG · 600×900 · 542 KB',
			alt: 'Tall Steam library capsule showing the painter and her easel with the logo at the bottom'
		},
		{
			name: 'Small capsule',
			file: `${PK}/smallcapsule.jpg`,
			meta: 'JPG · 462×174 · 105 KB',
			alt: 'Wide Steam small capsule with the Mini Me-Mao logo beside the painter at her canvas'
		},
		{
			name: 'Library hero',
			file: `${PK}/libraryhero.jpg`,
			meta: 'JPG · 3840×1240 · 3.8 MB',
			alt: 'Ultrawide Steam library hero: a close crop of the painter mid-brushstroke in front of a bookshelf'
		},
		{
			name: 'Itch.io capsule',
			file: `${PK}/itchcapsule.jpg`,
			meta: 'JPG · 630×500 · 342 KB',
			alt: 'Itch.io capsule art of the painter at her easel beside a large monstera plant'
		},
		{
			name: 'Social post',
			file: `${PK}/social-post.png`,
			meta: 'PNG · 1232×706 · 1.5 MB',
			alt: 'Social-media-sized version of the Mini Me-Mao key art with the logo'
		}
	];

	const screenshots = [
		{
			name: 'Design a space of your own',
			file: `${PK}/screenshot1.png`,
			meta: 'PNG · 1920×1080 · 722 KB',
			alt: 'A pixel art dollhouse room with a kitchen, bed, bonsai, and the mini painting at an easel, framed by trees on a pink backdrop'
		},
		{
			name: 'Master the arts and sell your paintings',
			file: `${PK}/screenshot2.png`,
			meta: 'PNG · 1920×1080 · 3.4 MB',
			alt: 'The Gallery window listing finished paintings with gold values, floating over a desktop next to a pink dollhouse room'
		},
		{
			name: 'Unlock endless decor and cosmetics',
			file: `${PK}/screenshot3.png`,
			meta: 'PNG · 1920×1080 · 2.4 MB',
			alt: 'The in-game Shop window showing decorations for sale, including a grandfather clock and a fish bowl, priced in gold'
		},
		{
			name: 'Improve your skills and display your masterpieces',
			file: `${PK}/screenshot4.png`,
			meta: 'PNG · 1920×1080 · 691 KB',
			alt: 'A dollhouse room with finished paintings hung in gold frames along the wall and the mini waving below them'
		},
		{
			name: 'Bring your mini artist to life',
			file: `${PK}/screenshot5.png`,
			meta: 'PNG · 1920×1080 · 406 KB',
			alt: 'The Character dress-up window with hairstyle, outfit, and skin tone options for the mini'
		}
	];

	const logos = [
		{
			name: 'Mini Me-Mao logo',
			file: `${PK}/Mini_Memao_Title.png`,
			meta: 'PNG · 4500×3600 · 2 MB · transparent',
			alt: 'The Mini Me-Mao wordmark: pixel-style "mini" above a soft rounded "me-mao", both with a hot pink glow'
		},
		{
			name: 'Sleeping Robot Games logo',
			file: '/images/full-logo-SRG.png',
			meta: 'PNG · 512×512',
			alt: 'Sleeping Robot Games logo: a sleeping robot head surrounded by red camellia flowers'
		}
	];

	const animations = [
		{
			name: 'Painting',
			file: `${PK}/paint1000.gif`,
			meta: 'GIF · 480×480 · 35 KB',
			alt: 'Animated pixel art of the mini painting at an easel'
		},
		{
			name: 'Reading',
			file: `${PK}/readingANIM.gif`,
			meta: 'GIF · 480×480 · 22 KB',
			alt: 'Animated pixel art of the mini reading a book'
		},
		{
			name: 'Waving',
			file: `${PK}/ogwave.gif`,
			meta: 'GIF · 192×192 · 19 KB',
			alt: 'Animated pixel art of the mini waving'
		},
		{
			name: 'Idle',
			file: `${PK}/ogidle.gif`,
			meta: 'GIF · 192×192 · 7 KB',
			alt: 'Animated pixel art of the mini standing idle'
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

	const contacts = [
		{
			label: 'Email',
			value: 'support@sleepingrobotgames.com',
			href: 'mailto:support@sleepingrobotgames.com'
		},
		{
			label: 'Bluesky',
			value: '@bronskydev.bsky.social',
			href: 'https://bsky.app/profile/bronskydev.bsky.social'
		},
		{
			label: 'Links',
			value: 'linktr.ee/SleepingRobotGames',
			href: 'https://linktr.ee/SleepingRobotGames'
		}
	];
</script>

<svelte:head>
	<title>Mini Me-Mao Press Kit | Sleeping Robot Games</title>
	<meta
		name="description"
		content="Press kit for Mini Me-Mao, a cozy desktop dollhouse from Sleeping Robot Games. Factsheet, descriptions, key art, screenshots, logos, and press contact."
	/>
	<meta property="og:type" content="website" />
	<meta property="og:title" content="Mini Me-Mao Press Kit" />
	<meta
		property="og:description"
		content="Factsheet, descriptions, key art, screenshots, logos, and press contact for Mini Me-Mao."
	/>
	<meta
		property="og:image"
		content="https://sleepingrobotgames.com/images/mini-me-mao/presskit/maincapsule.jpg"
	/>
</svelte:head>

<div class="mm-page">
	<!-- Nav -->
	<nav class="mm-nav">
		<a href="/mini-me-mao" class="mm-nav-back">
			<IconArrowLeft class="h-4 w-4" />
			<span>Mini Me-Mao</span>
		</a>
		<span class="mm-nav-badge">
			<IconNewspaper class="h-3.5 w-3.5" />
			Press Kit
		</span>
	</nav>

	<!-- Header -->
	<header class="mm-pk-hero">
		<img
			src="/images/mini-me-mao/presskit/Mini_Memao_Title.png"
			alt="Mini Me-Mao"
			class="mm-pk-hero-logo"
		/>
		<p class="mm-pk-eyebrow">Press Kit</p>
		<p class="mm-pk-hero-tagline">A tiny companion that lives right on your desktop</p>
		<div class="mm-hero-ctas mm-pk-hero-ctas">
			<a href="#assets" class="mm-btn mm-btn-primary">
				<IconDownload class="h-4 w-4" />
				Jump to assets
			</a>
			<a href="mailto:support@sleepingrobotgames.com" class="mm-btn mm-btn-ghost">
				<IconMail class="h-4 w-4" />
				Press contact
			</a>
		</div>
	</header>

	<main>
		<!-- Factsheet -->
		<section class="mm-section" id="factsheet">
			<h2 class="mm-h2">Factsheet</h2>
			<dl class="mm-facts">
				{#each factsheet as f}
					<div class="mm-fact">
						<dt>{f.label}</dt>
						<dd>
							{#if f.href}
								<a href={f.href} target={f.href.startsWith('mailto:') ? null : '_blank'}
									>{f.value}</a
								>
							{:else if f.todo}
								<span class="mm-todo">{f.value}</span>
							{:else}
								{f.value}
							{/if}
						</dd>
					</div>
				{/each}
			</dl>
		</section>

		<!-- Description -->
		<section class="mm-section" id="description">
			<h2 class="mm-h2">Description</h2>
			<div class="mm-copy">
				<h3 class="mm-h3">Short</h3>
				<p class="mm-quote">
					Mini Me-Mao is a cozy desktop dollhouse. Unpack and decorate a tiny home, dress up your
					mini, and watch them paint while you work or play.
				</p>

				<h3 class="mm-h3">Full</h3>
				<p class="mm-quote">
					Mini Me-Mao is a cozy desktop dollhouse that lives on top of your screen. Unpack and
					decorate a tiny home, dress up your mini, and watch them paint away while you work, study,
					or play something else entirely. Every finished canvas rolls a star rating and a price, so
					you can sell it in the gallery and spend the gold on new furniture and decor, which in
					turn keeps your mini inspired at the easel. Level up their skill to unlock six painting
					styles, from simple Doodles to intricate Master works. There are no timers and no
					pressure. Your dollhouse grows exactly as fast as you want it to.
				</p>
			</div>
		</section>

		<!-- Features -->
		<section class="mm-section" id="features">
			<h2 class="mm-h2">Features</h2>
			<ul class="mm-bullets">
				{#each features as f}
					<li>{f}</li>
				{/each}
			</ul>
		</section>

		<!-- Video -->
		<section class="mm-section" id="video">
			<h2 class="mm-h2">Video</h2>
			<div class="mm-placeholder">
				<IconFilm class="h-7 w-7" />
				<p class="mm-placeholder-title">Trailer coming soon</p>
				<p class="mm-placeholder-body">
					The announcement trailer is still in production. Email
					<a href="mailto:support@sleepingrobotgames.com">support@sleepingrobotgames.com</a> and we’ll
					send it over the moment it’s ready.
				</p>
			</div>
		</section>

		<!-- Assets -->
		<section class="mm-section" id="assets">
			<h2 class="mm-h2">Assets</h2>
			<p class="mm-section-sub">
				Right-click and save, or use the download link under each file. Everything here is cleared
				for coverage.
			</p>

			<h3 class="mm-h3 mm-h3-group">Key art</h3>
			<div class="mm-asset-grid">
				{#each keyArt as a}
					<figure class="mm-asset">
						<div class="mm-asset-frame mm-asset-frame-fit">
							<img src={a.file} alt={a.alt} />
						</div>
						<figcaption>
							<span class="mm-asset-name">{a.name}</span>
							<span class="mm-asset-meta">{a.meta}</span>
							<a class="mm-asset-dl" href={a.file} download>
								<IconDownload class="h-3.5 w-3.5" />
								Download
							</a>
						</figcaption>
					</figure>
				{/each}
			</div>

			<h3 class="mm-h3 mm-h3-group">Screenshots</h3>
			<div class="mm-asset-grid">
				{#each screenshots as a}
					<figure class="mm-asset">
						<div class="mm-asset-frame mm-asset-frame-wide">
							<img src={a.file} alt={a.alt} />
						</div>
						<figcaption>
							<span class="mm-asset-name">{a.name}</span>
							<span class="mm-asset-meta">{a.meta}</span>
							<a class="mm-asset-dl" href={a.file} download>
								<IconDownload class="h-3.5 w-3.5" />
								Download
							</a>
						</figcaption>
					</figure>
				{/each}
			</div>

			<h3 class="mm-h3 mm-h3-group">Logo</h3>
			<div class="mm-asset-grid">
				{#each logos as a}
					<figure class="mm-asset">
						<div class="mm-asset-frame mm-asset-frame-logo">
							<img src={a.file} alt={a.alt} />
						</div>
						<figcaption>
							<span class="mm-asset-name">{a.name}</span>
							<span class="mm-asset-meta">{a.meta}</span>
							<a class="mm-asset-dl" href={a.file} download>
								<IconDownload class="h-3.5 w-3.5" />
								Download
							</a>
						</figcaption>
					</figure>
				{/each}
			</div>

			<h3 class="mm-h3 mm-h3-group">Character animations</h3>
			<div class="mm-asset-grid mm-asset-grid-anim">
				{#each animations as a}
					<figure class="mm-asset">
						<div class="mm-asset-frame mm-asset-frame-anim">
							<img src={a.file} alt={a.alt} class="mm-pixel" />
						</div>
						<figcaption>
							<span class="mm-asset-name">{a.name}</span>
							<span class="mm-asset-meta">{a.meta}</span>
							<a class="mm-asset-dl" href={a.file} download>
								<IconDownload class="h-3.5 w-3.5" />
								Download
							</a>
						</figcaption>
					</figure>
				{/each}
			</div>

			<h3 class="mm-h3 mm-h3-group">Painting styles</h3>
			<div class="mm-styles-row">
				{#each paintingStyles as s}
					<a class="mm-style-card" href={s.img} download>
						<div class="mm-style-frame">
							<img src={s.img} alt="{s.name} painting style preview" />
						</div>
						<span class="mm-style-name">{s.name}</span>
					</a>
				{/each}
			</div>
		</section>

		<!-- Team -->
		<section class="mm-section" id="team">
			<h2 class="mm-h2">Team</h2>
			<p class="mm-copy-center">
				Mini Me-Mao is independently developed by Sleeping Robot Games, a small studio making games
				we want to play. <span class="mm-todo">[Team size and credits]</span>
			</p>
		</section>

		<!-- Contact -->
		<section class="mm-section" id="contact">
			<h2 class="mm-h2">Contact</h2>
			<p class="mm-section-sub">Press and creator inquiries are always welcome.</p>
			<dl class="mm-facts mm-facts-contact">
				{#each contacts as c}
					<div class="mm-fact">
						<dt>{c.label}</dt>
						<dd>
							<a href={c.href} target={c.href.startsWith('mailto:') ? null : '_blank'}>{c.value}</a>
						</dd>
					</div>
				{/each}
			</dl>
		</section>

		<!-- Asset use rights -->
		<section class="mm-section">
			<div class="mm-callout">
				<IconInfo class="mm-callout-icon h-5 w-5" />
				<div>
					<p class="mm-callout-title">Asset use rights</p>
					<p class="mm-callout-body">
						All screenshots, key art, logos, and other assets in this press kit are cleared for
						press, creator, video, stream, and social media coverage of Mini Me-Mao. Monetization of
						videos featuring the game is fine. Please credit Sleeping Robot Games and link back to
						<a href="/mini-me-mao">the game page</a> when covering it.
					</p>
				</div>
			</div>
		</section>
	</main>

	<!-- Footer -->
	<footer class="mm-footer">
		<p>
			<a href="/mini-me-mao" class="mm-footer-link">← Back to Mini Me-Mao</a>
		</p>
		<p>
			<a href="/" class="mm-footer-link">Sleeping Robot Games</a>
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
	.mm-h3,
	.mm-pk-hero-tagline,
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
	.mm-pk-hero {
		display: flex;
		flex-direction: column;
		align-items: center;
		text-align: center;
		padding: 2.75rem 1.5rem 2.5rem;
		background: radial-gradient(circle at 50% 0%, rgba(255, 63, 174, 0.16), transparent 62%),
			var(--mm-bg-2);
		border-bottom: 1px solid rgba(255, 255, 255, 0.06);
	}

	.mm-pk-hero-logo {
		width: min(340px, 72vw);
		height: auto;
		display: block;
		filter: drop-shadow(0 8px 24px rgba(0, 0, 0, 0.45));
	}

	.mm-pk-eyebrow {
		margin: 0.25rem 0 0;
		font-family: 'Baloo 2 Variable', sans-serif;
		font-size: 0.8rem;
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 0.16em;
		color: var(--mm-pink-soft);
	}

	.mm-pk-hero-tagline {
		margin: 0.5rem 0 1.6rem;
		font-size: clamp(1.05rem, 2.4vw, 1.35rem);
		font-weight: 600;
		color: var(--mm-cream);
		max-width: 40ch;
	}

	.mm-hero-ctas {
		display: flex;
		flex-wrap: wrap;
		gap: 0.9rem;
	}
	.mm-pk-hero-ctas {
		justify-content: center;
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

	:global(.mm-btn-ghost) {
		background: transparent;
		color: var(--mm-cream);
		border-color: rgba(255, 255, 255, 0.35);
	}
	:global(a.mm-btn-ghost:hover) {
		border-color: var(--mm-pink-soft);
		color: var(--mm-pink-soft);
	}

	/* Sections */
	.mm-section {
		max-width: 1100px;
		margin: 0 auto;
		padding: 3rem 1.5rem;
		scroll-margin-top: 4.5rem;
	}

	.mm-h2 {
		font-size: clamp(1.6rem, 3vw, 2.1rem);
		font-weight: 700;
		text-align: center;
		margin: 0 0 0.5rem;
		color: var(--mm-cream);
	}

	.mm-h3 {
		font-size: 0.8rem;
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		color: var(--mm-pink-soft);
		margin: 0 0 0.6rem;
	}
	.mm-h3-group {
		margin-top: 2.25rem;
		text-align: center;
	}

	.mm-section-sub {
		max-width: 58ch;
		margin: 0 auto;
		text-align: center;
		color: var(--mm-cream-dim);
		font-size: 0.95rem;
	}

	/* Factsheet */
	.mm-facts {
		margin: 2rem auto 0;
		max-width: 760px;
		display: grid;
		gap: 1px;
		background: rgba(255, 255, 255, 0.08);
		border: 1px solid rgba(255, 255, 255, 0.08);
		border-radius: 20px;
		overflow: hidden;
	}

	.mm-fact {
		display: grid;
		grid-template-columns: 1fr;
		gap: 0.15rem;
		background: var(--mm-panel);
		padding: 0.9rem 1.25rem;
	}

	@media (min-width: 560px) {
		.mm-fact {
			grid-template-columns: 190px 1fr;
			gap: 1rem;
			align-items: baseline;
		}
	}

	.mm-fact dt {
		font-family: 'Baloo 2 Variable', sans-serif;
		font-weight: 700;
		font-size: 0.85rem;
		text-transform: uppercase;
		letter-spacing: 0.06em;
		color: var(--mm-cream-dim);
	}

	.mm-fact dd {
		margin: 0;
		color: var(--mm-cream);
		overflow-wrap: anywhere;
	}

	.mm-fact dd a {
		color: var(--mm-pink-soft);
		text-decoration: none;
	}
	.mm-fact dd a:hover {
		text-decoration: underline;
	}

	.mm-todo {
		display: inline-block;
		font-size: 0.85rem;
		font-weight: 600;
		color: var(--mm-gold);
		background: rgba(255, 200, 87, 0.14);
		border: 1px dashed rgba(255, 200, 87, 0.45);
		border-radius: 8px;
		padding: 0.1rem 0.5rem;
	}

	/* Description */
	.mm-copy {
		max-width: 720px;
		margin: 2rem auto 0;
	}

	.mm-copy .mm-h3 {
		margin-top: 1.75rem;
	}
	.mm-copy .mm-h3:first-child {
		margin-top: 0;
	}

	.mm-quote {
		margin: 0;
		background: var(--mm-panel);
		border: 1px solid rgba(255, 255, 255, 0.06);
		border-left: 3px solid var(--mm-pink);
		border-radius: 0 16px 16px 0;
		padding: 1.1rem 1.35rem;
		color: var(--mm-cream);
		font-size: 1rem;
	}

	.mm-copy-center {
		max-width: 62ch;
		margin: 1.5rem auto 0;
		text-align: center;
		color: var(--mm-cream-dim);
	}

	/* Features */
	.mm-bullets {
		max-width: 760px;
		margin: 2rem auto 0;
		padding: 0;
		list-style: none;
		display: grid;
		gap: 0.75rem;
	}

	.mm-bullets li {
		position: relative;
		background: var(--mm-panel);
		border: 1px solid rgba(255, 255, 255, 0.06);
		border-radius: 14px;
		padding: 0.85rem 1.1rem 0.85rem 2.4rem;
		color: var(--mm-cream-dim);
		font-size: 0.95rem;
	}

	.mm-bullets li::before {
		content: '';
		position: absolute;
		left: 1.1rem;
		top: 1.35rem;
		width: 7px;
		height: 7px;
		border-radius: 999px;
		background: var(--mm-pink);
	}

	/* Video placeholder */
	.mm-placeholder {
		max-width: 640px;
		margin: 2rem auto 0;
		display: flex;
		flex-direction: column;
		align-items: center;
		text-align: center;
		gap: 0.35rem;
		background: var(--mm-panel);
		border: 1px dashed rgba(255, 255, 255, 0.18);
		border-radius: 20px;
		padding: 2.25rem 1.5rem;
		color: var(--mm-pink-soft);
	}

	.mm-placeholder-title {
		font-family: 'Baloo 2 Variable', sans-serif;
		font-weight: 700;
		font-size: 1.1rem;
		color: var(--mm-cream);
		margin: 0.4rem 0 0;
	}

	.mm-placeholder-body {
		margin: 0;
		max-width: 44ch;
		font-size: 0.92rem;
		color: var(--mm-cream-dim);
	}
	.mm-placeholder-body a {
		color: var(--mm-pink-soft);
	}

	/* Assets */
	.mm-asset-grid {
		margin-top: 1.25rem;
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
		gap: 1.25rem;
	}

	.mm-asset {
		margin: 0;
		display: flex;
		flex-direction: column;
	}

	.mm-asset-frame {
		display: flex;
		align-items: center;
		justify-content: center;
		background: #241528;
		border: 1px solid rgba(255, 255, 255, 0.08);
		border-radius: 18px;
		overflow: hidden;
		aspect-ratio: 4 / 3;
		box-shadow: 0 12px 30px rgba(0, 0, 0, 0.35);
	}

	.mm-asset-frame img {
		display: block;
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

	.mm-asset-frame-logo img,
	.mm-asset-frame img.mm-pixel {
		object-fit: contain;
		width: auto;
		max-width: 100%;
		height: 100%;
		padding: 0.75rem;
	}

	.mm-asset-frame img.mm-pixel {
		image-rendering: pixelated;
	}

	.mm-asset-frame-fit img {
		object-fit: contain;
		width: 100%;
		height: 100%;
		padding: 0.75rem;
	}

	.mm-asset-frame-wide {
		aspect-ratio: 16 / 9;
	}

	.mm-asset-grid-anim {
		grid-template-columns: repeat(auto-fit, minmax(170px, 1fr));
	}

	.mm-asset-frame-anim {
		aspect-ratio: 1 / 1;
		background: var(--mm-bg-2);
	}

	.mm-asset figcaption {
		display: flex;
		flex-direction: column;
		gap: 0.15rem;
		padding-top: 0.7rem;
	}

	.mm-asset-name {
		font-family: 'Baloo 2 Variable', sans-serif;
		font-weight: 700;
		font-size: 0.95rem;
		color: var(--mm-cream);
	}

	.mm-asset-meta {
		font-size: 0.78rem;
		color: var(--mm-cream-dim);
		opacity: 0.8;
	}

	.mm-asset-dl {
		margin-top: 0.35rem;
		display: inline-flex;
		align-items: center;
		gap: 0.35rem;
		align-self: flex-start;
		font-family: 'Baloo 2 Variable', sans-serif;
		font-weight: 700;
		font-size: 0.85rem;
		color: var(--mm-pink-soft);
		text-decoration: none;
	}
	.mm-asset-dl:hover {
		text-decoration: underline;
	}

	/* Painting styles */
	.mm-styles-row {
		margin-top: 1.25rem;
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
		text-decoration: none;
	}

	.mm-style-frame {
		background: var(--mm-panel);
		border: 1px solid rgba(255, 255, 255, 0.08);
		border-radius: 16px;
		padding: 0.9rem 1.1rem;
		box-shadow: 0 6px 16px rgba(0, 0, 0, 0.25);
	}
	.mm-style-card:hover .mm-style-frame {
		border-color: var(--mm-pink-soft);
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

	/* Callout */
	.mm-callout {
		display: flex;
		gap: 0.9rem;
		max-width: 760px;
		margin: 0 auto;
		background: linear-gradient(180deg, rgba(255, 63, 174, 0.1), rgba(255, 63, 174, 0.04));
		border: 1px solid rgba(255, 63, 174, 0.28);
		border-radius: 20px;
		padding: 1.25rem 1.4rem;
	}

	:global(.mm-callout-icon) {
		color: var(--mm-pink);
		flex-shrink: 0;
		margin-top: 0.2rem;
	}

	.mm-callout-title {
		font-family: 'Baloo 2 Variable', sans-serif;
		font-weight: 700;
		margin: 0 0 0.25rem;
		color: var(--mm-cream);
	}

	.mm-callout-body {
		margin: 0;
		font-size: 0.92rem;
		color: var(--mm-cream-dim);
	}
	.mm-callout-body a {
		color: var(--mm-pink-soft);
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
