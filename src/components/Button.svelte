<script>
    let counter = 0;
    $: total = counter //Esta $ anotacion ayuda a svelte a actualizarse el valor de una variable por si tiene otro valor

    function handleClick(){
        counter++;
    }

</script>

<div class="Button">
    <button on:click={handleClick}>Click me</button>
    <div>Has dado {total} clicks</div>
</div>