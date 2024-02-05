<script>
	let nombre= 'Jhoana';

	import Boton from "./components/Boton.svelte";
</script>

<main>
	<h2>Escribe tu nombre</h2>
	<input type="text" name="" id="" bind:value={nombre}>

	<p>Hola, {nombre}!</p>
	<Boton />
</main>

<style>
	h2 {
		color: green;
	}

</style>