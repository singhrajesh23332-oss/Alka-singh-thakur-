# Alka-singh-thakur-
Alka singh thakur site welcome to all <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NDA Quiz</title>
    <style>
        body { font-family: Arial, sans-serif; }
        .question { margin: 20px 0; }
    </style>
</head>
<body>
    <h1>NDA Quiz</h1>
    <div id="quiz-container"></div>
    <button id="next-btn">Next</button>
    <button id="toggle-lang-btn">Toggle Language</button>
    <script>
        const questions = [
            { en: "What is the capital of India?", hi: "भारत की राजधानी क्या है?", answer: "New Delhi" },
            { en: "Who wrote the national anthem of India?", hi: "भारत के राष्ट्रगान के लेखक कौन हैं?", answer: "Rabindranath Tagore" },
            // ... add all 10 questions here ...
        ];
        
        let currentQuestionIndex = 0;
        let score = 0;
        let isEnglish = true;

        function loadQuestion() {
            const question = questions[currentQuestionIndex];
            const questionText = isEnglish ? question.en : question.hi;
            document.getElementById('quiz-container').innerHTML = `<div class=\"question\">${questionText}</div>`;
        }

        document.getElementById('next-btn').addEventListener('click', () => {
            currentQuestionIndex++;
            if (currentQuestionIndex < questions.length) {
                loadQuestion();
            } else {
                alert(`Quiz finished! Your score: ${score}`);
            }
        });

        document.getElementById('toggle-lang-btn').addEventListener('click', () => {
            isEnglish = !isEnglish;
            loadQuestion();
        });

        loadQuestion();
    </script>
</body>
</html>
Alka singh thakur site welcome to all 
