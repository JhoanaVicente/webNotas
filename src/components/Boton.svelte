<script>
    let contador = 0;

    $: total = contador; //con este $ el valor tambien es reactivo 
    
    function handleClick(){
        contador++;
    }

</script>

<div class="Boton">
    <button on:click={handleClick}>Click me</button>
    <div>Has dado {total} clicks</div>

</div>

<style>

</style>