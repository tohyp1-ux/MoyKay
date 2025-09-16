
<html lang="zh">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>MX-5 Lemon & Juice Progress</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Roboto', sans-serif;
      margin: 0;
      background: linear-gradient(135deg, #f0f4f8, #d9e2ec);
      color: #333;
      text-align: center;
    }

    header {
      background-color: #ff6f61;
      color: white;
      padding: 40px 20px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }

    header h1 {
      margin: 0;
      font-size: 2.5em;
    }

    main {
      max-width: 900px;
      margin: 40px auto;
      padding: 0 20px;
    }

    .card {
      background: white;
      border-radius: 15px;
      padding: 30px;
      margin-bottom: 40px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.1);
      transition: transform 0.3s;
    }

    .card:hover {
      transform: translateY(-5px);
    }

    .progress-container {
      width: 100%;
      background: #eee;
      border-radius: 20px;
      overflow: hidden;
      margin: 20px 0;
    }

    .progress-bar {
      height: 35px;
      width: 0%;
      background: linear-gradient(90deg, #ff6f61, #ffb88c);
      color: white;
      font-weight: bold;
      line-height: 35px;
      font-size: 1.2em;
      transition: width 1s ease;
    }

    .cups-info {
      font-size: 1.1em;
      margin-top: 10px;
      color: #555;
    }

    .images img {
      width: 80%;
      max-width: 500px;
      margin: 20px 0;
      border-radius: 15px;
      border: 2px solid #ddd;
      box-shadow: 0 8px 15px rgba(0,0,0,0.1);
      transition: transform 0.3s;
    }

    .images img:hover {
      transform: scale(1.05);
    }

    footer {
      padding: 20px;
      color: #777;
    }
  </style>
</head>
<body>
  <header>
    <h1>MX-5 Lemon & Juice Progress</h1>
    <p>目标: 购买 MX-5 (150,000 MYR)</p>
  </header>

  <main>
    <div class="card">
      <h2>销售进度</h2>
      <div class="progress-container">
        <div class="progress-bar" id="progressBar">0%</div>
      </div>
      <div class="cups-info" id="moneyInfo"></div>
      <div class="cups-info" id="cupInfo"></div>
    </div>

    <h2>看看我们的 MX-5</h2>
    <img src="50-50-01-ext.jpg" alt="MX-5 Exterior" />
    <img src="50-50-01-holistic.jpg" alt="MX-5 Holistic View" />
    <img src="mx5-manual.png" alt="MX-5 Manual" />
  </main>

  <footer>
    &copy; 2025 Lemon & Juice MX-5 Progress
  </footer>

  <script>
    // ====== 这里设置你的销售数据 ======
    const lemonadeSold = 20;  // 卖出的柠檬水杯数
    const juiceSold = 0;     // 卖出的果蔬汁杯数
    const priceLemon = 3;     // 每杯柠檬水价格
    const priceJuice = 5;     // 每杯果蔬汁价格
    const priceMX5 = 150000;  // MX-5 价格（MYR）

    const totalMoney = lemonadeSold * priceLemon + juiceSold * priceJuice;
    const percent = Math.min((totalMoney / priceMX5) * 100, 100);

    const progressBar = document.getElementById('progressBar');
    progressBar.style.width = percent + '%';
    progressBar.textContent = Math.floor(percent) + '%';

    document.getElementById('moneyInfo').textContent = `已赚: ${totalMoney} MYR / ${priceMX5} MYR`;
    document.getElementById('cupInfo').textContent = `已卖出: ${lemonadeSold} 杯柠檬水, ${juiceSold} 杯果蔬汁`;
  </script>
</body>
</html>
