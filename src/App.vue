<template>
	<div class="container">
		<app-header :quotes="quotes"></app-header>
		<app-add-quote :quotes="quotes" @quoteWasAdded="quotes = $event"></app-add-quote>
		<app-quote>
			<div class="col-xs-3 marginBottom" v-for="(quote, index) in quotes" slot="text">
				<p class="quoteCard" @click="deleteQuote(index)">{{ quote }}</p>
			</div>
		</app-quote>
		<app-footer></app-footer>
	</div>
</div>
</template>

<script>
	import Header from './components/Header.vue';
	import AddQuote from './components/AddQuote.vue';
	import Quote from './components/Quote.vue';
	import Footer from './components/Footer.vue';

    export default {
    	data: function() {
    		return {
    			quotes: []
    		};
    	},
    	methods: {
    		deleteQuote(index) {
    			this.quotes.splice(index, 1);
    		}
    	},
        components: {
        	appHeader: Header,
        	appAddQuote: AddQuote,
        	appQuote: Quote,
        	appFooter: Footer
        }
    }
</script>

<style>
	
</style>
