# Roomyfastfake.github.io
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <title>LOCK IN — Countdown</title>
  <style>
    body {
      margin:0;
      height:100vh;
      background:#000;
      color:#fff;
      display:flex;
      flex-direction:column;
      align-items:center;
      justify-content:center;
      font-family: Inter, Arial, sans-serif;
      text-align:center;
    }
    h1 { font-size:60px; margin:0; }
    h2 { font-size:24px; font-weight:400; color:#9aa0a6; margin:12px 0 40px; }
    .countdown { display:flex; gap:24px; }
    .unit {
      background:rgba(255,255,255,0.05);
      padding:20px 24px;
      border-radius:12px;
      min-width:120px;
    }
    .num { font-size:42px; font-weight:700; }
    .label { font-size:14px; color:#aaa; margin-top:6px; text-transform:uppercase; }
  </style>
</head>
<body>
  <h1>AIR < 50 — IIT Bombay CSE</h1>
  <h2>911 Turbo S. Mansion. Generational wealth.</h2>
  <div class="countdown">
    <div class="unit"><div class="num" id="days">0</div><div class="label">Days</div></div>
    <div class="unit"><div class="num" id="hours">00</div><div class="label">Hours</div></div>
    <div class="unit"><div class="num" id="minutes">00</div><div class="label">Minutes</div></div>
    <div class="unit"><div class="num" id="seconds">00</div><div class="label">Seconds</div></div>
  </div>

<script>
  // Fixed target date: Jan 1, 2027 00:00
  const targetDate = new Date('2027-01-01T00:00:00');

  const daysEl = document.getElementById('days');
  const hoursEl = document.getElementById('hours');
  const minutesEl = document.getElementById('minutes');
  const secondsEl = document.getElementById('seconds');

  function pad(n){ return n < 10 ? '0' + n : n; }

  function update() {
    const now = new Date();
    let diff = targetDate - now;
    if (diff <= 0) {
      daysEl.textContent = '0';
      hoursEl.textContent = '00';
      minutesEl.textContent = '00';
      secondsEl.textContent = '00';
      return;
    }
    const sec = Math.floor(diff/1000);
    const days = Math.floor(sec / (3600*24));
    const hours = Math.floor((sec % (3600*24)) / 3600);
    const minutes = Math.floor((sec % 3600) / 60);
    const seconds = sec % 60;

    daysEl.textContent = days;
    hoursEl.textContent = pad(hours);
    minutesEl.textContent = pad(minutes);
    secondsEl.textContent = pad(seconds);
  }

  update();
  setInterval(update, 1000);
</script>
</body>
</html>

