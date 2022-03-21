<template>
	<div class="results">Reaction time - <span id="score">{{score}}</span> ms</div>
	<p class="rank">{{ rank }}</p>
</template>

<script>
export default {
	props: ['score'],
	data() {
		return {
			rank: null
		};
	},
	mounted() {
		if(this.score < 250){
			this.rank = 'Ninja Fingers';
		} else if (this.score < 400) {
			this.rank = 'Rapid reflexes';
		}
		else{
			this.rank = 'Snale pace...';
		}
	},
}
</script>

<style>
	.results {
		padding: 10px;
		color: #000;
		padding: 10px 0;
		margin: 10px auto;
	}
	#score {
		color: #0faf87;
		font-weight: bold;
	}
	.rank{
		font-size: 1.4em;
		color: #0faf87;
		font-weight: bold;
	}
</style>
