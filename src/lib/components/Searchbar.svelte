<script lang="js">
	import Button from '$lib/components/Button.svelte';
	export let text= any;
</script>

<div class="searchBar">
	<input id="searchQueryInput" type="text" name="searchQueryInput" placeholder={text} value="" />
	<Button variant="search"><span class="material-symbols-outlined"> search </span>Search</Button>
</div>

<style>
	.searchBar {
		width: 25%;
		display: flex;
		align-items: center;
		margin-right: 20px;
	}

	#searchQueryInput {
		width: 100%;
		height: 2.8rem;
		background: #f5f5f5;
		outline: none;
		border: none;
		border-radius: 20px; 	/* border radius thora increse++ */
		padding: 0 3.5rem 0 1.5rem;
		font-size: 1rem;
	}
	.searchBar span {
		font-size: 1.5rem;
		margin-right: 0.5rem;
	}
	
	/* change search querry place holder and add some focus */
	#searchQueryInput::placeholder {
		color: #999; 
	}

	#searchQueryInput:focus {
		box-shadow: 0 0 0 2px rgba(0, 0, 0, 0.1); 
	}
</style>
