# Chaba-is-me
Тестовый сайт по заказу видеомонтажа

<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#07130d">
<title>CHABA IS ME | ARTUR</title>

<style>
:root {
  --green: #a7ff4f;
  --dark: #061109;
  --panel: #10251a;
  --text: #f4fff5;
  --muted: #a4b4a8;
}

* { box-sizing: border-box; margin: 0; padding: 0; }

html { scroll-behavior: smooth; }

body {
  background:
    radial-gradient(ellipse at 10% 10%, #235b30 0%, transparent 40%),
    radial-gradient(ellipse at 90% 35%, #174b29 0%, transparent 38%),
    radial-gradient(ellipse at 50% 100%, #174323 0%, transparent 45%),
    linear-gradient(145deg, #07130d, #0c2112, #061109);
  background-attachment: fixed;
  color: var(--text);
  font-family: Arial, sans-serif;
}

a { text-decoration: none; color: inherit; }
button { cursor: pointer; font: inherit; }

.container {
  width: min(1150px, 90%);
  margin: auto;
}

header {
  position: sticky;
  top: 0;
  z-index: 10;
  background: rgba(4, 17, 9, .9);
  backdrop-filter: blur(15px);
  border-bottom: 1px solid #315b36;
}

.nav {
  min-height: 75px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
}

.logo {
  font-size: 22px;
  font-weight: 900;
  letter-spacing: 2px;
}

.logo span { color: var(--green); }

nav {
  display: flex;
  gap: 22px;
  align-items: center;
  font-size: 13px;
  color: #c4d7c7;
}

nav a:hover { color: var(--green); }

.cart-link {
  border: 1px solid #568d46;
  padding: 10px 14px;
  border-radius: 30px;
  color: var(--green);
}

.hero {
  min-height: 570px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 90px 0;
}

.tag {
  color: var(--green);
  font-size: 12px;
  font-weight: bold;
  letter-spacing: 4px;
}

h1 {
  font-size: clamp(60px, 11vw, 115px);
  line-height: .9;
  letter-spacing: -6px;
  margin: 25px 0;
}

h1 span { color: var(--green); }

.hero p {
  max-width: 520px;
  color: #c0d0c3;
  line-height: 1.8;
  font-size: 16px;
}

.btn {
  display: inline-block;
  padding: 15px 23px;
  background: var(--green);
  color: #07130d;
  border: none;
  border-radius: 10px;
  font-weight: 900;
  font-size: 12px;
  margin-top: 25px;
  transition: .25s;
}

.btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 0 25px #a7ff4f66;
}

.btn-outline {
  background: transparent;
  border: 1px solid #8bd94d;
  color: white;
  margin-left: 10px;
}

section {
  padding: 75px 0;
  scroll-margin-top: 85px;
}

h2 {
  font-size: clamp(32px, 5vw, 48px);
  margin: 12px 0 25px;
}

.green { color: var(--green); }

.paper-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 15px;
}

.paper {
  background: linear-gradient(145deg, #1b4828, #0b2112);
  border: 1px solid #477d40;
  border-radius: 18px;
  padding: 25px;
  min-height: 180px;
  transition: .3s;
}

.paper:hover {
  transform: translateY(-7px);
  border-color: var(--green);
  box-shadow: 0 10px 35px #8bff4f20;
}

.paper .icon {
  font-size: 30px;
  display: block;
  margin: 20px 0;
}

.paper strong { font-size: 19px; }
.paper p { color: var(--muted); font-size: 13px; margin-top: 8px; }

.panel {
  background: linear-gradient(145deg, #153720eF, #0b1b10f5);
  border: 1px solid #345f39;
  border-radius: 20px;
  padding: 25px;
}

.about-grid {
  display: grid;
  grid-template-columns: 1fr 1.3fr;
  gap: 20px;
}

.about-name {
  min-height: 260px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  background: radial-gradient(circle at 70% 25%, #8bff4f55, transparent 45%), #102d19;
}

.about-name h3 {
  font-size: clamp(50px, 8vw, 85px);
  letter-spacing: -5px;
}

.about-name h3 span { color: var(--green); }

.about-text {
  color: #c4d5c7;
  line-height: 1.9;
}

.chips {
  display: flex;
  flex-wrap: wrap;
  gap: 9px;
  margin-top: 22px;
}

.chip {
  border: 1px solid #568d46;
  padding: 9px 13px;
  border-radius: 30px;
  font-size: 12px;
  color: var(--green);
}

.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 18px;
}

.project {
  overflow: hidden;
  padding: 0;
}

.preview {
  aspect-ratio: 16/10;
  background: linear-gradient(135deg, #245c31, #07130d);
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

.preview video,
.preview iframe {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border: 0;
}

.play {
  font-size: 42px;
  color: var(--green);
}

.project-info { padding: 18px; }
.project-info h3 { margin-bottom: 8px; }
.project-info p { color: var(--muted); font-size: 13px; line-height: 1.6; }

.service p {
  color: var(--muted);
  line-height: 1.7;
  font-size: 14px;
  margin-top: 12px;
}

.price {
  color: var(--green);
  font-weight: bold;
  font-size: 13px;
  margin-top: 20px;
}

.service .btn { width: 100%; }

input, textarea {
  width: 100%;
  background: #07150b;
  border: 1px solid #477348;
  border-radius: 10px;
  padding: 14px;
  color: white;
  margin: 9px 0;
  outline: none;
}

input:focus, textarea:focus { border-color: var(--green); }

textarea { min-height: 110px; resize: vertical; }

.upload-box {
  margin-top: 25px;
  border: 1px dashed #76b94c;
  padding: 22px;
  border-radius: 15px;
}

.upload-box input[type=file] { border: none; }

.cart-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-bottom: 1px solid #315b36;
  padding: 15px 0;
}

.remove {
  background: transparent;
  border: none;
  color: #ff8585;
  font-size: 20px;
}

footer {
  border-top: 1px solid #315b36;
  padding: 35px 0;
  text-align: center;
  color: #9caf9f;
  font-size: 13px;
}

@media(max-width: 800px) {
  .paper-grid { grid-template-columns: repeat(2, 1fr); }
  .grid { grid-template-columns: repeat(2, 1fr); }
}

@media(max-width: 600px) {
  .nav { flex-direction: column; padding: 18px 0; }
  nav { flex-wrap: wrap; justify-content: center; gap: 14px; }
  .hero { min-height: 480px; }
  .about-grid, .grid { grid-template-columns: 1fr; }
  .paper-grid { grid-template-columns: repeat(2, 1fr); }
  h1 { letter-spacing: -3px; }
  .btn-outline { margin-left: 0; }
}
</style>
</head>

<body>

<header>
  <div class="container nav">
    <a href="#home" class="logo">CHABA <span>IS ME.</span></a>
    <nav>
      <a href="#about">Обо мне</a>
      <a href="#projects">Проекты</a>
      <a href="#services">Услуги</a>
      <a href="#cart" class="cart-link">Корзина <b id="count">0</b></a>
    </nav>
  </div>
</header>

<main>

<div class="container hero" id="home">
  <div class="tag">VIDEO EDITOR / CREATIVE STUDIO</div>
  <h1>MAKE IT<br><span>LOOK</span> DIFFERENT.</h1>
  <p>
    Привет! Я Артур. Занимаюсь видеомонтажом,
    создаю Reels, Shorts, игровые видео и
    атмосферные ролики. Превращаю обычные кадры
    в нечто особенное.
  </p>
  <div>
    <a href="#projects" class="btn">МОИ ПРОЕКТЫ ↗</a>
    <a href="#order" class="btn btn-outline">ЗАКАЗАТЬ</a>
  </div>
</div>

<section class="container">
  <div class="tag">NAVIGATION</div>
  <h2>Выбери <span class="green">раздел.</span></h2>

  <div class="paper-grid">
    <a href="#about" class="paper">
      <span class="tag">01 / PROFILE</span>
      <span class="icon">✳</span>
      <strong>Обо мне</strong>
      <p>Моя история и навыки</p>
    </a>

    <a href="#projects" class="paper">
      <span class="tag">02 / WORKS</span>
      <span class="icon">▶</span>
      <strong>Проекты</strong>
      <p>Мои видеоработы</p>
    </a>

    <a href="#cart" class="paper">
      <span class="tag">03 / CART</span>
      <span class="icon">▤</span>
      <strong>Корзина</strong>
      <p>Выбранные услуги</p>
    </a>

    <a href="#order" class="paper">
      <span class="tag">04 / CONTACT</span>
      <span class="icon">↗</span>
      <strong>Заказать</strong>
      <p>Оформить заявку</p>
    </a>
  </div>
</section>

<section class="container" id="about">
  <div class="tag">ABOUT ME</div>
  <h2>Обо <span class="green">мне.</span></h2>

  <div class="about-grid">
    <div class="panel about-name">
      <div class="tag">VIDEO EDITOR</div>
      <h3>ART<span>UR.</span></h3>
      <p class="tag">CHABA IS ME</p>
    </div>

    <div class="panel">
      <p class="about-text">
        Меня зовут Артур. Я занимаюсь видеомонтажом
        и люблю превращать обычные кадры в красивые
        и динамичные истории. Работаю с короткими
        роликами, игровыми видео, Reels и Shorts.
        Для меня важны атмосфера, ритм и внимание
        к каждой детали.
      </p>

      <div class="chips">
        <span class="chip">Reels / Shorts</span>
        <span class="chip">Gaming</span>
        <span class="chip">Video Editing</span>
        <span class="chip">Transitions</span>
        <span class="chip">Effects</span>
      </div>
    </div>
  </div>
</section>

<section class="container" id="projects">
  <div class="tag">MY CREATIONS</div>
  <h2>Мои <span class="green">проекты.</span></h2>

  <div class="grid" id="videos">
    <article class="panel project">
      <div class="preview"><span class="play">▶</span></div>
      <div class="project-info">
        <h3>Reels / Shorts</h3>
        <p>Динамичный короткий монтаж и переходы.</p>
      </div>
    </article>

    <article class="panel project">
      <div class="preview"><span class="play">▶</span></div>
      <div class="project-info">
        <h3>Gaming Edit</h3>
        <p>Игровые моменты, эффекты и музыка.</p>
      </div>
    </article>

    <article class="panel project">
      <div class="preview"><span class="play">▶</span></div>
      <div class="project-info">
        <h3>Creative Montage</h3>
        <p>Атмосферные видеоролики и визуальные эффекты.</p>
      </div>
    </article>
  </div>

  <div class="panel upload-box">
    <div class="tag">ADD NEW WORK</div>
    <h3 style="margin:12px 0">Добавить проект</h3>

    <input id="videoName" placeholder="Название проекта">
    <input id="videoDesc" placeholder="Описание проекта">
    <input id="videoFile" type="file" accept="video/*">
    <input id="videoUrl" type="url" placeholder="Или ссылка на видео (необязательно)">

    <button class="btn" onclick="addVideo()">ДОБАВИТЬ ПРОЕКТ +</button>

    <p style="color:#9caf9f;font-size:11px;margin-top:12px;line-height:1.6">
      Видео, выбранное с компьютера, будет доступно только в текущем просмотре.
      Для публикации всем посетителям используй общедоступную ссылку на видео.
    </p>
  </div>
</section>

<section class="container" id="services">
  <div class="tag">WHAT I DO</div>
  <h2>Мои <span class="green">услуги.</span></h2>

  <div class="grid">
    <div class="panel service">
      <h3>Reels / Shorts</h3>
      <p>Динамичный монтаж коротких видео, музыка, эффекты и переходы.</p>
      <div class="price">Цена по договорённости</div>
      <button class="btn" onclick="addCart('Reels / Shorts')">В КОРЗИНУ +</button>
    </div>

    <div class="panel service">
      <h3>YouTube монтаж</h3>
      <p>Полноценный монтаж роликов, титры, музыка и оформление.</p>
      <div class="price">Цена по договорённости</div>
      <button class="btn" onclick="addCart('YouTube монтаж')">В КОРЗИНУ +</button>
    </div>

    <div class="panel service">
      <h3>Gaming / AMV</h3>
      <p>Игровые нарезки, клипы, эффекты и атмосферный монтаж.</p>
      <div class="price">Цена по договорённости</div>
      <button class="btn" onclick="addCart('Gaming / AMV')">В КОРЗИНУ +</button>
    </div>
  </div>
</section>

<section class="container" id="cart">
  <div class="tag">YOUR SELECTION</div>
  <h2>Моя <span class="green">корзина.</span></h2>

  <div class="panel">
    <div id="cartItems">
      <p style="color:#9caf9f">Корзина пока пустая.</p>
    </div>
    <button class="btn" onclick="goOrder()">ПЕРЕЙТИ К ЗАКАЗУ ↗</button>
    <button class="btn btn-outline" onclick="clearCart()">ОЧИСТИТЬ</button>
  </div>
</section>

<section class="container" id="order">
  <div class="tag">CONTACT ME</div>
  <h2>Оформить <span class="green">заказ.</span></h2>

  <div class="panel">
    <form id="orderForm">
      <input id="clientName" placeholder="Твоё имя" required>
      <input id="clientContact" placeholder="Твой Telegram или другой контакт" required>
      <textarea id="details" placeholder="Расскажи, какой монтаж тебе нужен..."></textarea>
      <button class="btn" type="submit">ОТПРАВИТЬ ЗАЯВКУ ↗</button>
    </form>
  </div>
</section>

</main>

<footer>
  <div class="logo">CHABA <span>IS ME.</span></div>
  <p style="margin-top:12px">ARTUR · VIDEO EDITOR</p>
  <p style="margin-top:8px">© 2026 All rights reserved.</p>
</footer>

<script>
const EMAIL = "progamerrutr.com@gmail.com";
let cart = [];

function addCart(name) {
  cart.push(name);
  renderCart();
}

function renderCart() {
  document.getElementById("count").textContent = cart.length;

  const box = document.getElementById("cartItems");
  box.innerHTML = "";

  if (cart.length === 0) {
    box.innerHTML = '<p style="color:#9caf9f">Корзина пока пустая.</p>';
    return;
  }

  cart.forEach((item, index) => {
    const row = document.createElement("div");
    row.className = "cart-item";

    const name = document.createElement("span");
    name.textContent = item;

    const remove = document.createElement("button");
    remove.className = "remove";
    remove.textContent = "×";
    remove.onclick = () => {
      cart.splice(index, 1);
      renderCart();
    };

    row.append(name, remove);
    box.appendChild(row);
  });
}

function clearCart() {
  cart = [];
  renderCart();
}

function goOrder() {
  if (cart.length === 0) {
    alert("Сначала добавь услугу в корзину!");
    return;
  }

  document.getElementById("details").value =
    "Выбранные услуги: " + cart.join(", ") + "\n\n";
  document.getElementById("order").scrollIntoView({behavior:"smooth"});
}

function addVideo() {
  const file = document.getElementById("videoFile").files[0];
  const name = document.getElementById("videoName").value.trim() || "Мой проект";
  const desc = document.getElementById("videoDesc").value.trim() || "Video editing · Chaba is me";
  const url = document.getElementById("videoUrl").value.trim();

  if (!file && !url) {
    alert("Выбери видео или вставь ссылку!");
    return;
  }

  const card = document.createElement("article");
  card.className = "panel project";

  const preview = document.createElement("div");
  preview.className = "preview";

  if (file) {
    const video = document.createElement("video");
    video.src = URL.createObjectURL(file);
    video.controls = true;
    video.playsInline = true;
    preview.appendChild(video);
  } else {
    const link = document.createElement("a");
    link.href = url;
    link.target = "_blank";
    link.rel = "noopener noreferrer";
    link.className = "play";
    link.textContent = "▶";
    preview.appendChild(link);
  }

  const info = document.createElement("div");
  info.className = "project-info";

  const title = document.createElement("h3");
  title.textContent = name;

  const description = document.createElement("p");
  description.textContent = desc;

  info.append(title, description);
  card.append(preview, info);

  document.getElementById("videos").prepend(card);

  document.getElementById("videoName").value = "";
  document.getElementById("videoDesc").value = "";
  document.getElementById("videoFile").value = "";
  document.getElementById("videoUrl").value = "";
}

document.getElementById("orderForm").addEventListener("submit", function(e) {
  e.preventDefault();

  const name = document.getElementById("clientName").value;
  const contact = document.getElementById("clientContact").value;
  const details = document.getElementById("details").value;

  const subject = "Заказ видеомонтажа — Chaba is me";
  const body =
    "Здравствуйте, Артур!\n\n" +
    "Имя: " + name + "\n" +
    "Контакт: " + contact + "\n" +
    "Услуги: " + (cart.join(", ") || "Не выбраны") + "\n\n" +
    "Описание заказа:\n" + details;

  window.location.href =
    "mailto:" + EMAIL +
    "?subject=" + encodeURIComponent(subject) +
    "&body=" + encodeURIComponent(body);
});

renderCart();
</script>

</body>
</html>
