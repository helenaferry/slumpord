<script>
	// @ts-nocheck

	import { nouns } from '../nouns';
	import { adjectives } from '../adjectives';
	import { verbs } from './../verbs';
	import { whenOrWhere } from './../whenOrWhere';

	let nounsPos;
	let adjectivesPos;
	let verbsPos;
	let whenOrWherePos;

	function getRandomInt(max) {
		return Math.floor(Math.random() * max);
	}

	function randomize() {
		nounsPos = getRandomInt(nouns.length - 1);
		adjectivesPos = getRandomInt(adjectives.length - 1);
		verbsPos = getRandomInt(verbs.length - 1);
		whenOrWherePos = getRandomInt(whenOrWhere.length - 1);
	}

	console.log('nouns', nouns.length);
	console.log('adjectives', adjectives.length);
	console.log('verbs', verbs.length);
	console.log('whenOrWhere', whenOrWhere.length);

	randomize();
</script>

<section>
	<div>
		<h1>Slumpord till skrivövningar</h1>
		<p>{nouns[nounsPos]}</p>

		<p>{adjectives[adjectivesPos]}</p>

		<p>{verbs[verbsPos]}</p>

		<p>{whenOrWhere[whenOrWherePos]}</p>

		<p>
			<button on:click={randomize}>Nya ord, tack!</button>
		</p>
	</div>
	<footer>
		Slumpordsapp för skrivövningar av <a href="https://helenas.dagar.se">Helena Ferry</a>.
	</footer>
</section>
