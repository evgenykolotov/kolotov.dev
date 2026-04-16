<svelte:head>
	<title>kolotov.dev</title>
	<meta
		name="description"
		content="Новая версия kolotov.dev находится в разработке и скоро появится."
	/>
	<meta name="robots" content="noindex, nofollow" />
	<meta name="theme-color" content="#ffffff" />
	<link rel="canonical" href="https://kolotov.dev/" />
	<meta property="og:title" content="kolotov.dev" />
	<meta
		property="og:description"
		content="Новая версия kolotov.dev находится в разработке и скоро появится."
	/>
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://kolotov.dev/" />
	<meta property="og:image" content="https://kolotov.dev/og-image.png" />
	<meta property="og:locale" content="ru_RU" />
	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:title" content="kolotov.dev" />
	<meta
		name="twitter:description"
		content="Новая версия kolotov.dev находится в разработке и скоро появится."
	/>
	<meta name="twitter:image" content="https://kolotov.dev/og-image.png" />
</svelte:head>

<main class="holding-page">
	<div class="background-layer" aria-hidden="true">
		<div class="orb orb-blue"></div>
		<div class="orb orb-cool"></div>
		<div class="orb orb-soft"></div>
		<div class="grid"></div>
	</div>

	<header class="topbar">
		<a class="brand" href="/" aria-label="kolotov.dev home">
			<span>kolotov</span><span class="brand-accent">.</span><span>dev</span>
		</a>
		<p class="topbar-note">launching soon</p>
	</header>

	<section class="hero-shell" aria-labelledby="hero-title">
		<p class="status-pill">
			<span class="status-dot"></span>
			Сайт в разработке
		</p>

		<div class="hero-copy">
			<p class="eyebrow">новая версия kolotov.dev</p>
			<h1 id="hero-title">
				Скоро здесь появится
				<span class="accent-line">новый сайт</span>
			</h1>
			<p class="lead">
				Готовлю минималистичное пространство с проектами, кейсами и продуманной подачей. Пока
				страница находится в разработке.
			</p>
			<p class="contact-line">
				<a href="https://t.me/evgenykolotov_dev" rel="me noopener noreferrer" target="_blank">
					Telegram: @evgenykolotov_dev
				</a>
			</p>
		</div>

		<div class="light-band" aria-hidden="true">
			<span class="band-glow"></span>
		</div>

		<div class="info-row" aria-label="Site status highlights">
			<p>Минималистичный интерфейс</p>
			<p>Системная типографика</p>
			<p>Запуск скоро</p>
		</div>
	</section>
</main>

<style>
	:global(body) {
		background:
			radial-gradient(circle at top left, var(--color-accent-subtle), transparent 24%),
			linear-gradient(180deg, var(--color-surface) 0%, var(--color-surface-soft) 100%);
		color: var(--color-ink);
	}

	.holding-page {
		position: relative;
		min-height: 100svh;
		overflow: clip;
		padding: var(--space-page);
		isolation: isolate;
	}

	.background-layer {
		position: absolute;
		inset: 0;
		pointer-events: none;
	}

	.orb {
		position: absolute;
		border-radius: var(--radius-pill);
		filter: blur(var(--blur-orb));
		opacity: 0.7;
		animation: float-orb var(--duration-float) ease-in-out infinite;
	}

	.orb-blue {
		top: 10%;
		left: 8%;
		width: 20rem;
		height: 20rem;
		background: var(--color-accent-glow);
	}

	.orb-cool {
		right: 10%;
		top: 18%;
		width: 26rem;
		height: 26rem;
		background: var(--color-accent-cool-soft);
		animation-delay: -6s;
	}

	.orb-soft {
		bottom: 12%;
		left: 38%;
		width: 18rem;
		height: 18rem;
		background: var(--color-accent-soft);
		animation-delay: -11s;
	}

	.grid {
		position: absolute;
		inset: 0;
		background-image:
			linear-gradient(var(--color-line-faint) 1px, transparent 1px),
			linear-gradient(90deg, var(--color-line-faint) 1px, transparent 1px);
		background-size: 4.5rem 4.5rem;
		mask-image: radial-gradient(circle at center, black 28%, transparent 82%);
		opacity: 0.3;
	}

	.topbar {
		position: relative;
		z-index: 1;
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 1rem;
		height: 4rem;
		padding: 1rem 1.5rem;
		margin: 0 auto;
		max-width: 85.625rem;
		border: 1px solid var(--color-line-overlay);
		border-radius: var(--radius-topbar);
		background: var(--color-surface-topbar);
		backdrop-filter: blur(var(--blur-topbar));
		animation: rise-in var(--duration-enter) var(--ease-smooth) both;
	}

	.brand {
		color: var(--color-ink);
		font-size: 1.125rem;
		font-weight: 700;
		letter-spacing: -0.03em;
		text-decoration: none;
	}

	.brand-accent {
		color: var(--color-accent);
	}

	.topbar-note {
		margin: 0;
		color: var(--color-muted);
		font-size: 0.875rem;
		letter-spacing: 0.08em;
		text-transform: uppercase;
	}

	.hero-shell {
		position: relative;
		z-index: 1;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		gap: 2rem;
		min-height: calc(100svh - 6rem);
		max-width: 85.625rem;
		margin: 0 auto;
		padding: var(--space-shell-y) var(--space-shell-x) 2rem;
		text-align: center;
	}

	.hero-shell::before {
		content: '';
		position: absolute;
		inset: 9% 12%;
		border: 1px solid var(--color-line-overlay);
		border-radius: var(--radius-panel);
		background: linear-gradient(
			180deg,
			var(--color-surface-panel-start) 0%,
			var(--color-surface-panel-end) 100%
		);
		box-shadow: var(--shadow-panel);
		backdrop-filter: blur(var(--blur-panel));
	}

	.hero-shell > * {
		position: relative;
	}

	.status-pill {
		display: inline-flex;
		align-items: center;
		gap: 0.625rem;
		margin: 0;
		padding: 0.5rem 1rem;
		border-radius: var(--radius-pill);
		background: var(--color-surface-accent);
		color: var(--color-accent);
		font-size: 0.875rem;
		letter-spacing: -0.01em;
		animation: rise-in var(--duration-enter) 0.08s var(--ease-smooth) both;
	}

	.status-dot {
		width: 0.5rem;
		height: 0.5rem;
		border-radius: var(--radius-pill);
		background: var(--color-accent);
		box-shadow: 0 0 0 0 var(--color-accent-ring);
		animation: pulse-dot var(--duration-pulse) ease-out infinite;
	}

	.hero-copy {
		display: grid;
		gap: 1rem;
		max-width: 48rem;
	}

	.eyebrow {
		margin: 0;
		color: var(--color-muted);
		font-size: 0.875rem;
		letter-spacing: 0.14em;
		text-transform: uppercase;
		animation: rise-in var(--duration-enter) 0.16s var(--ease-smooth) both;
	}

	h1 {
		margin: 0;
		font-size: clamp(3rem, 8vw, 4.5rem);
		font-weight: 600;
		line-height: 0.96;
		letter-spacing: -0.055em;
		color: var(--color-ink);
		animation: rise-in var(--duration-enter) 0.24s var(--ease-smooth) both;
	}

	.accent-line {
		display: block;
		background: linear-gradient(
			90deg,
			var(--color-ink) 0%,
			var(--color-accent) 45%,
			var(--color-accent-cool) 100%
		);
		background-size: 170% 100%;
		background-clip: text;
		-webkit-background-clip: text;
		color: transparent;
		animation: accent-shift var(--duration-accent) ease-in-out infinite;
	}

	.lead {
		margin: 0 auto;
		max-width: 40rem;
		color: var(--color-muted);
		font-size: clamp(1rem, 2vw, 1.25rem);
		line-height: 1.6;
		letter-spacing: -0.02em;
		animation: rise-in var(--duration-enter) 0.32s var(--ease-smooth) both;
	}

	.contact-line {
		margin: 0;
		font-size: 0.9375rem;
		letter-spacing: -0.02em;
		animation: rise-in var(--duration-enter) 0.38s var(--ease-smooth) both;
	}

	.contact-line a {
		color: var(--color-text);
		text-decoration: none;
		border-bottom: 1px solid color-mix(in srgb, var(--color-accent) 22%, transparent);
		transition:
			color 180ms ease,
			border-color 180ms ease;
	}

	.contact-line a:hover,
	.contact-line a:focus-visible {
		color: var(--color-accent);
		border-color: color-mix(in srgb, var(--color-accent) 60%, transparent);
	}

	.light-band {
		position: relative;
		width: min(38rem, 72vw);
		height: 0.625rem;
		border-radius: var(--radius-pill);
		background: var(--color-line-overlay);
		overflow: hidden;
		animation: rise-in var(--duration-enter) 0.4s var(--ease-smooth) both;
	}

	.band-glow {
		position: absolute;
		inset: 0;
		border-radius: inherit;
		background: linear-gradient(
			90deg,
			transparent 0%,
			var(--color-accent-strong) 42%,
			var(--color-accent-cool-strong) 58%,
			transparent 100%
		);
		transform: translateX(-120%);
		animation: sweep-band var(--duration-band) ease-in-out infinite;
	}

	.info-row {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 0.75rem;
		max-width: 44rem;
		animation: rise-in var(--duration-enter) 0.48s var(--ease-smooth) both;
	}

	.info-row p {
		margin: 0;
		padding: 0.875rem 1.125rem;
		border: 1px solid var(--color-line);
		border-radius: var(--radius-card);
		background: var(--color-surface-overlay);
		color: var(--color-text);
		font-size: 1rem;
		letter-spacing: -0.02em;
		box-shadow: var(--shadow-card);
	}

	@keyframes rise-in {
		from {
			opacity: 0;
			transform: translateY(1rem);
		}

		to {
			opacity: 1;
			transform: translateY(0);
		}
	}

	@keyframes float-orb {
		0%,
		100% {
			transform: translate3d(0, 0, 0) scale(1);
		}

		50% {
			transform: translate3d(1.5rem, -1.25rem, 0) scale(1.08);
		}
	}

	@keyframes pulse-dot {
		0% {
			box-shadow: 0 0 0 0 var(--color-accent-ring);
		}

		70% {
			box-shadow: 0 0 0 0.65rem transparent;
		}

		100% {
			box-shadow: 0 0 0 0 transparent;
		}
	}

	@keyframes accent-shift {
		0%,
		100% {
			background-position: 0% 50%;
		}

		50% {
			background-position: 100% 50%;
		}
	}

	@keyframes sweep-band {
		0% {
			transform: translateX(-120%);
		}

		50% {
			transform: translateX(120%);
		}

		100% {
			transform: translateX(120%);
		}
	}

	@media (max-width: 48rem) {
		.holding-page {
			padding: var(--space-page-compact);
		}

		.grid {
			opacity: 0.2;
		}

		.orb-blue {
			width: 15rem;
			height: 15rem;
		}

		.orb-cool {
			width: 18rem;
			height: 18rem;
			right: -12%;
			top: 14%;
		}

		.orb-soft {
			width: 14rem;
			height: 14rem;
			left: 48%;
			bottom: 10%;
		}

		.topbar {
			height: 3.5rem;
			padding-inline: 1rem;
			border-radius: var(--radius-topbar-compact);
		}

		.topbar-note {
			display: none;
		}

		.hero-shell {
			padding: var(--space-shell-y-compact) 1rem 1.5rem;
			gap: 1.5rem;
			min-height: calc(100svh - 5rem);
		}

		.hero-shell::before {
			inset: 7% 0.25rem 2% 0.25rem;
			border-radius: var(--radius-panel-compact);
			box-shadow: 0 24px 48px -40px rgba(15, 23, 42, 0.16);
		}

		.hero-copy {
			gap: 0.75rem;
		}

		.eyebrow {
			font-size: 0.8125rem;
			letter-spacing: 0.12em;
		}

		h1 {
			font-size: clamp(2.625rem, 14vw, 3.75rem);
			line-height: 0.92;
			letter-spacing: -0.06em;
		}

		.lead {
			max-width: 32rem;
			font-size: 1rem;
			line-height: 1.5;
		}

		.contact-line {
			font-size: 0.875rem;
		}

		.light-band {
			width: min(20rem, 78vw);
			height: 0.5rem;
		}

		.info-row {
			max-width: 22rem;
			gap: 0.625rem;
		}

		.info-row p {
			width: 100%;
			padding: 0.75rem 0.9375rem;
			border-radius: 0.75rem;
			font-size: 0.9375rem;
			box-shadow: 0 12px 32px -32px rgba(15, 23, 42, 0.2);
		}
	}

	@media (max-width: 30rem) {
		.status-pill {
			padding-inline: 0.875rem;
			font-size: 0.8125rem;
		}

		.hero-shell {
			padding: 2.75rem 0.875rem 1.25rem;
			gap: 1.25rem;
		}

		.hero-shell::before {
			inset: 6% 0 1.5% 0;
		}

		.lead {
			max-width: 19rem;
		}

		.contact-line {
			line-height: 1.45;
		}
	}

	@media (prefers-reduced-motion: reduce) {
		.orb,
		.status-dot,
		.accent-line,
		.band-glow,
		.topbar,
		.status-pill,
		.eyebrow,
		h1,
		.lead,
		.light-band,
		.info-row {
			animation: none;
		}
	}
</style>
