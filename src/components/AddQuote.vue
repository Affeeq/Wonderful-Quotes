<template>
	<div class="row">
		<div class="col-xs-12 text-center">
			<h5>Quote</h5>
			<div>
				<textarea rows="5" cols="100" v-model="newQuote"></textarea>
			</div>
			<button class="btn btn-primary" @click="addQuote">Add Quote</button>
		</div>
	</div>
</template>

<script>

    export default {
    	data: function() {
    		return {
                localQuotes: this.quotes,
    			newQuote: ''
    		}
    	},
    	props: ['quotes'],
    	methods: {
    		addQuote() {
                if(this.localQuotes.length == 10) {
                    alert('You have reached the maxiumum number of quotes. Delete and try again.');
                } else {
                    this.localQuotes.push(this.newQuote);
                    this.$emit('quoteWasAdded', this.localQuotes);
                    this.newQuote = '';
                }
    		}
    	}
    }
</script>

<style>
	.text-center {
		text-align: center;
	}
</style>