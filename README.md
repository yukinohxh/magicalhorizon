<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<title>Magical Horizon Archive - Sunshine Days</title>
<style>
  body {
    background-color: #008080; /* teal desktop background */
    margin: 0; padding: 20px;
    font-family: 'Courier New', monospace;
  }
  .window {
    width: 600px;
    border: 2px solid #000;
    background: #C0C0C0;
    box-shadow: 4px 4px 0 #666;
    margin: 0 auto;
  }
  .title-bar {
    background: #000080;
    color: white;
    padding: 4px;
    font-size: 14px;
    display: flex;
    justify-content: space-between;
  }
  .title-bar .title { font-weight: bold; }
  .title-bar .buttons span {
    display: inline-block;
    width: 16px; height: 14px;
    margin-left: 2px;
    background: #C0C0C0;
    border: 2px solid #fff;
    box-shadow: inset -1px -1px 0 #000;
    text-align: center;
    line-height: 14px;
    font-weight: bold;
    cursor: default;
  }
  .menu-bar {
    background: #C0C0C0;
    padding: 4px;
    border-top: 1px solid #fff;
    border-bottom: 1px solid #777;
  }
  .menu-bar span {
    margin-right: 12px;
    cursor: default;
  }
  .content {
    background: white;
    padding: 10px;
    height: 300px;
    overflow-y: auto;
    font-size: 14px;
  }
  .footer {
    background: #C0C0C0;
    padding: 4px;
    font-size: 12px;
  }
  a.translate-btn {
    display: inline-block;
    margin-top: 10px;
    background: #000080;
    color: #fff;
    padding: 4px 8px;
    text-decoration: none;
    font-size: 12px;
  }
</style>
</head>
<body>

<div class="window">
  <div class="title-bar">
    <div class="title">magicalhorizon.web‑jp.cc</div>
    <div class="buttons">
      <span>—</span><span>□</span><span>✕</span>
    </div>
  </div>
  <div class="menu-bar">
    <span>File</span><span>Edit</span><span>View</span><span>Help</span>
  </div>
  <div class="content" id="main-content">
    <p>ようこそ、皆さん。😊<br><br>
    このサイトは**Sunshine Days**のアーカイブですが、2014年に閉鎖されました。<br>
    心の中では…物語は今も続いていると私は信じています。<br><br>
    キャラクターたちは私と友達自身。<br>
    誰かの夜に小さな光になっていたのなら、それが私の宝物です。<br><br>
    魔法は見えないところにある。<br>
    そして…あなたの心の中にも。それを忘れないでください。<br><br>
    🌸 RibbonDreamzより<br>
    (2014年12月21日)</p>
    <a href="#" class="translate-btn" onclick="translate(); return false;">Translate / 翻訳</a>
  </div>
  <div class="footer">
    Microsoft Internet Explorer -- 6.0   |   Windows 2000
  </div>
</div>

<script>
  let isJap = true;
  const main = document.getElementById('main-content');

  function translate(){
    if(isJap){
      main.innerHTML = `
        <p>Hello everyone! 😊<br><br>
        This site is an archive of <b>Sunshine Days</b>, but it was closed in 2014.<br>
        I believe the story still lives in your hearts.<br><br>
        The characters come from me and my friends.<br>
        If they ever shone as a little light in your night, that means the world to me.<br><br>
        Magic exists where you cannot see it.<br>
        And it lives... in your heart too. Please don’t forget.<br><br>
        🌸 From RibbonDreamz<br>
        (December 21, 2014)</p>
        <a href="#" class="translate-btn" onclick="translate(); return false;">日本語 / Japanese</a>
      `;
      isJap = false;
    } else {
      main.innerHTML = `
        <p>ようこそ、皆さん。😊<br><br>
        このサイトは**Sunshine Days**のアーカイブですが、2014年に閉鎖されました。<br>
        心の中では…物語は今も続いていると私は信じています。<br><br>
        キャラクターたちは私と友達自身。<br>
        誰かの夜に小さな光になっていたのなら、それが私の宝物です。<br><br>
        魔法は見えないところにある。<br>
        そして…あなたの心の中にも。それを忘れないでください。<br><br>
        🌸 RibbonDreamzより<br>
        (2014年12月21日)</p>
        <a href="#" class="translate-btn" onclick="translate(); return false;">Translate / 翻訳</a>
      `;
      isJap = true;
    }
  }
</script>

</body>
</html>
