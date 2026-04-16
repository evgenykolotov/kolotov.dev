<svelte:head>
	<title>kolotov.dev</title>
	<meta
		name="description"
		content="Новая версия kolotov.dev находится в разработке и скоро появится."
	/>
</svelte:head>

<main class="holding-page">
	<div class="background-layer" aria-hidden="true">
		<div class="orb orb-blue"></div>
		<div class="orb orb-violet"></div>
		<div class="orb orb-mint"></div>
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
			radial-gradient(circle at top left, rgba(21, 93, 252, 0.08), transparent 24%),
			linear-gradient(180deg, #ffffff 0%, #f8fafc 100%);
		color: #0a0a0a;
	}

	.holding-page {
		position: relative;
		min-height: 100svh;
		overflow: clip;
		padding: 1rem;
		isolation: isolate;
	}

	.background-layer {
		position: absolute;
		inset: 0;
		pointer-events: none;
	}

	.orb {
		position: absolute;
		border-radius: 999px;
		filter: blur(90px);
		opacity: 0.7;
		animation: float-orb 18s ease-in-out infinite;
	}

	.orb-blue {
		top: 10%;
		left: 8%;
		width: 20rem;
		height: 20rem;
		background: rgba(21, 93, 252, 0.16);
	}

	.orb-violet {
		right: 10%;
		top: 18%;
		width: 26rem;
		height: 26rem;
		background: rgba(152, 16, 250, 0.1);
		animation-delay: -6s;
	}

	.orb-mint {
		bottom: 12%;
		left: 38%;
		width: 18rem;
		height: 18rem;
		background: rgba(16, 185, 129, 0.08);
		animation-delay: -11s;
	}

	.grid {
		position: absolute;
		inset: 0;
		background-image:
			linear-gradient(rgba(243, 244, 246, 0.7) 1px, transparent 1px),
			linear-gradient(90deg, rgba(243, 244, 246, 0.7) 1px, transparent 1px);
		background-size: 4.5rem 4.5rem;
		mask-image: radial-gradient(circle at center, black 28%, transparent 82%);
		opacity: 0.45;
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
		border: 1px solid rgba(243, 244, 246, 0.95);
		border-radius: 1.25rem;
		background: rgba(255, 255, 255, 0.8);
		backdrop-filter: blur(16px);
		animation: rise-in 0.75s cubic-bezier(0.22, 1, 0.36, 1) both;
	}

	.brand {
		color: #101828;
		font-size: 1.125rem;
		font-weight: 700;
		letter-spacing: -0.03em;
		text-decoration: none;
	}

	.brand-accent {
		color: #155dfc;
	}

	.topbar-note {
		margin: 0;
		color: #4a5565;
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
		padding: 4rem 1.5rem 2rem;
		text-align: center;
	}

	.hero-shell::before {
		content: '';
		position: absolute;
		inset: 9% 12%;
		border: 1px solid rgba(243, 244, 246, 0.95);
		border-radius: 2rem;
		background: linear-gradient(
			180deg,
			rgba(255, 255, 255, 0.82) 0%,
			rgba(248, 250, 252, 0.68) 100%
		);
		box-shadow:
			0 30px 60px -42px rgba(15, 23, 42, 0.18),
			inset 0 1px 0 rgba(255, 255, 255, 0.8);
		backdrop-filter: blur(22px);
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
		border-radius: 999px;
		background: #eff6ff;
		color: #155dfc;
		font-size: 0.875rem;
		letter-spacing: -0.01em;
		animation: rise-in 0.75s 0.08s cubic-bezier(0.22, 1, 0.36, 1) both;
	}

	.status-dot {
		width: 0.5rem;
		height: 0.5rem;
		border-radius: 999px;
		background: #155dfc;
		box-shadow: 0 0 0 0 rgba(21, 93, 252, 0.36);
		animation: pulse-dot 2.8s ease-out infinite;
	}

	.hero-copy {
		display: grid;
		gap: 1rem;
		max-width: 48rem;
	}

	.eyebrow {
		margin: 0;
		color: #4a5565;
		font-size: 0.875rem;
		letter-spacing: 0.14em;
		text-transform: uppercase;
		animation: rise-in 0.75s 0.16s cubic-bezier(0.22, 1, 0.36, 1) both;
	}

	h1 {
		margin: 0;
		font-size: clamp(3rem, 8vw, 4.5rem);
		font-weight: 600;
		line-height: 0.96;
		letter-spacing: -0.055em;
		color: #0a0a0a;
		animation: rise-in 0.75s 0.24s cubic-bezier(0.22, 1, 0.36, 1) both;
	}

	.accent-line {
		display: block;
		background: linear-gradient(90deg, #0a0a0a 0%, #155dfc 45%, #9810fa 100%);
		background-size: 170% 100%;
		background-clip: text;
		-webkit-background-clip: text;
		color: transparent;
		animation: accent-shift 6s ease-in-out infinite;
	}

	.lead {
		margin: 0 auto;
		max-width: 40rem;
		color: #4a5565;
		font-size: clamp(1rem, 2vw, 1.25rem);
		line-height: 1.6;
		letter-spacing: -0.02em;
		animation: rise-in 0.75s 0.32s cubic-bezier(0.22, 1, 0.36, 1) both;
	}

	.light-band {
		position: relative;
		width: min(38rem, 72vw);
		height: 0.625rem;
		border-radius: 999px;
		background: rgba(243, 244, 246, 0.95);
		overflow: hidden;
		animation: rise-in 0.75s 0.4s cubic-bezier(0.22, 1, 0.36, 1) both;
	}

	.band-glow {
		position: absolute;
		inset: 0;
		border-radius: inherit;
		background: linear-gradient(
			90deg,
			rgba(21, 93, 252, 0) 0%,
			rgba(21, 93, 252, 0.8) 42%,
			rgba(152, 16, 250, 0.75) 58%,
			rgba(152, 16, 250, 0) 100%
		);
		transform: translateX(-120%);
		animation: sweep-band 4.8s ease-in-out infinite;
	}

	.info-row {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 0.75rem;
		max-width: 44rem;
		animation: rise-in 0.75s 0.48s cubic-bezier(0.22, 1, 0.36, 1) both;
	}

	.info-row p {
		margin: 0;
		padding: 0.875rem 1.125rem;
		border: 1px solid #f3f4f6;
		border-radius: 0.875rem;
		background: rgba(255, 255, 255, 0.78);
		color: #364153;
		font-size: 1rem;
		letter-spacing: -0.02em;
		box-shadow: 0 16px 40px -36px rgba(15, 23, 42, 0.22);
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
			box-shadow: 0 0 0 0 rgba(21, 93, 252, 0.32);
		}

		70% {
			box-shadow: 0 0 0 0.65rem rgba(21, 93, 252, 0);
		}

		100% {
			box-shadow: 0 0 0 0 rgba(21, 93, 252, 0);
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
			padding: 0.75rem;
		}

		.topbar {
			padding-inline: 1rem;
			border-radius: 1rem;
		}

		.topbar-note {
			display: none;
		}

		.hero-shell {
			padding: 3rem 1rem 1.5rem;
			gap: 1.5rem;
		}

		.hero-shell::before {
			inset: 6% 0;
			border-radius: 1.5rem;
		}

		.lead {
			max-width: 32rem;
		}

		.info-row {
			max-width: 22rem;
		}

		.info-row p {
			width: 100%;
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
