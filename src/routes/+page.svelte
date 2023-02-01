<script>
	import Footer from "./Components/Footer.svelte";
	import Header from "./Components/Header.svelte";
	import Tabs from "./Components/Tabs.svelte";
	import Home from "./Components/Home.svelte"
	import Form from "./Components/Form.svelte";

	let items = ["Home", "Enroll Online Now"]
	let activeItem = "Home"
	const tabChanger = (e) => {
		activeItem = e.detail;

	}


</script>
<div class="main">
	<Header/>
	<main>
		<Tabs {items} {activeItem} on:tabChanger={tabChanger}/>
		{#if activeItem === "Home"}
		<Home/>
		{:else if activeItem === "Enroll Online Now"}
		<Form/>
		{/if}


	</main>
	<Footer/>
</div>

<style>
	main {
		height: 70vh;
		background-image: url("./Components/Images/galaxy_art3.png");
	}
	
	
</style>

