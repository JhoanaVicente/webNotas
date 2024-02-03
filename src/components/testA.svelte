<!-- TestA.svelte -->
<script>
    import Question from './Question.svelte';

    let questions = [
        {
            question1: "Prefiero estar conmigo mismo o tener relaciones persona-persona.",
            question2: "Prefiero estar rodeado de varias personas, me gusta la interrelación dentro de los grupos.",
            options: [-5, -4, -3, -2, -1, 0, 1, 2, 3, 4, 5]
        },
        // Agrega más preguntas aquí
        {
            question1: "Prefiero la profundidad de las experiencias a su variedad.",
            question2: "Prefiero la variedad de experiencias a la profundidad de cada una.",
            options: [-5, -4, -3, -2, -1, 0, 1, 2, 3, 4, 5]
        },

    ];

    let currentIndex = 0;

    function handleNext() {
        currentIndex += 1;
    }
</script>

<main>
    <h1>Personality Test</h1>
    <Question
        {question1=questions[currentIndex].question}
        {question2=questions[currentIndex].question}
        {options=questions[currentIndex].options}
        {currentIndex=currentIndex}
        {totalQuestions=questions.length}
        {onNext=handleNext}
    />
</main>
