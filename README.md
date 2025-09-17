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
      background: #000; /* fallback */
    }

    /* Hero 背景图片 + 半透明蒙版 */
    .hero::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: url('50-50-01-ext.jpg') center/cover no-repeat;
      opacity: 0.5;
      z-index: 0;
    }

    .hero-content {
      position: relative;
      z-index: 1;
      text-align: center;
    }

    .hero h1 {
      font-size: 3em;
      margin: 0;
      padding: 0 20px;
    }

    .hero p {
      font-size: 1.5em;
      margin-top: 10px;
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

    /* 助力按钮 */
    .support-container {
      margin-top: 30px;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 10px;
    }

    .support-container img {
      width: 50px;
      cursor: pointer;
      transition: transform 0.2s;
    }

    .support-container img:hover {
      transform: scale(1.2);
    }

    .support-count {
      font-size: 1.3em;
      font-weight: bold;
      color: #ff5722;
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
    <div class="hero-content">
      <h1>MX-5 Lemon & Juice Progress</h1>
      <p>目标: 购买 MX-5 (150,000 MYR)</p>
    </div>
  </div>

  <main>
    <!-- Progress bar -->
    <div class="progress-container">
      <div class="progress-bar" id="progressBar">0%</div>
    </div>
    <div class="cups-info" id="moneyInfo"></div>
    <div class="cups-info" id="cupInfo"></div>
    <div class="cups-info" id="dateInfo"></div>

    <!-- 助力按钮 -->
    <div class="support-container">
      <img src="flame-icon.webp" alt="Support Icon" id="supportBtn">
      <div class="support-count" id="supportCount">0</div>
    </div>

    <!-- 两张 MX-5 图片 -->
    <div class="images">
      <img src="Arrogant-Rich-Man.3.meme.webp" alt="Meme Image">
      <img src="2089hz-300x290.jpg" alt="2089hz Image">
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

    document.getElementById('moneyInfo').textContent =
      `已赚: ${totalMoney} MYR / ${priceMX5} MYR`;

    document.getElementById('cupInfo').textContent =
      `已卖出: ${lemonadeSold} 杯柠檬水 + ${juiceSold} 杯果汁`;

    // ====== 日期显示 ======
    const today = new Date();
    const dateString = today.getDate() + "/" + (today.getMonth() + 1) + "/" + today.getFullYear();
    document.getElementById('dateInfo').textContent = `今天是 ${dateString}`;

    // ====== 助力按钮点击计数 ======
    let supportCount = 0;
    const supportBtn = document.getElementById('supportBtn');
    const supportCountEl = document.getElementById('supportCount');

    supportBtn.addEventListener('click', () => {
      supportCount++;
      supportCountEl.textContent = supportCount;
    });
  </script>
</body>
</html>
