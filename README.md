<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Magical Horizon - Sunshine Days Archive</title>
<style>
  /* Style pixelisé Windows 2000 cutecore */
  @import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');
  body {
    background: #c0c0c0;
    font-family: 'Press Start 2P', cursive, monospace;
    color: #000080;
    margin: 0; padding: 10px;
  }
  header {
    background: #000080;
    color: white;
    padding: 15px;
    text-align: center;
    font-size: 16px;
    border: 4px solid #ffffff;
  }
  nav {
    background: #ffffff;
    padding: 10px;
    border: 4px solid #000080;
    margin-top: 10px;
  }
  nav ul {
    list-style: none;
    padding-left: 0;
  }
  nav ul li {
    cursor: pointer;
    padding: 6px;
    border: 2px solid #000080;
    margin: 4px 0;
    background: #e0e0ff;
  }
  nav ul li:hover {
    background: #a0a0ff;
  }
  .submenu {
    margin-left: 20px;
    display: none;
  }
  .submenu li {
    background: #f0f0ff;
    border-color: #8080ff;
  }
  main {
    margin-top: 20px;
    padding: 10px;
    border: 4px solid #000080;
    background: #f8f8ff;
    min-height: 200px;
  }
  button {
    font-family: 'Press Start 2P', cursive;
    background: #000080;
    color: white;
    border: none;
    padding: 6px 12px;
    cursor: pointer;
    margin-top: 10px;
  }
  button:hover {
    background: #4040ff;
  }
</style>
</head>
<body>

<header>
  ✨ Magical Horizon - Sunshine Days Archive ✨
</header>

<nav>
  <ul>
    <li onclick="toggleSubmenu('s1')">Season 1</li>
    <ul id="s1" class="submenu">
      <li onclick="showEpisode('Episode 1: The Beginning')">Episode 1: The Beginning</li>
      <li onclick="showEpisode('Episode 2: Lost Memories')">Episode 2: Lost Memories</li>
      <li onclick="showEpisode('Episode 3: The Secret')">Episode 3: The Secret</li>
      <li onclick="showEpisode('Episode 4: Blooming Heart')">Episode 4: Blooming Heart</li>
      <li onclick="showEpisode('Episode 5: Shadows')">Episode 5: Shadows</li>
      <li onclick="showEpisode('Episode 6: The Pact')">Episode 6: The Pact</li>
      <li onclick="showEpisode('Episode 7: Forbidden Magic')">Episode 7: Forbidden Magic</li>
      <li onclick="showEpisode('Episode 8: The Betrayal')">Episode 8: The Betrayal</li>
      <li onclick="showEpisode('Episode 9: Last Hope')">Episode 9: Last Hope</li>
      <li onclick="showEpisode('Episode 10: Rebirth')">Episode 10: Rebirth</li>
      <li onclick="showEpisode('Episode 11: Farewell')">Episode 11: Farewell</li>
      <li onclick="showEpisode('Episode 12: The End')">Episode 12: The End</li>
    </ul>
    <li onclick="toggleSubmenu('s2')">Season 2</li>
    <ul id="s2" class="submenu">
      <li onclick="showEpisode('Uh oh, nothing anymore!')">Uh oh, nothing anymore!</li>
    </ul>
    <li onclick="toggleSubmenu('s3')">Season 3</li>
    <ul id="s3" class="submenu">
      <li onclick="showEpisode('Uh oh, nothing anymore!')">Uh oh, nothing anymore!</li>
    </ul>
    <li onclick="toggleSubmenu('s4')">Season 4</li>
    <ul id="s4" class="submenu">
      <li onclick="showEpisode('Uh oh, nothing anymore!')">Uh oh, nothing anymore!</li>
    </ul>
  </ul>
</nav>

<main id="content">
  <p>ようこそ！このサイトは「Sunshine Days」のアーカイブです。  
  このサイトは2014年に閉鎖されましたが、ファンが内容を保存しています。(•‿•)</p>
</main>

<button onclick="toggleLanguage()">Translate / 翻訳</button>

<script>
  // Toggle submenu visibility
  function toggleSubmenu(id) {
    const submenu = document.getElementById(id);
    if(submenu.style.display === 'block') {
      submenu.style.display = 'none';
    } else {
      submenu.style.display = 'block';
    }
  }

  // Show episode content
  function showEpisode(title) {
    const content = document.getElementById('content');
    if(title === 'Uh oh, nothing anymore!') {
      content.innerHTML = '<h2>' + title + '</h2><p>Sorry, this episode is lost or never existed. (•﹏•)</p>';
    } else {
      content.innerHTML = '<h2>' + title + '</h2><p>Episode details are lost to time... but the memories stay forever! (✿◕‿◕)</p>';
    }
  }

  // Translate toggle
  let isJapanese = true;
  function toggleLanguage() {
    const content = document.getElementById('content');
    if(isJapanese) {
      content.innerHTML = `
      <p>Welcome! This site is an archive of "Sunshine Days".  
      The original site closed in 2014, but fans saved the content. (•‿•)</p>
      `;
      isJapanese = false;
    } else {
      content.innerHTML = `
      <p>ようこそ！このサイトは「Sunshine Days」のアーカイブです。  
      このサイトは2014年に閉鎖されましたが、ファンが内容を保存しています。(•‿•)</p>
      `;
      isJapanese = true;
    }
  }
</script>

</body>
</html>
