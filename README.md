
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MX-5 Lemon & Juice Sale</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 20px;
        }
        img {
            max-width: 80%;
            height: auto;
            margin: 20px 0;
            border: 2px solid #ccc;
            border-radius: 10px;
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
        }
        p {
            font-size: 18px;
        }
    </style>
</head>
<body>
    <h1>MX-5 Lemon & Juice Sale Progress</h1>
    <p>目标：购买 MX-5（价格 150,000 MYR）</p>

    <div class="progress-container">
        <div class="progress-bar" id="progressBar">0%</div>
    </div>

    <p id="moneyInfo"></p>
    <p id="cupInfo"></p>

    <h2>看看我们的 MX-5</h2>
    <img src="50-50-01-ext.jpg" alt="MX-5 Exterior">
    <img src="50-50-01-holistic.jpg" alt="MX-5 Holistic View">
    <img src="mx5-manual.png" alt="MX-5 Manual">

    <script>
        // ====== 这里设置你卖出的数量 ======
        const lemonadeSold = 20;  // 卖出的柠檬水杯数
        const juiceSold = 15;     // 卖出的果蔬汁杯数
        const priceLemon = 3;     // 每杯柠檬水价格
        const priceJuice = 5;     // 每杯果蔬汁价格
        const priceMX5 = 150000;  // MX-5 价格（MYR）

        // 计算总收入
        const totalMoney = lemonadeSold * priceLemon + juiceSold * priceJuice;
        const percent = Math.min((totalMoney / priceMX5) * 100, 100);

        // 更新进度条
        const progressBar = document.getElementById('progressBar');
        progressBar.style.width = percent + '%';
        progressBar.textContent = Math.floor(percent) + '%';

        // 显示金额和卖出杯数
        document.getElementById('moneyInfo').textContent = `已赚: ${totalMoney} MYR / ${priceMX5} MYR`;
        document.getElementById('cupInfo').textContent = `已卖出: ${lemonadeSold} 杯柠檬水, ${juiceSold} 杯果蔬汁`;
    </script>
</body>
</html>
