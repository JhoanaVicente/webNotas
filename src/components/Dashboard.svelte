<script>
    export let notes;
    import Notes from "./Notes.svelte";
</script>

<div class="Dashboard">
    <div class="notes-container">
        {#each notes as {title, color, text} }
            <Notes {title} {color} {text} />
        {/each}

    </div>
</div>

<style>
    .Dashboard{
        width: 100px;
        padding: 20px;
        box-sizing: border-box;
    }

    .notes-container{
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        width: 100%;
        gap: 10px;
    }

</style>