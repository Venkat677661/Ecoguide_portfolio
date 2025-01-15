# Ecoguide_portfolio
A sustainable living tips app with quizzes
here's the code for ecoguide's tips page: 
```
<!-- tips.html -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ecoguide Tips</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1>Personalized Eco-Tips for You!</h1>
  </header>
  <main>
    <div class="filters">
      <button class="active" onclick="filterTips('all')">All</button>
      <button onclick="filterTips('food')">Food</button>
      <button onclick="filterTips('fashion')">Fashion</button>
      <button onclick="filterTips('beauty')">Beauty</button>
    </div>
    <div id="tips-container">
      <!-- tips will be displayed here -->
    </div>
  </main>
  <script src="script.js"></script>
  <script>
    // sample tips data, replace with actual data or api call
    let tipsData = [
      { category: 'food', tip: 'use reusable bags for grocery shopping' },
      { category: 'fashion', tip: 'choose sustainable clothing brands' },
      { category: 'beauty', tip: 'opt for refillable beauty products' },
      { category: 'food', tip: 'plan meals to reduce food waste' },
      // add more tips here...
    ];
    displayTips(tipsData);
    function filterTips(category) {
      let filteredTips = tipsData.filter(tip => tip.category === category || category === 'all');
      displayTips(filteredTips);
    }
    function displayTips(tips) {
      let tipsHtml = '';
      tips.forEach(tip => {
        tipsHtml += `<div class="tip">${tip.tip}</div>`;
      });
      document.getElementById('tips-container').innerHTML = tipsHtml;
    }
  </script>
</body>
</html>
```
this code displays personalized eco-tips filtered by category,
