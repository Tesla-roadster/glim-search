# glim-search
```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>glim.</title>
<style>
* { box-sizing: border-box; }
body {
  margin: 0; min-height: 100vh; padding: 30px 16px;
  background: radial-gradient(ellipse at top, #30234b, #100d19 70%);
  color: white; font-family: Arial, sans-serif;
  display: flex; flex-direction: column; align-items: center;
  justify-content: center;
}
h1 { font-size: 72px; letter-spacing: -5px; margin: 0; }
h1 span { color: #baff7a; }
p { color: #aaa3bb; }
form {
  display: flex; width: min(600px, 100%); padding: 8px;
  background: #211b30; border: 1px solid #493b5c;
  border-radius: 18px;
}
input {
  flex: 1; min-width: 0; padding: 14px; color: white;
  background: transparent; border: 0; outline: none;
  font-size: 16px;
}
button {
  background: #baff7a; border: 0; border-radius: 12px;
  padding: 0 18px; font-weight: bold; cursor: pointer;
}
.links {
  display: flex; flex-wrap: wrap; justify-content: center;
  gap: 12px; margin-top: 30px;
}
a {
  color: white; text-decoration: none; padding: 15px;
  background: #211b30; border: 1px solid #493b5c;
  border-radius: 12px;
}
a:hover { border-color: #baff7a; }
</style>
</head>
<body>
  <h1>glim<span>.</span></h1>
  <p>Your internet, your way.</p>

  <form id="search">
    <input id="q" placeholder="Search anything..." required>
    <button>Search ↗</button>
  </form>

  <div class="links">
    <a href="https://youtube.com">▶ YouTube</a>
    <a href="https://discord.com/app">Discord</a>
    <a href="https://roblox.com">Roblox</a>
    <a href="https://twitch.tv">Twitch</a>
    <a href="https://reddit.com">Reddit</a>
  </div>

  <script>
    document.getElementById('search').addEventListener('submit', e => {
      e.preventDefault();
      const q = document.getElementById('q').value.trim();
      if (q) location.href =
        'https://www.google.com/search?q=' + encodeURIComponent(q);
    });
  </script>
</body>
</html>
```
