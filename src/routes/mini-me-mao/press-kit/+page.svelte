<script>
	import IconMail from 'lucide-svelte/icons/mail';
	import IconDownload from 'lucide-svelte/icons/download';
	import IconFolderDown from 'lucide-svelte/icons/folder-down';
	import IconInfo from 'lucide-svelte/icons/info';
	import IconFilm from 'lucide-svelte/icons/film';
	import IconSmartphone from 'lucide-svelte/icons/smartphone';
	import IconCheck from 'lucide-svelte/icons/check';

	const factsheet = [
		{ label: 'Developer', value: 'Sleeping Robot Games' },
		{ label: 'Genre', value: 'Cozy / Desktop Companion / Idle' },
		{ label: 'Platform', value: 'PC (Windows, macOS, Linux)' },
		{ label: 'Release window', value: '[Release window]', todo: true },
		{
			label: 'Press contact',
			value: 'press@sleepingrobotgames.com',
			href: 'mailto:press@sleepingrobotgames.com'
		},
		{ label: 'Steam page', value: '[Steam page link]', todo: true }
	];

	const features = [
		'A desktop companion you can place anywhere and have run in the background',
		'Idle painting: your mini creates art while you work or play on other tasks',
		'Sell finished paintings for gold in the gallery, then shop daily deals for 150+ decorations across furniture, wallpaper, flooring, and knick-knacks',
		'Dress up your mini with a wide array of outfits, for over 135 trillion possible character combinations',
		"Unlockable painting styles, each improving in quality as your mini's skill grows — collect every star rating to master a painting and unlock it as a decoration for your room"
	];

	const roadmap = [
		{ name: 'Style Shop', done: true },
		{ name: 'Wardrobe, with outfits you can equip for any occasion', done: true },
		{ name: 'Minimize game window', done: true },
		{ name: 'Creativity and Charisma skills', done: false },
		{ name: 'Pets', done: false },
		{ name: 'Multiple rooms', done: false },
		{ name: 'Roommates', done: false },
		{ name: 'Create your own pixel art masterpieces', done: false },
		{ name: 'Multiplayer snail mail system', done: false }
	];

	const PK = '/images/mini-me-mao/presskit';

	// Drop the trailer zip into static/press/ and fill these in to enable the download button.
	const trailerZip = '';
	const trailerZipMeta = '';

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

	const contacts = [
		{
			label: 'Email',
			value: 'press@sleepingrobotgames.com',
			href: 'mailto:press@sleepingrobotgames.com'
		},
		{ label: 'Discord', value: 'discord.gg/zAxUhJ4F2H', href: 'https://discord.gg/zAxUhJ4F2H' },
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
		content="Press kit for Mini Me-Mao, a cozy desktop companion from Sleeping Robot Games. Factsheet, descriptions, key art, screenshots, logos, and press contact."
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
	<!-- Header -->
	<header class="mm-pk-hero">
		<picture>
			<source media="(min-width: 700px)" srcset="/images/mini-me-mao/presskit/libraryhero.jpg" />
			<img
				src="/images/mini-me-mao/presskit/itchcapsule.jpg"
				alt=""
				class="mm-pk-hero-bg"
				aria-hidden="true"
			/>
		</picture>
		<div class="mm-pk-hero-scrim"></div>
		<div class="mm-pk-hero-content">
			<img
				src="/images/mini-me-mao/presskit/Mini_Memao_Title.png"
				alt="Mini Me-Mao"
				class="mm-pk-hero-logo"
			/>
			<p class="mm-pk-eyebrow">Press Kit</p>
			<p class="mm-pk-hero-tagline">A tiny companion that lives right on your desktop</p>
			<div class="mm-hero-ctas mm-pk-hero-ctas">
				<a href="#video" class="mm-btn mm-btn-primary">
					<IconFilm class="h-4 w-4" />
					Watch the trailer
				</a>
				<a href="mailto:press@sleepingrobotgames.com" class="mm-btn mm-btn-ghost">
					<IconMail class="h-4 w-4" />
					Press contact
				</a>
			</div>
		</div>
	</header>

	<main>
		<!-- Overview: factsheet + copy -->
		<section class="mm-section mm-overview" id="factsheet">
			<aside class="mm-overview-side">
				<h2 class="mm-h2 mm-h2-left">Factsheet</h2>
				<dl class="mm-facts mm-facts-compact">
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
			</aside>

			<div class="mm-overview-main">
				<div id="description" class="mm-copy">
					<h2 class="mm-h2 mm-h2-left">Description</h2>
					<p class="mm-quote">
						A mini companion that lives right on your desktop! Unpack and decorate a cozy desktop
						dollhouse, dress up your mini, and watch them paint while you work or play. Sell their
						art for gold, unlock new painting styles, collect charming decorations, and create the
						perfect space that grows with you.
					</p>
				</div>

				<div id="features">
					<h2 class="mm-h2 mm-h2-left">Features</h2>
					<div class="mm-quote">
						<ul class="mm-bullets">
							{#each features as f}
								<li>{f}</li>
							{/each}
						</ul>
					</div>
				</div>
			</div>
		</section>

		<!-- Video -->
		<section class="mm-section" id="video">
			<h2 class="mm-h2">Video</h2>
			<p class="mm-section-sub">
				The announcement trailer is still in production. Email
				<a href="mailto:press@sleepingrobotgames.com">press@sleepingrobotgames.com</a> and we’ll send
				it over the moment it’s ready.
			</p>
			<div class="mm-video-grid">
				<figure class="mm-video">
					<div class="mm-placeholder mm-placeholder-wide">
						<IconFilm class="h-7 w-7" />
						<p class="mm-placeholder-title">Coming soon</p>
					</div>
					<figcaption>
						<span class="mm-asset-name">Trailer, horizontal</span>
						<span class="mm-asset-meta">16:9 · 1920×1080</span>
					</figcaption>
				</figure>
				<figure class="mm-video">
					<div class="mm-placeholder mm-placeholder-tall">
						<IconSmartphone class="h-7 w-7" />
						<p class="mm-placeholder-title">Coming soon</p>
					</div>
					<figcaption>
						<span class="mm-asset-name">Trailer, vertical</span>
						<span class="mm-asset-meta">9:16 · 1080×1920</span>
					</figcaption>
				</figure>
			</div>
			{#if trailerZip}
				<a class="mm-btn mm-btn-zip" href={trailerZip} download>
					<IconFolderDown class="h-4 w-4" />
					Download all trailers
					<span class="mm-zip-meta">{trailerZipMeta}</span>
				</a>
			{:else}
				<span class="mm-btn mm-btn-zip mm-btn-zip-off" aria-disabled="true">
					<IconFolderDown class="h-4 w-4" />
					Download all trailers
					<span class="mm-zip-meta">Available once the trailer lands</span>
				</span>
			{/if}
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
			<a class="mm-btn mm-btn-zip" href="/press/mini-me-mao-key-art.zip" download>
				<IconFolderDown class="h-4 w-4" />
				Download all key art
				<span class="mm-zip-meta">ZIP · 7.8 MB</span>
			</a>

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
			<a class="mm-btn mm-btn-zip" href="/press/mini-me-mao-screenshots.zip" download>
				<IconFolderDown class="h-4 w-4" />
				Download all screenshots
				<span class="mm-zip-meta">ZIP · 7.5 MB</span>
			</a>

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
			<a class="mm-btn mm-btn-zip" href="/press/mini-me-mao-logos.zip" download>
				<IconFolderDown class="h-4 w-4" />
				Download all logos
				<span class="mm-zip-meta">ZIP · 1.8 MB</span>
			</a>

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
			<a class="mm-btn mm-btn-zip" href="/press/mini-me-mao-animations.zip" download>
				<IconFolderDown class="h-4 w-4" />
				Download all animations
				<span class="mm-zip-meta">ZIP · 68 KB</span>
			</a>
		</section>

		<!-- Roadmap -->
		<section class="mm-section" id="roadmap">
			<h2 class="mm-h2">Roadmap</h2>
			<p class="mm-section-sub">Mini Me-Mao is in active development.</p>
			<ul class="mm-roadmap">
				{#each roadmap as r}
					<li class:mm-road-done={r.done}>
						{#if r.done}
							<IconCheck class="mm-road-icon h-4 w-4" />
						{:else}
							<span class="mm-road-dot"></span>
						{/if}
						<span>{r.name}</span>
						{#if r.done}<span class="mm-road-tag">Shipped</span>{/if}
					</li>
				{/each}
			</ul>
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
	:global(.mm-btn) {
		font-family: 'Baloo 2 Variable', sans-serif;
	}

	/* Hero */
	.mm-pk-hero {
		position: relative;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		text-align: center;
		min-height: min(62vh, 560px);
		padding: 3.5rem 1.5rem 3rem;
		background: var(--mm-bg-2);
		border-bottom: 1px solid rgba(255, 255, 255, 0.06);
		overflow: hidden;
	}

	.mm-pk-hero picture {
		position: absolute;
		inset: 0;
	}

	.mm-pk-hero-bg {
		position: absolute;
		inset: 0;
		width: 100%;
		height: 100%;
		object-fit: cover;
		object-position: 50% 45%;
	}

	.mm-pk-hero-scrim {
		position: absolute;
		inset: 0;
		background: linear-gradient(
				180deg,
				rgba(20, 10, 20, 0.55) 0%,
				rgba(20, 10, 20, 0.68) 55%,
				rgba(32, 19, 32, 0.96) 100%
			),
			radial-gradient(
				ellipse 70% 60% at 50% 45%,
				rgba(20, 10, 20, 0.62),
				rgba(20, 10, 20, 0.35) 100%
			);
	}

	.mm-pk-hero-content {
		position: relative;
		z-index: 1;
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.mm-pk-hero-logo {
		width: min(340px, 72vw);
		height: auto;
		display: block;
		filter: drop-shadow(0 6px 20px rgba(0, 0, 0, 0.7));
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
		text-shadow: 0 2px 10px rgba(0, 0, 0, 0.55);
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

	/* Overview two-column */
	.mm-overview {
		display: grid;
		grid-template-columns: 1fr;
		gap: 2.5rem;
		align-items: start;
	}

	@media (min-width: 900px) {
		.mm-overview {
			grid-template-columns: minmax(0, 300px) minmax(0, 1fr);
			gap: 3rem;
		}
		.mm-overview-side {
			position: sticky;
			top: 4.5rem;
		}
	}

	.mm-overview-main {
		display: grid;
		gap: 2.5rem;
		min-width: 0;
	}

	.mm-h2-left {
		text-align: left;
		font-size: clamp(1.35rem, 2.4vw, 1.7rem);
		margin-bottom: 0.9rem;
	}

	.mm-overview .mm-copy,
	.mm-overview .mm-bullets {
		max-width: none;
		margin-left: 0;
		margin-right: 0;
	}

	.mm-overview .mm-copy {
		margin-top: 0;
	}

	.mm-overview .mm-bullets {
		margin-top: 0;
	}

	/* Compact factsheet for the side rail */
	.mm-facts-compact {
		margin: 0;
		max-width: none;
		border-radius: 16px;
	}

	.mm-facts-compact .mm-fact {
		grid-template-columns: 1fr;
		gap: 0.1rem;
		padding: 0.7rem 1rem;
	}

	.mm-facts-compact dt {
		font-size: 0.7rem;
		letter-spacing: 0.08em;
	}

	.mm-facts-compact dd {
		font-size: 0.88rem;
		line-height: 1.45;
	}

	.mm-facts-compact .mm-todo {
		font-size: 0.78rem;
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

	/* Features */
	.mm-bullets {
		margin: 0;
		padding: 0;
		list-style: none;
		display: grid;
		gap: 0.6rem;
	}

	.mm-bullets li {
		position: relative;
		padding-left: 1.3rem;
		color: var(--mm-cream);
		font-size: 0.95rem;
	}

	.mm-bullets li::before {
		content: '';
		position: absolute;
		left: 0;
		top: 0.62rem;
		width: 7px;
		height: 7px;
		border-radius: 999px;
		background: var(--mm-pink);
	}

	/* Roadmap */
	.mm-roadmap {
		max-width: 760px;
		margin: 2rem auto 0;
		padding: 0;
		list-style: none;
		display: grid;
		gap: 0.6rem;
	}

	.mm-roadmap li {
		display: flex;
		align-items: center;
		gap: 0.7rem;
		background: var(--mm-panel);
		border: 1px solid rgba(255, 255, 255, 0.06);
		border-radius: 14px;
		padding: 0.8rem 1.1rem;
		color: var(--mm-cream);
		font-size: 0.95rem;
	}

	.mm-roadmap li.mm-road-done {
		color: var(--mm-cream-dim);
	}

	:global(.mm-road-icon) {
		color: #7ee0a8;
		flex-shrink: 0;
	}

	.mm-road-dot {
		width: 7px;
		height: 7px;
		margin: 0 3.5px;
		border-radius: 999px;
		background: var(--mm-pink);
		flex-shrink: 0;
	}

	.mm-road-tag {
		margin-left: auto;
		font-family: 'Baloo 2 Variable', sans-serif;
		font-size: 0.7rem;
		font-weight: 700;
		text-transform: uppercase;
		letter-spacing: 0.06em;
		color: #7ee0a8;
		background: rgba(126, 224, 168, 0.14);
		border-radius: 999px;
		padding: 0.15rem 0.55rem;
		white-space: nowrap;
	}

	/* Video placeholder */
	.mm-video-grid {
		margin: 2rem auto 0;
		max-width: 900px;
		display: grid;
		grid-template-columns: 1fr;
		gap: 1.5rem;
		justify-items: center;
	}

	@media (min-width: 700px) {
		.mm-video-grid {
			grid-template-columns: minmax(0, 2fr) minmax(0, 1fr);
			align-items: center;
			justify-items: stretch;
		}
	}

	.mm-video {
		margin: 0;
		display: flex;
		flex-direction: column;
		width: 100%;
		max-width: 380px;
	}

	@media (min-width: 700px) {
		.mm-video {
			max-width: none;
		}
	}

	.mm-video figcaption {
		display: flex;
		flex-direction: column;
		gap: 0.15rem;
		padding-top: 0.7rem;
	}

	.mm-placeholder-wide {
		aspect-ratio: 16 / 9;
	}

	.mm-placeholder-tall {
		aspect-ratio: 9 / 16;
	}

	.mm-placeholder {
		margin: 0;
		width: 100%;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
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

	:global(.mm-btn-zip) {
		display: flex;
		width: fit-content;
		margin: 1.1rem auto 0;
		background: var(--mm-panel);
		color: var(--mm-cream);
		border-color: rgba(255, 63, 174, 0.35);
		font-size: 0.9rem;
		padding: 0.6rem 1.1rem;
	}
	:global(a.mm-btn-zip:hover) {
		border-color: var(--mm-pink);
		color: var(--mm-pink-soft);
	}

	:global(.mm-btn-zip-off) {
		cursor: default;
		opacity: 0.55;
		border-color: rgba(255, 255, 255, 0.18);
	}

	.mm-zip-meta {
		font-size: 0.75rem;
		font-weight: 600;
		color: var(--mm-cream-dim);
		opacity: 0.8;
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
