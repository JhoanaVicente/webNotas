<script>
	let nombre= 'Jhoana';

	import Boton from "./components/Boton.svelte";
  import QuestionsA from "./components/QuestionsA.svelte";
	import TestA from "./components/TestA.svelte";

</script>

<main>
	<h2>Escribe tu nombre</h2>
	<input type="text" name="" id="" bind:value={nombre}>

	<p>Hola, {nombre}!</p>
	<Boton />
	<TestA />
	<QuestionsA />
</main>

<style>
	/*h1 {
		color: green;
	}*/

</style>