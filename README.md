# Pasandida-mard-
hello nimmi ilyf !
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Nimmi 💖 Gittu Chat</title>
  <style>
    body {
      font-family: 'Comic Sans MS', cursive, sans-serif;
      background: linear-gradient(135deg, #ffd6ff, #e7c6ff);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }
    .chat-box {
      width: 350px;
      height: 500px;
      background: white;
      border-radius: 20px;
      box-shadow: 0 0 15px rgba(0,0,0,0.2);
      display: flex;
      flex-direction: column;
      overflow: hidden;
    }
    .messages {
      flex: 1;
      padding: 15px;
      overflow-y: auto;
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
    .user, .bot {
      padding: 10px;
      border-radius: 10px;
      max-width: 80%;
      word-wrap: break-word;
    }
    .user {
      background: #c8b6ff;
      align-self: flex-end;
    }
    .bot {
      background: #ffc6ff;
      align-self: flex-start;
    }
    .input-area {
      display: flex;
      padding: 10px;
      border-top: 2px solid #ccc;
    }
    input {
      flex: 1;
      border: none;
      outline: none;
      padding: 10px;
      border-radius: 10px;
      background: #f2f2f2;
      font-size: 14px;
    }
    button {
      margin-left: 10px;
      border: none;
      background: #b8c0ff;
      color: white;
      padding: 10px 15px;
      border-radius: 10px;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover {
      background: #a0a0ff;
    }
  </style>
</head>
<body>
  <div class="chat-box">
    <div class="messages" id="chat"></div>
    <div class="input-area">
      <input type="text" id="userInput" placeholder="Type a message..." />
      <button onclick="sendMessage()">Send</button>
    </div>
  </div>

  <script>
    const chat = document.getElementById('chat');
    const input = document.getElementById('userInput');

    function addMessage(text, sender) {
      const msg = document.createElement('div');
      msg.classList.add(sender);
      msg.innerText = text;
      chat.appendChild(msg);
      chat.scrollTop = chat.scrollHeight;
    }

    function sendMessage() {
      const text = input.value.trim();
      if (!text) return;
      addMessage(text, 'user');
      input.value = '';

      const reply = getReply(text);
      setTimeout(() => addMessage(reply, 'bot'), 400);
    }

    function getReply(text) {
      const msg = text.toLowerCase();

      if (msg.includes('ily gittu') || msg.includes('i love you gittu') || msg.includes('ilyf')) {
        return 'I LOVE YOU FOREVER MY NIMMI END EVER END EVER 😸😙💖';
      }
      if (msg === 'kkrh') {
        return 'MERI PATNI SHREE SE BAATE';
      }
      if (msg === 'bui bui') {
        return 'OK BABAAYYY😙, BUI BUI LOVE U FOREVER TAKE CARE ! MWAHHH';
      }
      if (msg === 'hehe') {
        return 'badmos😭';
      }
      if (msg === 'pic do👀' || msg === 'pic do' || msg.includes('👀 pic')) {
        return 'hawasi aurat😾';
      }
      if (msg === 'kal scl aoge?' || msg.includes('school aoge')) {
        return 'ofc aunga bby tumhare liyeh hi toh scl jata hu😸💖';
      }
      if (msg === 'bie') {
        return 'kyaaa huii😭😭 sorry sorrry babeeeeeeee gussa mat hooo ilyf😭💖';
      }
      if (msg === '👀') {
        return 'ese tukur tukur kya dekh rhe ho👀😗 Chalo paas aoo hehehe';
      }
      if (msg.includes('tumse gussa hu')) {
        return 'qqqqqq😭😭😭 bataooo tumhee kya huaaa';
      }
      if (msg.startsWith('good morning baby')) {
        return 'goood morning bachhuuu have a cookie pookie dayyy love u forever ❤️‍🩹😙';
      }

      return 'hmmm kyaaa 😙💞';
    }

    input.addEventListener('keypress', function(e) {
      if (e.key === 'Enter') sendMessage();
    });
  </script>
</body>
</html>
