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

	randomize();
</script>

<section>
	<h1>Slumpord till skrivövningar</h1>
	<p>{nouns[nounsPos]}</p>

	<p>{adjectives[adjectivesPos]}</p>

	<p>{verbs[verbsPos]}</p>

	<p>{whenOrWhere[whenOrWherePos]}</p>

	<p>
		<button on:click={randomize}>Nya ord, tack!</button>
	</p>
</section>
