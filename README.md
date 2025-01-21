<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ちょうしぜんけんきゅうぶ</title>
    <style>
        body {
            background-color: #000;
            color: #fff;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        header {
            text-align: center;
            padding: 20px;
            background: linear-gradient(90deg, #ff044, #000);
        }
        header h1 {
            font-size: 3rem;
            text-shadow: 0 0 10px #ff0000;
        }
        .members, .archives, .message-board {
            margin: 20px;
            padding: 20px;
            border: 1px solid #444;
            border-radius: 10px;
            background-color: #111;
        }
        .members h2, .archives h2, .message-board h2 {
            font-size: 2rem;
            text-shadow: 0 0 5px #fff;
        }
        .member-group {
            margin-bottom: 20px;
        }
        .member-group h3 {
            color: #ff4444;
        }
        .member {
            margin: 5px 0;
            padding: 5px;
            border-bottom: 1px dashed #444;
        }
        .member span {
            font-size: 1.2rem;
            color: #ff0000;
        }
        .archives .event {
            margin: 10px 0;
            padding: 10px;
            border: 1px solid #222;
            border-radius: 5px;
            background-color: #222;
        }
        .archives .event span {
            display: inline-block;
            margin-left: 5px;
            font-size: 1rem;
            color: #ff6666;
        }
        .message-board form {
            margin-bottom: 20px;
        }
        .message-board form input, .message-board form textarea {
            width: calc(100% - 20px);
            margin-bottom: 10px;
            padding: 10px;
            border: 1px solid #333;
            border-radius: 5px;
            background-color: #222;
            color: #fff;
        }
        .message-board .message {
            margin-bottom: 10px;
            padding: 10px;
            border: 1px solid #333;
            border-radius: 5px;
            background-color: #222;
        }
        footer {
            text-align: center;
            padding: 10px;
            background-color: #111;
            font-size: 1rem;
        }
        footer a {
            color: #ff4444;
            text-decoration: none;
        }
    </style>
</head>
<body>
    <header>
        <h1>ちょうしぜんけんきゅうぶ</h1>
    </header>
    <div class="members">
        <h2>メンバー一覧</h2>
        <div class="member-group">
            <h3>三年生組</h3>
            <div class="member">久世 怜 <span>部長</span></div>
            <div class="member">本間 榊</div>
            <div class="member">箱崎 終</div>
            <div class="member">三生 此</div>
            <div class="member">今清水 朔</div>
        </div>
        <div class="member-group">
            <h3>二年生組</h3>
            <div class="member">浅倉 亜紀🍥</div>
            <div class="member">黒見 代</div>
            <div class="member">今清水 榎</div>
            <div class="member">笹留 幽</div>
            <div class="member">笹留 言</div>
        </div>
    </div>
    <div class="archives">
        <h2>怪异事件记录簿</h2>
        <div class="event">事件一：不存在的同学 <span>💀 已探索</span></div>
        <div class="event">事件二：学校楼顶的...? <span>👾 未探索</span></div>
    </div>
    <div class="message-board">
        <h2>留言板</h2>
        <form id="messageForm">
            <input type="text" id="username" placeholder="名字（可匿名）" required>
            <textarea id="messageContent" placeholder="留言内容" rows="4" required></textarea>
            <button type="submit">提交</button>
        </form>
        <div id="messages">
            <!-- Messages will appear here -->
        </div>
    </div>
    <footer>
        <p>联系团长！: <a href="https://x.com/reiovo_o_" target="_blank">@reiovo_o_</a></p>
    </footer>
    <script>
        // Handle message board submission
        const form = document.getElementById('messageForm');
        const messages = document.getElementById('messages');

        form.addEventListener('submit', function(event) {
            event.preventDefault();
            const username = document.getElementById('username').value || "匿名";
            const messageContent = document.getElementById('messageContent').value;
            
            const message = document.createElement('div');
            message.className = 'message';
            message.innerHTML = `<strong>${username}:</strong> ${messageContent}`;
            messages.prepend(message);

            form.reset();
        });
    </script>
</body>
</html>
