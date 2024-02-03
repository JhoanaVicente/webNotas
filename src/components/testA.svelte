<script>
    document.getElementById('test-form').addEventListener('submit', function (event) {
    event.preventDefault();

    const form = event.target;
    const inputs = form.getElementsByTagName('input');
    let total = 0;

    for (let i = 0; i < inputs.length; i++) {
        if (inputs[i].checked) {
            total += parseInt(inputs[i].value);
        }
    }

    const resultText = `Your score is ${total}.`;
    document.getElementById('result-text').innerText = resultText;

    form.classList.add('hidden');
    document.getElementById('results').classList.remove('hidden');
});

</script>


<main>
    <h1>Personality Test</h1>
    <form id="test-form">
        <h2>TEST A</h2>
        <!-- Add your questions and answer options here -->
        <!-- Example: -->
        <div class="question">
            <p>Prefiero estar rodeado de varias personas, me gusta la interrelación dentro de los grupos.</p>
            <label><input type="radio" name="q1" value="-5"> Strongly disagree</label>
            <label><input type="radio" name="q1" value="-4"> Disagree</label>
            <label><input type="radio" name="q1" value="-3"> Somewhat disagree</label>
            <label><input type="radio" name="q1" value="0"> Neutral</label>
            <label><input type="radio" name="q1" value="3"> Somewhat agree</label>
            <label><input type="radio" name="q1" value="4"> Agree</label>
            <label><input type="radio" name="q1" value="5"> Strongly agree</label>
        </div>
        <!-- Add more questions as needed -->
        <button type="submit">Submit</button>
    </form>
    <div id="results" class="hidden">
        <h2>Your Results</h2>
        <p id="result-text"></p>
    </div>
</main>


<style>

</style>