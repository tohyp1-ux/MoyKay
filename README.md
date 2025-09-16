@@ -1,161 +1,150 @@

<!DOCTYPE html>
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
      background: #f0f4f8;
      color: #333;
      text-align: center;
    }

    /* Hero section */
    .hero {
      position: relative;
      height: 50vh;
      display: flex;
      justify-content: center;
      align-items: center;
      color: white;
      overflow: hidden;
      background: linear-gradient(rgba(0,0,0,0.4), rgba(0,0,0,0.4));
    }

    .hero img {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
      opacity: 0.5; /* semi-transparent */
      z-index: 0;
    }

    .hero h1 {
      position: relative;
      font-size: 3em;
      z-index: 1;
      margin: 0;
      padding: 0 20px;
    }

    .hero p {
      position: relative;
      font-size: 1.5em;
      z-index: 1;
    }

    main {
      max-width: 900px;
      margin: 40px auto;
      padding: 0 20px;
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

    .images {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 20px;
      margin-top: 40px;
    }

    .images img {
      width: 45%;
      max-width: 400px;
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
      margin-top: 50px;
    }
  </style>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>MX-5 Lemon & Juice Progress</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            text-align: center;
            background-color: #f0f4f8;
            color: #333;
        }

        /* Hero section */
        .hero {
            position: relative;
            height: 50vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            background-color: #333;
            color: white;
        }

        .hero img {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            opacity: 0.4; /* semi-transparent */
            z-index: 0;
        }

        .hero h1 {
            position: relative;
            font-size: 2.5em;
            z-index: 1;
            margin: 0;
        }

        .hero p {
            position: relative;
            font-size: 1.2em;
            z-index: 1;
        }

        .progress-container {
            width: 80%;
            background-color: #eee;
            margin: 20px auto;
            border-radius: 20px;
            overflow: hidden;
        }

        .progress-bar {
            height: 30px;
            width: 0%;
            background-color: #4caf50;
            line-height: 30px;
            color: white;
            font-weight: bold;
            transition: width 1s ease;
        }

        .cups-info {
            font-size: 1.1em;
            margin-top: 10px;
            color: #555;
        }

        .images {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 40px 0;
            flex-wrap: wrap;
        }

        .images img {
            width: 45%;
            max-width: 400px;
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
            margin-top: 50px;
        }
    </style>
</head>
<body>
  <!-- Hero section with transparent MX-5 background -->
  <div class="hero">
    <img src="50-50-01-ext.jpg" alt="MX-5 Hero">
    <div>
      <h1>MX-5 Lemon & Juice Progress</h1>
      <p>目标: 购买 MX-5 (150,000 MYR)</p>
    <!-- Hero section with semi-transparent background -->
    <div class="hero">
        <img src="50-50-01-ext.jpg" alt="MX-5 Hero">
        <div>
            <h1>MX-5 Lemon & Juice Progress</h1>
            <p>目标：购买 MX-5（价格 150,000 MYR）</p>
        </div>
    </div>
  </div>

  <main>
    <!-- Progress card -->
    <!-- Progress section -->
    <div class="progress-container">
      <div class="progress-bar" id="progressBar">0%</div>
        <div class="progress-bar" id="progressBar">0%</div>
    </div>
    <div class="cups-info" id="moneyInfo"></div>
    <div class="cups-info" id="cupInfo"></div>

    <!-- Two MX-5 images below -->
    <div class="images">
      <img src="50-50-01-holistic.jpg" alt="MX-5 Holistic View">
      <img src="mx5-manual.png" alt="MX-5 Manual">
        <img src="50-50-01-holistic.jpg" alt="MX-5 Holistic View">
        <img src="mx5-manual.png" alt="MX-5 Manual">
    </div>
  </main>

  <footer>
    &copy; 2025 Lemon & Juice MX-5 Progress
  </footer>

  <script>
    // ====== 销售数据 ======
    const lemonadeSold = 20;
    const juiceSold = 15;
    const priceLemon = 3;
    const priceJuice = 5;
    const priceMX5 = 150000;

    const totalMoney = lemonadeSold * priceLemon + juiceSold * priceJuice;
    const percent = Math.min((totalMoney / priceMX5) * 100, 100);

    const progressBar = document.getElementById('progressBar');
    progressBar.style.width = percent + '%';
    progressBar.textContent = Math.floor(percent) + '%';

    document.getElementById('moneyInfo').textContent = `已赚: ${totalMoney} MYR / ${priceMX5} MYR`;
    document.getElementById('cupInfo').textContent = `已卖出: ${lemonadeSold} 杯柠檬水, ${juiceSold} 杯果蔬汁`;
  </script>

    <footer>
        &copy; 2025 Lemon & Juice MX-5 Progress
    </footer>

    <script>
        // ==== 销售数据 ====
        const lemonadeSold = 20;
        const juiceSold = 15;
        const priceLemon = 3;
        const priceJuice = 5;
        const priceMX5 = 150000;

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
