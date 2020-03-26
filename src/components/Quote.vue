<template>
	<div class="row">
		<slot name="text"></slot>
	</div>
</template>

<script>
</script>

<style>
	.text-center {
		text-align: center;
	}
	.quoteCard {
		border: 1px solid black;
		padding: 0 5px;
	}
	.quoteCard:hover {
		background-color: lightblue;
		cursor: pointer;
	}
	.marginBottom {
		margin-bottom: 10px;
	}
</style>