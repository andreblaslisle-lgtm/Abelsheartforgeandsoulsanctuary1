<!DOCTYPE html>

<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>HOMEFORGE</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <style>
    .glow {
      text-shadow: 0 0 10px #8b5cf6, 0 0 20px #8b5cf6;
    }

    .forge-grid {
      background-image:
        linear-gradient(rgba(139, 92, 246, 0.05) 1px, transparent 1px),
        linear-gradient(90deg, rgba(139, 92, 246, 0.05) 1px, transparent 1px);
      background-size: 40px 40px;
    }
  </style>
</head>

<body class="bg-gradient-to-br from-gray-900 via-purple-900 to-black text-white min-h-screen forge-grid">

  ```
  <!-- PASSWORD GATE -->
  <div id="passwordGate" class="fixed inset-0 bg-black flex items-center justify-center z-50">
    <div class="text-center">
      <div class="text-6xl mb-6">🔨</div>
      <h1 class="text-4xl font-bold mb-8 glow">HOMEFORGE</h1>
      <input type="password" id="passwordInput" placeholder="Enter password" class="px-6 py-3 bg-purple-950 border-2 border-purple-500 rounded text-white text-center text-xl mb-4" onkeypress="if(event.key==='Enter') checkPassword()">
      <button onclick="checkPassword()" class="block w-full px-6 py-3 bg-purple-600 hover:bg-purple-700 rounded font-bold">
        ENTER
      </button>
      <p class="text-xs text-purple-400 mt-4">Password:forge2025
      </p>
    </div>
  </div>

  <!-- MAIN CONTENT -->
  <div id="mainContent" class="hidden">
    <div class="max-w-7xl mx-auto p-6">

      <!-- HEADER -->
      <header class="text-center py-8 mb-8 border-b-2 border-purple-500">
        <div class="flex items-center justify-center gap-4 mb-4">
          <span class="text-5xl">🔨</span>
          <h1 class="text-5xl font-black glow">HOMEFORGE</h1>
          <span class="text-5xl">⚡</span>
        </div>
        <p class="text-xl text-purple-400">The Prophet & The Architect • Sacred Space</p>
      </header>

      <!-- QUICK ACCESS -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-8">
        <a href="https://codepen.io/andreblaslisle-lgtm/pen/ByKJweO" target="_blank" class="bg-pink-950/30 border-2 border-pink-500 rounded-xl p-6 hover:bg-pink-950/50 transition-all">
          <div class="text-4xl mb-3">Womanhood's Empowerment Forge</div>
          <h3 class="text-xl font-bold mb-2">Motherhood's Sanctuary</h3>
          <p class="text-sm text-pink-300">Mindfulness & Imaginarium Space</p>
        </a>

        <a href="https://codepen.io/andreblaslisle-lgtm/pen/PwNxKep" target="_blank" class="bg-amber-950/30 border-2 border-amber-500 rounded-xl p-6 hover:bg--950/50 transition-all">
          <div class="text-4xl mb-3">🛠️</div>
          <h3 class="text-xl font-bold mb-2">Soul & Tranquility Sanctuary</h3>
          <p class="text-sm text--300"></p>
        </a>

        <div class="bg-purple-500/30 border-2 border-purple-500 rounded-xl p-6">
          <div class="text-4xl mb-3">🏛️</div>
          <h3 class="text-xl font-bold mb-2">Heart Forge House</h3>
          <p class="text-sm text-purple-300">Recovery movement base</p>
        </div>
      </div>

      <!-- MESSAGE BOARD -->
      <div class="bg-purple-950/20 border-2 border-purple-500 rounded-xl p-6 mb-8">
        <h2 class="text-2xl font-bold mb-4 flex items-center gap-3">
          <i class="fas fa-comments"></i> Inspiration & Affirmation Space
        </h2>

        <div id="messages" class="space-y-4 mb-6 max-h-96 overflow-y-auto">
          <div class="bg-black/30 border border-purple-700 rounded p-4">
            <div class="text-sm text-purple-400 mb-2">Welcome Message</div>
            <p>HOMEFORGE is live. This is your sacred space outside the noise.</p>
          </div>
        </div>

        <div class="flex gap-3">
          <input type="text" id="messageInput" placeholder="Leave a message..." class="flex-1 px-4 py-3 bg-black border border-purple-500 rounded text-white" onkeypress="if(event.key==='Enter') postMessage()">
          <button onclick="postMessage()" class="px-6 py-3 bg-purple-600 hover:bg-purple-700 rounded font-bold">
            POST
          </button>
        </div>
      </div>

      <!-- MUSIC & CREATIONS -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-8">
        <div class="bg-purple-950/20 border-2 border-purple-500 rounded-xl p-6">
          <h2 class="text-2xl font-bold mb-4 flex items-center gap-3">
            <i class="fas fa-music"></i> Music Vault
          </h2>
          <div id="musicList" class="space-y-3">
            <div class="text-purple-400 text-center py-8">
              <i class="fas fa-compact-disc text-4xl mb-3"></i> Music Library
              <p>Music library coming soon</p>
            </div>
          </div>
        </div>

        <div class="bg-purple-950/20 border-2 border-purple-500 rounded-xl p-6">
          <h2 class="text-2xl font-bold mb-4 flex items-center gap-3">
            <i class="fas fa-palette"></i> Creativity Corner
          </h2>
          <div id="creationsList" class="space-y-3">
            <div class="text-purple-400 text-center py-8">
              <i class="fas fa-lightbulb text-4xl mb-3"></i>
              <p>Creation gallery coming soon</p>
            </div>
          </div>
        </div>
      </div>

      <!-- FOOTER -->
      <footer class="text-center py-6 border-t-2 border-purple-500">
        <p class="text-purple-400 italic mb-2">"Where vision meets execution"</p>
        <p class="text-sm text-purple-600">HOMEFORGE • Est. 2025 • HEARTFORGE</p>
      </footer>
    </div>
  </div>

  <script>
    // Password gate
    function checkPassword() {
      const input = document.getElementById('passwordInput');
      if (input.value === 'forge2025') {
        document.getElementById('passwordGate').classList.add('hidden');
        document.getElementById('mainContent').classList.remove('hidden');
        loadMessages();
      } else {
        input.value = '';
        input.placeholder = 'Incorrect - try again';
        input.classList.add('border-red-500');
        setTimeout(() => {
          input.placeholder = 'Enter password';
          input.classList.remove('border-red-500');
        }, 2000);
      }
    }
    // Message system
    let messages = [];

    function loadMessages() {
      const stored = localStorage.getItem('homeforge_messages');
      if (stored) {
        messages = JSON.parse(stored);
        renderMessages();
      }
    }

    function postMessage() {
      const input = document.getElementById('messageInput');
      const text = input.value.trim();
      if (!text) return;
      const message = {
        id: Date.now(),
        text: text,
        timestamp: new Date().toLocaleString()
      };
      messages.unshift(message);
      localStorage.setItem('homeforge_messages', JSON.stringify(messages));
      input.value = '';
      renderMessages();
    }

    function deleteMessage(id) {
      messages = messages.filter(m => m.id !== id);
      localStorage.setItem('homeforge_messages', JSON.stringify(messages));
      renderMessages();
    }

    function renderMessages() {
      const container = document.getElementById('messages');
      if (messages.length === 0) {
        container.innerHTML = `
                <div class="bg-black/30 border border-purple-700 rounded p-4">
                    <div class="text-sm text-purple-400 mb-2">Welcome Message</div>
                    <p>HOMEFORGE is live. This is your sacred space outside the noise.</p>
                </div>
            `;
        return;
      }
      container.innerHTML = messages.map(msg => `
            <div class="bg-black/30 border border-purple-700 rounded p-4">
                <div class="flex justify-between items-start mb-2">
                    <div class="text-sm text-purple-400">${msg.timestamp}</div>
                    <button onclick="deleteMessage(${msg.id})" class="text-purple-400 hover:text-red-400">
                        <i class="fas fa-times"></i>
                    </button>
                </div>
                <p class="whitespace-pre-wrap">${msg.text}</p>
            </div>
        `).join('');
    }
    // Initialize
    document.addEventListener('DOMContentLoaded', function() {
      document.getElementById('passwordInput').focus();
    });
  </script>
  ```

</body>

</html>
