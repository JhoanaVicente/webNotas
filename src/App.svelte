<script>
	import Header from "./components/Header.svelte";
	import Dashboard from "./components/Dashboard.svelte";


	let notes = [
		{
			id: 0,
			title: 'Vacaciones', 
			color: 'yellow',
			text: 'Hola!',
		},
		{
			id: 1,
			title: 'Vacaciones', 
			color: 'red',
			text: 'Hola!',
		}
	]; 
	let copyNotes = [...notes];

	let count = notes.length;

</script>

<main>
	<Header />
	<div>{count} notes</div>
	<Dashboard notes={notes} />
	
</main>

<style>
	
</style>