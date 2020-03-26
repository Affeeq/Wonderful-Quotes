<template>
	<div class="row">
		<div class="col-xs-12">
			<h3>Quotes Added</h3>
			<div class="bar">
				<div class="bar text-center" style="background-color: #2e6da4; margin: 0; color: white" :style="{width: (localQuotes.length*10) + '%'}">
					<p>{{ localQuotes.length }}/10</p>
				</div>
			</div>
		</div>
	</div>
</template>

<script>

    export default {
    	data: function() {
    		return {
    			localQuotes: this.quotes
    		}
    	},
    	props: ['quotes']
    }
</script>

<style>
	.row {
		margin-bottom: 20px;
	}
	.bar {
		width: 100%;
		height: 40px;
		background-color: #eee;
		margin: auto;
		transition: width 500ms;
		border-radius: 5px;
	}

	.text-center {
		text-align: center;
	}

	p {
		line-height: 40px;
		margin: 0;
		font-size: 20px;
	}
</style>