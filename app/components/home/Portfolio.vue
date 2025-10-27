<template>
	<section class="home-portfolio">
		<div class="layout-block">
			<hgroup>
				<h2>Portfolio</h2>
				<p>
					Partnering with visionary founders building the next generation of
					Web3 infrastructure and applications.
				</p>
			</hgroup>
			<div class="home-portfolio__cards">
				<ui-card
					v-for="card in PLACEHOLDER_CARDS"
					:key="card.id"
					:block="card"
				/>
			</div>
		</div>
	</section>
</template>

<script setup lang="ts">
const PLACEHOLDER_CARDS = [
	{
		id: 'Aethir',
		logo: '/images/aethir.png',
		description: 'Powerful GPU solutions on demand',
	},
	{
		id: 'Grass',
		logo: '/images/grass.png',
		description: 'Get rewards on your unused internet',
	},
	{
		id: 'Octra',
		logo: '/images/octra.png',
		description: 'Universal FHE protocol enabling the future',
	},
	{
		id: 'Antimetal',
		logo: '/images/antimetal.png',
		description: 'Savings, visibility and infrastructure guardrails',
	},
	{
		id: 'Fraction AI',
		logo: '/images/fraction-ai.png',
		description: 'Powerful GPU solutions on demand',
	},
];
</script>

<style lang="scss" scoped>
.home-portfolio {
	padding: var(--spacer-64) 0;

	.layout-block {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	hgroup {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		gap: var(--spacer-16);

		h2 {
			@include h2;
		}

		p {
			text-align: center;
			text-wrap: balance;
			max-width: 620px;
		}
	}

	&__cards {
		position: relative;
		width: 100%;
		margin-top: var(--spacer-64);
		display: grid;
		gap: var(--spacer-8);
		grid-template-columns: 1fr;

		@media screen and (min-width: 800px) {
			grid-template-columns: repeat(2, 1fr);
		}

		@media screen and (min-width: 1024px) {
			grid-template-columns: repeat(3, 1fr);
		}

		@media screen and (min-width: 1280px) {
			grid-template-columns: repeat(4, 1fr);
		}

		> * {
			flex: 1;
		}
	}
}
</style>
