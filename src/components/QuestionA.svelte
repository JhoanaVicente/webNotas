<!-- Question.svelte -->
<script>
    export let questions;
    export let options;
    export let currentIndex;
    export let totalQuestions;
    export let onNext;

    function handleNext() {
        onNext();
    }
</script>

<div class="question">
    <h2>TEST {currentIndex + 1} of {totalQuestions}</h2>
    <p>{questions}</p>
    {#each options as option}
        <label><input type="radio" name="q{currentIndex + 1}" value="{option}"> {option}</label>
    {/each}
    {#if currentIndex !== totalQuestions - 1}
        <button type="button" on:click={handleNext}>Next</button>
    {/if}
</div>
