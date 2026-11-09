<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>東泳記泳裝店 | 知本溫泉票券與泳具專賣</title>
    <style>
        /* 基礎全域設定 */
        :root {
            --primary: #e67e22;
            --secondary: #3498db;
            --bg-color: #f0f2f5;
            --card-bg: #ffffff;
            --text-main: #333333;
            --text-muted: #666666;
        }
        body {
            font-family: 'PingFang TC', 'Microsoft JhengHei', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-main);
            margin: 0;
            padding: 0;
            line-height: 1.6;
        }
        a { text-decoration: none; }
        
        /* 主容器：限制最大寬度，讓電腦版也好看 */
        .container {
            max-width: 600px;
            margin: 0 auto;
            padding: 15px;
            padding-bottom: 80px; /* 留空間給懸浮按鈕 */
        }

        /* 頂部資訊卡片 */
        .header-card {
            background: var(--card-bg);
            border-radius: 12px;
            padding: 20px;
            text-align: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            margin-bottom: 20px;
        }
        .header-card h1 {
            margin: 0 0 10px 0;
            font-size: 24px;
            color: var(--primary);
        }
        .header-card a.info-link {
            display: block;
            color: var(--text-muted);
            margin: 8px 0;
            font-size: 16px;
        }

        /* 簡介文字 */
        .intro-box {
            background: var(--card-bg);
            border-radius: 12px;
            padding: 15px;
            margin-bottom: 20px;
            font-size: 15px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }

        /* 標題共用樣式 */
        .section-title {
            font-size: 18px;
            font-weight: bold;
            margin: 25px 0 15px 0;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        /* 熱賣商品網格 */
        .product-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 10px;
        }
        .product-item {
            background: var(--card-bg);
            border-radius: 12px;
            padding: 15px 5px;
            text-align: center;
            box-shadow: 0 2px 8px rgba(0,0,0,0.03);
        }
        .product-item .icon { font-size: 28px; margin-bottom: 5px; }
        .product-item .name { font-size: 14px; font-weight: bold; }

        /* 溫泉 SPA 卡片 */
        .spa-card {
            background: var(--card-bg);
            border-radius: 12px;
            padding: 15px;
            margin-bottom: 15px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }
        .spa-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 10px;
        }
        .spa-title { font-weight: bold; font-size: 17px; }
        .spa-distance { font-size: 13px; color: var(--text-muted); }
        .nav-btn {
            background: var(--secondary);
            color: white;
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 13px;
        }
        .spa-desc { font-size: 14px; color: var(--text-muted); margin-bottom: 15px; }
        
        /* 橫向滾動照片區 */
        .image-scroller {
            display: flex;
            overflow-x: auto;
            gap: 10px;
            padding-bottom: 5px;
            /* 隱藏滾動條但保持功能 */
            scrollbar-width: none; 
        }
        .image-scroller::-webkit-scrollbar { display: none; }
        .image-scroller img {
            height: 120px;
            width: 160px;
            object-fit: cover;
            border-radius: 8px;
            background-color: #eee; /* 圖片失效時的底色 */
        }

        /* 下拉詳細資訊 */
        details {
            background: #f8f9fa;
            border-radius: 8px;
            padding: 10px;
            margin-top: 10px;
            font-size: 14px;
        }
        summary {
            cursor: pointer;
            font-weight: bold;
            color: var(--primary);
            outline: none;
        }
        details ul {
            padding-left: 20px;
            margin: 10px 0 0 0;
            color: var(--text-muted);
        }
        details li { margin-bottom: 6px; }

        /* 順遊景點 */
        .attraction-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 10px;
        }
        .attraction-item {
            background: var(--card-bg);
            border-radius: 12px;
            padding: 15px;
            text-align: center;
            box-shadow: 0 2px 8px rgba(0,0,0,0.03);
            color: var(--text-main);
            display: block;
        }
        .attraction-item:hover { background: #fdfdfd; transform: translateY(-2px); transition: 0.2s;}
        .attraction-icon { font-size: 24px; margin-bottom: 5px; }
        .attraction-title { font-weight: bold; font-size: 15px; }
        .attraction-sub { font-size: 12px; color: var(--text-muted); }

        /* 底部資訊與評論 */
        .footer-info {
            background: #fff3e0;
            border-radius: 12px;
            padding: 15px;
            margin-top: 30px;
            font-size: 14px;
        }
        .footer-info p { margin: 5px 0; }
        .review-link {
            display: block;
            text-align: center;
            margin-top: 15px;
            font-weight: bold;
            color: #d35400;
        }

        /* 懸浮按鈕 (FAB) */
        .fab-container {
            position: fixed;
            bottom: 20px;
            right: 20px;
            display: flex;
            flex-direction: column;
            gap: 12px;
            z-index: 100;
        }
        .fab {
            width: 48px;
            height: 48px;
            border-radius: 50%;
            background: var(--card-bg);
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 22px;
            color: var(--text-main);
            transition: 0.2s;
        }
        .fab.fab-primary {
            background: var(--primary);
            color: white;
        }
        .fab:hover { transform: scale(1.08); }
    </style>
</head>
<body>

<div class="container">
    <!-- 頂部資訊區 -->
    <div class="header-card">
        <h1>東泳記泳裝店</h1>
        <a href="https://maps.google.com/?q=台東縣卑南鄉溫泉路370號" target="_blank" class="info-link">
            📍 卑南鄉溫泉路370號 🚗
        </a>
        <a href="tel:0910557998" class="info-link">
            📞 0910-557-998
        </a>
    </div>

    <!-- 簡介區 -->
    <div class="intro-box">
        <div style="text-align: center; font-size: 24px; margin-bottom: 10px;">🛟 👙 🥽 🩱</div>
        店內提供精選平價泳裝、優惠溫泉券、泳具週邊與大中小各式泳圈，讓您不傷荷包，就能輕鬆拿捏時尚穿搭。<br>
        <small style="color: var(--text-muted); display: block; margin-top: 10px;">*也歡迎預約男仕理髮服務 ✂️</small>
    </div>

    <!-- 熱賣商品 -->
    <div class="section-title"><span>🛍️</span> 本店熱賣商品</div>
    <div class="product-grid">
        <div class="product-item"><div class="icon">🎟️</div><div class="name">優惠溫泉券</div></div>
        <div class="product-item"><div class="icon">👙</div><div class="name">精選泳裝</div></div>
        <div class="product-item"><div class="icon">🥽</div><div class="name">泳具與配件</div></div>
        <div class="product-item"><div class="icon">🛟</div><div class="name">各式泳圈</div></div>
        <div class="product-item"><div class="icon">👶</div><div class="name">嬰幼兒童</div></div>
        <div class="product-item"><div class="icon">🏖️</div><div class="name">玩水周邊</div></div>
    </div>

    <!-- 知本溫泉精選 -->
    <div class="section-title"><span>♨️</span> 知本在地SPA溫泉精選</div>
    
    <!-- 溫泉卡片 1：東遊季 -->
    <div class="spa-card">
        <div class="spa-header">
            <div>
                <div class="spa-title">東遊季溫泉渡假村</div>
                <div class="spa-distance">距離本店約400公尺</div>
            </div>
            <a href="https://maps.google.com/?q=東遊季溫泉渡假村" target="_blank" class="nav-btn">🚗 導航</a>
        </div>
        <div class="spa-desc">
            由台東縣農會經營，養生溫泉區占地3000坪，規劃有溫泉水療區、露天溫泉區、冷水池、兒童戲水區等，知本最大戶外溫泉SPA。
        </div>
        <div class="image-scroller">
            <img src="Images/tyg-1.jpg" alt="東遊季照片">
            <img src="Images/tyg-2.jpg" alt="東遊季照片">
            <img src="Images/tyg-3.jpg" alt="東遊季照片">
        </div>
        <details>
            <summary>▼ 交通與詳細資訊</summary>
            <ul>
                <li><b>路線指引：</b>度假村坐落於溫泉路指標路段右側。</li>
                <li><b>大眾運輸：</b>搭乘公車［8129］可於「東遊季」站下車。</li>
                <li><b>停車資訊：</b>園區內備有免費露天停車場。</li>
            </ul>
        </details>
    </div>

    <!-- 溫泉卡片 2：知本老爺 -->
    <div class="spa-card">
        <div class="spa-header">
            <div>
                <div class="spa-title">知本老爺酒店</div>
                <div class="spa-distance">距離本店約3.3公里</div>
            </div>
            <a href="https://maps.google.com/?q=知本老爺酒店" target="_blank" class="nav-btn">🚗 導航</a>
        </div>
        <div class="spa-desc">
            五星級天幕風呂緊鄰戶外游泳池畔，豐富泡湯設備；戶外游泳池依季節更替水溫，設施精緻頂級享受。
        </div>
        <div class="image-scroller">
            <img src="Images/royal-1.jpg" alt="老爺照片">
            <img src="Images/royal-2.jpg" alt="老爺照片">
        </div>
        <details>
            <summary>▼ 交通與詳細資訊</summary>
            <ul>
                <li><b>路線指引：</b>沿著溫泉路轉龍泉路循指標即可輕鬆抵達。</li>
                <li><b>停車資訊：</b>館內設有免費停車場。</li>
            </ul>
        </details>
    </div>

    <!-- 附近順遊景點 -->
    <div class="section-title"><span>🌲</span> 附近順遊景點推薦</div>
    <div class="attraction-grid">
        <a href="https://maps.google.com/?q=知本國家森林遊樂區" target="_blank" class="attraction-item">
            <div class="attraction-icon">🌳</div>
            <div class="attraction-title">知本森林遊樂區</div>
            <div class="attraction-sub">漫步林間吸收芬多精</div>
        </a>
        <a href="https://maps.google.com/?q=白玉瀑布" target="_blank" class="attraction-item">
            <div class="attraction-icon">💦</div>
            <div class="attraction-title">白玉瀑布</div>
            <div class="attraction-sub">輕鬆好走的秘境瀑布</div>
        </a>
        <a href="https://maps.google.com/?q=勇男橋" target="_blank" class="attraction-item">
            <div class="attraction-icon">🌉</div>
            <div class="attraction-title">知本勇男橋</div>
            <div class="attraction-sub">壯觀斜張橋打卡地標</div>
        </a>
        <a href="https://maps.google.com/?q=清覺寺" target="_blank" class="attraction-item">
            <div class="attraction-icon">⛩️</div>
            <div class="attraction-title">清覺寺</div>
            <div class="attraction-sub">半山腰上的幽靜聖地</div>
        </a>
    </div>

    <!-- 底部位置資訊 -->
    <div class="footer-info">
        <b>📍 本店位置與交通指引</b>
        <p>本店位於卑南鄉溫泉路370號。<br>自行開車行經溫泉路即可抵達。</p>
        <p>若搭乘大眾交通工具，搭乘公車[8129]至東遊季站下車步行即可抵達；從本店前往東遊季溫泉區約400公尺的距離。</p>
        
        <a href="https://maps.google.com/?q=台東縣卑南鄉溫泉路370號" target="_blank" class="review-link">
            如果您也喜歡這份用心，歡迎給我們留個五星評價⭐⭐⭐⭐⭐
        </a>
    </div>

</div>

<!-- 懸浮操作按鈕 (右下角) -->
<div class="fab-container">
    <a href="https://maps.google.com/?q=台東縣卑南鄉溫泉路370號" class="fab" title="導航到店">🚗</a>
    <a href="tel:0910557998" class="fab fab-primary" title="撥打電話">📞</a>
</div>

</body>
</html>
