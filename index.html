<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>考試時間表</title>
    <style>
        :root {
            --bg-color: #1a1a1a;
            --text-color: #ffffff;
            --accent-color: #4CAF50; /* 考試進行中的顏色 */
            --sidebar-bg: #2d2d2d;
            --sidebar-width: 350px;
        }

        body {
            margin: 0;
            padding: 0;
            background-color: var(--bg-color);
            color: var(--text-color);
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            display: flex;
            height: 100vh;
            overflow: hidden;
        }

        /* 中間：時鐘區域 */
        #main-display {
            flex: 1;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        #clock-time {
            font-size: 12rem; /* 超大時間字體 */
            font-weight: bold;
            font-variant-numeric: tabular-nums; /* 防止數字跳動 */
            line-height: 1;
        }

        #clock-date {
            font-size: 3rem;
            color: #aaaaaa;
            margin-top: 1rem;
        }

        /* 右邊：考試列表 */
        #schedule-sidebar {
            width: var(--sidebar-width);
            background-color: var(--sidebar-bg);
            padding: 2rem;
            box-shadow: -5px 0 15px rgba(0,0,0,0.3);
            display: flex;
            flex-direction: column;
            overflow-y: auto;
        }

        h2 {
            margin-top: 0;
            border-bottom: 2px solid #555;
            padding-bottom: 10px;
        }

        .exam-item {
            background: #3d3d3d;
            margin-bottom: 1rem;
            padding: 1.5rem;
            border-radius: 8px;
            border-left: 5px solid transparent;
            transition: transform 0.2s;
        }

        .exam-item.active {
            border-left: 5px solid var(--accent-color);
            background: #2e3b2f;
            transform: scale(1.02);
        }

        .exam-item.past {
            opacity: 0.5;
        }

        .exam-time {
            font-size: 1.2rem;
            color: #ddd;
            margin-bottom: 0.5rem;
            font-weight: bold;
        }

        .exam-subject {
            font-size: 1.5rem;
            font-weight: bold;
        }

        /* 響應式：手機版改為上下排列 */
        @media (max-width: 768px) {
            body {
                flex-direction: column;
            }
            #schedule-sidebar {
                width: 100%;
                height: 40%;
            }
            #clock-time {
                font-size: 5rem;
            }
        }
    </style>
</head>
<body>

    <main id="main-display">
        <div id="clock-time">00:00:00</div>
        <div id="clock-date">YYYY/MM/DD</div>
    </main>

    <aside id="schedule-sidebar">
        <h2>今日考試流程</h2>
        <div id="schedule-list">
            </div>
    </aside>

    <script>
        // ==========================================
        // CONFIG: 請在這裡編輯您的考試科目與時間
        // 格式: { time: "HH:MM - HH:MM", subject: "科目名稱" }
        // ==========================================
        const examSchedule = [
            { time: "08:10 - 09:00", subject: "早自習 / 準備" },
            { time: "09:00 - 10:30", subject: "國語文" },
            { time: "11:00 - 12:10", subject: "英語文" },
            { time: "13:30 - 14:50", subject: "數學" },
            { time: "15:20 - 16:20", subject: "自然科學" }
        ];
        // ==========================================

        function updateClock() {
            const now = new Date();
            
            // 更新時間 HH:MM:SS
            const timeString = now.toLocaleTimeString('en-GB', { 
                hour12: false, 
                hour: '2-digit', 
                minute: '2-digit', 
                second: '2-digit' 
            });
            document.getElementById('clock-time').textContent = timeString;

            // 更新日期 YYYY/MM/DD
            const year = now.getFullYear();
            const month = String(now.getMonth() + 1).padStart(2, '0');
            const day = String(now.getDate()).padStart(2, '0');
            document.getElementById('clock-date').textContent = `${year}/${month}/${day}`;

            checkScheduleStatus(now);
        }

        function renderSchedule() {
            const listContainer = document.getElementById('schedule-list');
            listContainer.innerHTML = '';

            examSchedule.forEach((exam, index) => {
                const div = document.createElement('div');
                div.className = 'exam-item';
                div.id = `exam-${index}`;
                div.innerHTML = `
                    <div class="exam-time">${exam.time}</div>
                    <div class="exam-subject">${exam.subject}</div>
                `;
                listContainer.appendChild(div);
            });
        }

        function checkScheduleStatus(now) {
            const currentHm = now.getHours() * 60 + now.getMinutes();

            examSchedule.forEach((exam, index) => {
                const el = document.getElementById(`exam-${index}`);
                
                // 解析時間字串 "09:00 - 10:30"
                const [startStr, endStr] = exam.time.split('-').map(s => s.trim());
                
                const startHm = parseTime(startStr);
                const endHm = parseTime(endStr);

                // 移除舊狀態
                el.classList.remove('active', 'past');

                if (currentHm >= endHm) {
                    el.classList.add('past'); // 考試已結束
                } else if (currentHm >= startHm && currentHm < endHm) {
                    el.classList.add('active'); // 考試進行中
                }
            });
        }

        function parseTime(timeStr) {
            const [h, m] = timeStr.split(':').map(Number);
            return h * 60 + m;
        }

        // 初始化
        renderSchedule();
        setInterval(updateClock, 1000); // 每秒更新
        updateClock(); // 立即執行一次
    </script>
</body>
</html>
