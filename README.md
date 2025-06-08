<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width,initial-scale=1"/>
  <title>Magical Horizon Archive</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');
    body {
      background: #ffe4e1 url('https://i.imgur.com/ISlhk1r.gif') repeat;
      font-family: 'Press Start 2P', cursive;
      color: #000000;
      margin:0; padding:20px;
    }
    .win {
      background: #faf8f0;
      border:4px solid #000080;
      max-width:640px;
      margin: auto;
      box-shadow: 4px 4px 0px #808080;
    }
    .titlebar {
      background:#000080;
      color:#fff;
      padding:4px 8px;
      font-size:14px;
      display:flex;
      justify-content: space-between;
      align-items:center;
    }
    .titlebar .buttons span {
      display:inline-block;
      width:12px; height:12px;
      background:#ff0000;
      margin-left:4px;
    }
    nav {
      background:#fff;
      border:2px solid #000080;
      padding:8px;
      margin-top:8px;
    }
    nav ul{ list-style:none; padding:0;}
    nav li {
      cursor:pointer; padding:6px;
      margin:2px 0;
      background:#e0e0ff;
      border:2px solid #8080ff;
    }
    nav li:hover{background:#c0c0ff;}
    .submenu{display:none; margin-left:20px;}
    main {
      padding:10px;
      background:#fff;
      border-top:2px solid #000080;
      min-height:160px;
    }
    button {
      margin:10px; padding:6px 12px;
      background:#000080;
      color:#fff;
      border:none;
      cursor:pointer;
      font-family:'Press Start 2P',cursive;
    }
    button:hover{background:#4040ff;}
  </style>
</head>
<body>

<div class="win">
  <div class="titlebar">
    <div>Sunshine Days Archive</div>
    <div class="buttons">
      <span></span><span></span><span></span>
    </div>
  </div>

  <nav>
    <ul>
      <li onclick="toggleSub('s1')">Season 1</li>
      <ul id="s1" class="submenu">
        <li onclick="showEp('Episode 1: The Beginning')">Ep 1: The Beginning</li>
        <!-- ... jusqu'à Ep 12 -->
        <li onclick="showEp('Episode 12: The End')">Ep 12: The End</li>
      </ul>
      <li onclick="toggleSub('s2')">Season 2</li>
      <ul id="s2" class="submenu">
        <li onclick="showEp('Uh oh nothing anymore !')">Uh oh nothing anymore !</li>
      </ul>
      <li onclick="toggleSub('s3')">Season 3</li>
      <ul id="s3" class="submenu">
        <li onclick="showEp('Uh oh nothing anymore !')">Uh oh nothing anymore !</li>
      </ul>
      <li onclick="toggleSub('s4')">Season 4</li>
      <ul id="s4" class="submenu">
        <li onclick="showEp('Uh oh nothing anymore !')">Uh oh nothing anymore !</li>
      </ul>
    </ul>
  </nav>

  <main id="content">
    <p>ようこそ！このサイトは「Sunshine Days」のアーカイブです。  
    このサイトは2014年に閉鎖されましたが、ファンが内容を保存しています。(•‿•)</p>
  </main>

  <button onclick="toggleLang()">🇯🇵/🇺🇸</button>
</div>

<script>
  function toggleSub(id) {
    const el = document.getElementById(id);
    el.style.display = el.style.display === 'block' ? 'none' : 'block';
  }

  function showEp(title) {
    const cnt = document.getElementById('content');
    if(title.includes('Uh oh')) {
      cnt.innerHTML = `<h2>${title}</h2><p>Sorry, this episode is lost or never existed. (•﹏•)</p>`;
    } else {
      cnt.innerHTML = `<h2>${title}</h2><p>Episode info has vanished, but memories remain! (✿◕‿◕)</p>`;
    }
  }

  let jap = true;
  function toggleLang() {
    const cnt = document.getElementById('content');
    if(jap) {
      cnt.innerHTML = `<p>Welcome! This is an archive for “Sunshine Days”.<br>
        The original site closed in 2014, but fans saved what they could. (•‿•)</p>`;
    } else {
      cnt.innerHTML = `<p>ようこそ！このサイトは「Sunshine Days」のアーカイブです。<br>
        このサイトは2014年に閉鎖されましたが、ファンが内容を保存しています。(•‿•)</p>`;
    }
    jap = !jap;
  }
</script>

</body>
</html>
