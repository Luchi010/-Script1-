<!doctype html>
<html lang="ja">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>簡単メモ保存サイト</title>
<style>
  body {
    background:#111;
    color:#fff;
    font-family:sans-serif;
    padding:20px;
  }
  textarea {
    width:100%;
    height:200px;
    background:#222;
    color:#fff;
    border:1px solid #444;
    border-radius:8px;
    padding:10px;
    font-size:16px;
  }
  button {
    margin-top:10px;
    padding:10px 20px;
    background:#7c3aed;
    border:none;
    border-radius:8px;
    color:#fff;
    font-size:16px;
  }
</style>
</head>
<body>
  <h1>メモ保存サイト ✨</h1>
  <textarea id="memo"></textarea><br>
  <button onclick="saveMemo()">💾 保存</button>
  <button onclick="loadMemo()">📂 読み込み</button>

<script>
  function saveMemo(){
    const text = document.getElementById("memo").value;
    localStorage.setItem("myMemo", text);
    alert("保存しました！");
  }
  function loadMemo(){
    const text = localStorage.getItem("myMemo");
    if(text !== null){
      document.getElementById("memo").value = text;
      alert("読み込みました！");
    } else {
      alert("保存されているメモはありません。");
    }
  }
</script>
</body>
</html>
