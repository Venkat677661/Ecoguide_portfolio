# Ecoguide_portfolio
A sustainable living tips app with quizzes
here's the code for ecoguide's quiz page:

  here's the code for ecoguide's result page: 
```
<!-- results.html -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ecoguide Results</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1>Your Eco-Score Results!</h1>
  </header>
  <main>
    <div id="results-container">
      <h2>Your score is: <span id="score"></span>/10</h2>
      <p id="message"></p>
      <button onclick="location.href='tips.html'">Get Personalized Tips!</button>
    </div>
  </main>
  <script src="script.js"></script>
  <script>
    let score = localStorage.getItem('score');
    document.getElementById('score').innerText = score;
    if (score <= 3) {
      document.getElementById('message').innerText = 'keep working on sustainability!';
    } else if (score <= 6) {
      document.getElementById('message').innerText = 'good start, keep going!';
    } else {
      document.getElementById('message').innerText = 'eco-rockstar!';
    }
  </script>
</body>
</html>
```
this code displays user's eco-score and message based on score range,
