<script lang="ts">
	import { onMount } from 'svelte';

	onMount(() => {
		const cats = [
			{ name: 'Doodles', lvl: 0, min: 25, max: 75 },
			{ name: 'Miniature', lvl: 2, min: 50, max: 100 },
			{ name: 'Landscape', lvl: 4, min: 75, max: 125 },
			{ name: 'Pop', lvl: 6, min: 100, max: 150 },
			{ name: 'Memao', lvl: 8, min: 125, max: 175 },
			{ name: 'Master', lvl: 10, min: 150, max: 200 }
		];
		const STAR_MULT = [0.6, 0.8, 1.0, 1.3, 1.7];

		const getInput = (id: string) => document.getElementById(id) as HTMLInputElement;
		const getOutput = (id: string) => document.getElementById(id) as HTMLSpanElement;
		const lerp = (a: number, b: number, t: number) => a + (b - a) * t;

		function calc() {
			const c = cats[Number(getInput('s_cat').value)];
			const star = Number(getInput('s_star').value);
			const logicLvl = Number(getInput('s_logic').value);
			const insp = Number(getInput('s_insp').value);
			const hun = Number(getInput('s_hun').value);

			const sMult = STAR_MULT[star - 1];
			const logicMult = 1 + logicLvl * 0.1;
			const inspMult = lerp(0.7, 1.3, insp / 100);
			const hunMult = lerp(0.7, 1.0, Math.min(hun / 50, 1));
			const combo = sMult * logicMult * inspMult * hunMult;
			const mid = (c.min + c.max) / 2;

			getOutput('o_cat').textContent = `${c.name} (Lv ${c.lvl})`;
			getOutput('o_star').textContent = `${star}★ ×${sMult.toFixed(1)}`;
			getOutput('o_logic').textContent = `Lv ${logicLvl} ×${logicMult.toFixed(1)}`;
			getOutput('o_insp').textContent = `${insp}% ×${inspMult.toFixed(2)}`;
			getOutput('o_hun').textContent = `${hun}% ×${hunMult.toFixed(2)}`;

			getOutput('b_base').textContent = String(Math.round(mid));
			getOutput('b_star').textContent = sMult.toFixed(2);
			getOutput('b_logic').textContent = logicMult.toFixed(2);
			getOutput('b_insp').textContent = inspMult.toFixed(2);
			getOutput('b_hun').textContent = hunMult.toFixed(2);

			getOutput('o_final').textContent = String(Math.round(mid * combo));
			getOutput('o_range').textContent = `${Math.round(c.min * combo)}…${Math.round(c.max * combo)} g`;
		}

		['s_cat', 's_star', 's_logic', 's_insp', 's_hun'].forEach((id) =>
			getInput(id).addEventListener('input', calc)
		);
		calc();
	});
</script>

<svelte:head>
	<title>Mini Me Mao — Painting Sale-Price Calculator</title>
</svelte:head>

<div class="page">
	<h1>Painting sale-price calculator</h1>
	<p class="sub">Mini Me Mao — models the gold value a finished painting sells for.</p>

	<div class="formula">value = base(gold_min…gold_max) × star × (1 + logic×0.1) × inspiration × hunger</div>

	<div class="gb-card">
		<div class="gb-row">
			<span class="gb-lbl">Category</span>
			<input type="range" id="s_cat" min="0" max="5" step="1" value="0" style="flex:1" />
			<span class="gb-out" id="o_cat">Doodles</span>
		</div>
		<div class="gb-row">
			<span class="gb-lbl">Star tier</span>
			<input type="range" id="s_star" min="1" max="5" step="1" value="3" style="flex:1" />
			<span class="gb-out" id="o_star">3★ ×1.0</span>
		</div>
		<div class="gb-row">
			<span class="gb-lbl">Logic skill</span>
			<input type="range" id="s_logic" min="0" max="10" step="1" value="0" style="flex:1" />
			<span class="gb-out" id="o_logic">Lv 0 ×1.0</span>
		</div>
		<div class="gb-row">
			<span class="gb-lbl">Inspiration</span>
			<input type="range" id="s_insp" min="0" max="100" step="1" value="50" style="flex:1" />
			<span class="gb-out" id="o_insp">50% ×1.0</span>
		</div>
		<div class="gb-row">
			<span class="gb-lbl">Hunger</span>
			<input type="range" id="s_hun" min="0" max="100" step="1" value="50" style="flex:1" />
			<span class="gb-out" id="o_hun">50% ×1.0</span>
		</div>

		<div
			style="border-top:0.5px solid var(--border); margin-top:14px; padding-top:14px; display:flex; align-items:flex-end; justify-content:space-between; gap:16px; flex-wrap:wrap;"
		>
			<div>
				<div class="gb-chip" style="margin-bottom:4px">Expected sale price (mid-range roll)</div>
				<div class="gb-final"><span id="o_final">45</span><span style="font-size:22px; font-weight:400"> g</span></div>
			</div>
			<div class="gb-chip" style="text-align:right; line-height:1.9">
				<div>base <span class="gb-mult" id="b_base">50</span></div>
				<div>× star <span class="gb-mult" id="b_star">1.00</span></div>
				<div>× logic <span class="gb-mult" id="b_logic">1.00</span></div>
				<div>× insp <span class="gb-mult" id="b_insp">1.00</span></div>
				<div>× hunger <span class="gb-mult" id="b_hun">1.00</span></div>
			</div>
		</div>
		<div class="gb-chip" style="margin-top:10px">
			Range with min…max roll: <span id="o_range" style="font-weight:500; color:var(--text-primary)">30…60 g</span>
		</div>
	</div>
</div>

<style>
	:global(html),
	:global(body) {
		margin: 0;
		background: #1a1a19;
		color: #ffffff;
		font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial,
			sans-serif;
		line-height: 1.6;
		-webkit-font-smoothing: antialiased;
	}

	:global(*) {
		box-sizing: border-box;
	}

	.page {
		max-width: 560px;
		margin: 0 auto;
		padding: 2rem 1.25rem 3rem;
	}

	h1 {
		font-size: 22px;
		font-weight: 500;
		margin: 0 0 0.25rem;
	}

	.sub {
		color: #c3c2b7;
		font-size: 14px;
		margin: 0 0 1.5rem;
	}

	.formula {
		background: #2c2c2a;
		border: 0.5px solid rgba(255, 255, 255, 0.12);
		border-radius: 8px;
		padding: 0.75rem 1rem;
		font-family: ui-monospace, SFMono-Regular, Menlo, monospace;
		font-size: 13px;
		color: #c3c2b7;
		overflow-x: auto;
		white-space: pre;
		margin-bottom: 1.5rem;
	}

	.gb-row {
		display: flex;
		align-items: center;
		gap: 12px;
		margin: 0 0 12px;
	}

	.gb-lbl {
		font-size: 13px;
		color: #c3c2b7;
		min-width: 92px;
	}

	.gb-out {
		font-size: 14px;
		font-weight: 500;
		min-width: 92px;
		text-align: right;
		font-variant-numeric: tabular-nums;
	}

	.gb-card {
		background: #232321;
		border-radius: 8px;
		padding: 1.25rem 1.35rem;
	}

	.gb-final {
		font-size: 52px;
		font-weight: 500;
		font-variant-numeric: tabular-nums;
		line-height: 1;
	}

	.gb-chip {
		font-size: 12px;
		color: #c3c2b7;
		font-variant-numeric: tabular-nums;
	}

	.gb-mult {
		display: inline-block;
		min-width: 46px;
		text-align: right;
		font-variant-numeric: tabular-nums;
		font-weight: 500;
	}

	input[type='range'] {
		-webkit-appearance: none;
		appearance: none;
		height: 4px;
		border-radius: 2px;
		background: #2c2c2a;
		outline: none;
	}

	input[type='range']::-webkit-slider-thumb {
		-webkit-appearance: none;
		appearance: none;
		width: 18px;
		height: 18px;
		border-radius: 50%;
		background: #3987e5;
		cursor: pointer;
		border: none;
	}

	input[type='range']::-moz-range-thumb {
		width: 18px;
		height: 18px;
		border-radius: 50%;
		background: #3987e5;
		cursor: pointer;
		border: none;
	}
</style>
