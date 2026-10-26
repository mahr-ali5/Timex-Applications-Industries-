<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>TIMEX APPLICATIONS INDUSTRIES</title>
  <style>
    :root{
      --bg:#071822;
      --bg2:#0d2231;
      --panel:#11293a;
      --panel2:#183a4d;
      --line:#244d62;
      --cyan:#4fe1ff;
      --cyan2:#67d5ff;
      --gold:#f0bf66;
      --text:#edfaff;
      --muted:#a7c7d8;
      --success:#7ce7b2;
      --shadow:0 18px 40px rgba(0,0,0,.35);
    }
    *{box-sizing:border-box}
    html{scroll-behavior:smooth}
    body{
      margin:0;
      font-family:Segoe UI, Tahoma, Arial, sans-serif;
      background:linear-gradient(180deg, var(--bg), #08151d);
      color:var(--text);
    }
    a{text-decoration:none;color:inherit}
    button,input,select{font:inherit}
    .container{max-width:1200px;margin:0 auto;padding:0 18px 40px}
    header{
      position:sticky;top:0;z-index:10;
      backdrop-filter:blur(8px);
      background:rgba(7,24,34,.78);
      border-bottom:1px solid rgba(255,255,255,.06);
    }
    .topbar{
      max-width:1200px; margin:0 auto; padding:16px 18px;
      display:flex; align-items:center; justify-content:space-between; gap:16px;
    }
    .brand{
      display:flex; align-items:center; gap:12px; font-weight:700;
    }
    .logo{
      width:38px;height:38px;border-radius:12px;
      display:grid;place-items:center;
      background:linear-gradient(135deg,var(--cyan),#1ca6d1);
      color:#07202b;font-weight:900;box-shadow:var(--shadow);
    }
    .brand small{
      display:block;color:var(--muted);font-size:11px;letter-spacing:1px;
    }
    .chip{
      padding:8px 14px;border-radius:999px;
      border:1px solid rgba(79,225,255,.28);
      background:rgba(79,225,255,.06);
      color:var(--cyan); font-size:12px; font-weight:700;
    }
    nav{
      display:flex; gap:8px; flex-wrap:wrap;
      padding:10px 0 16px; max-width:1200px; margin:0 auto;
    }
    nav button{
      border:1px solid var(--line);
      background:rgba(255,255,255,.02);
      color:var(--muted);
      border-radius:10px;
      padding:10px 14px;
      cursor:pointer;
      font-weight:700;
    }
    nav button.active, nav button:hover{
      background:linear-gradient(135deg, rgba(79,225,255,.18), rgba(79,225,255,.05));
      border-color:rgba(79,225,255,.45);
      color:var(--text);
    }

    .screen[hidden]{display:none !important}
    .hero{
      display:grid; grid-template-columns:1.3fr .7fr; gap:22px; margin-top:24px;
    }
    .panel{
      background:linear-gradient(180deg, rgba(18,40,58,.92), rgba(13,30,44,.95));
      border:1px solid var(--line);
      border-radius:20px;
      box-shadow:var(--shadow);
    }
    .hero-main{
      padding:30px; position:relative; overflow:hidden;
    }
    .hero-main::before{
      content:"";
      position:absolute; inset:0;
      background:radial-gradient(circle at top right, rgba(79,225,255,.10), transparent 25%);
      pointer-events:none;
    }
    .eyebrow{
      display:inline-block; padding:7px 12px; border-radius:999px;
      background:rgba(79,225,255,.08); border:1px solid rgba(79,225,255,.18);
      color:var(--cyan); font-size:12px; font-weight:700;
    }
    h1{
      margin:18px 0 14px;
      font-size:clamp(2rem,4vw,3.4rem);
      line-height:1.1;
      letter-spacing:-.8px;
    }
    .lead{
      color:var(--muted); line-height:1.9; font-size:16px; max-width:650px;
    }
    .cta{
      display:flex; flex-wrap:wrap; gap:12px; margin-top:22px;
    }
    .btn{
      border:none; border-radius:12px; padding:12px 18px; cursor:pointer; font-weight:700;
    }
    .btn.primary{
      background:linear-gradient(135deg,var(--cyan), var(--cyan2));
      color:#041d2a; box-shadow:0 12px 24px rgba(79,225,255,.28);
    }
    .btn.secondary{
      background:rgba(79,225,255,.06); border:1px solid rgba(79,225,255,.22); color:var(--text);
    }

    .stats-box{
      padding:20px; display:grid; gap:14px;
    }
    .mini-stat{
      background:rgba(255,255,255,.02); border:1px solid var(--line);
      border-radius:16px; padding:18px;
    }
    .label{
      display:block; color:var(--muted); font-size:12px; margin-bottom:8px;
    }
    .mini-stat strong{
      display:block; color:var(--cyan); font-size:28px;
    }
    .mini-stat small{
      display:block; color:var(--muted); margin-top:6px; font-size:12px;
    }

    .grid-2{
      display:grid; grid-template-columns:repeat(2,minmax(0,1fr)); gap:22px; margin-top:24px;
    }
    .section{padding:24px}
    .section-head{
      display:flex; justify-content:space-between; align-items:center; margin-bottom:18px;
    }
    .section-head h2{margin:0; font-size:1.2rem}
    .tag{
      font-size:12px; font-weight:700; color:var(--cyan);
      padding:7px 10px; border-radius:999px; background:rgba(79,225,255,.07);
      border:1px solid rgba(79,225,255,.18);
    }

    .cards{
      display:grid; grid-template-columns:repeat(2,minmax(0,1fr)); gap:14px;
    }
    .feature-card{
      background:rgba(255,255,255,.02); border:1px solid var(--line);
      border-radius:16px; padding:18px;
    }
    .icon{
      width:42px;height:42px; border-radius:12px;
      display:grid;place-items:center;
      background:linear-gradient(135deg, rgba(79,225,255,.2), rgba(79,225,255,.08));
      border:1px solid rgba(79,225,255,.2); color:var(--cyan);
      font-size:20px; margin-bottom:12px;
    }
    .feature-card h3{margin:0 0 8px; font-size:1.05rem}
    .feature-card p{
      margin:0; color:var(--muted); line-height:1.8; font-size:14px;
    }

    .metrics{
      display:grid; grid-template-columns:repeat(3,minmax(0,1fr)); gap:14px;
    }
    .metric{
      background:rgba(255,255,255,.02); border:1px solid var(--line);
      border-radius:16px; padding:18px 12px; text-align:center;
    }
    .metric .name{
      display:block; color:var(--muted); font-size:12px; margin-bottom:10px;
    }
    .metric strong{
      display:block; color:var(--cyan); font-size:1.4rem; margin-bottom:6px;
    }
    .metric small{
      color:var(--muted); font-size:12px;
    }

    .notes{
      margin-top:16px; padding:16px; border-radius:12px;
      background:rgba(255,255,255,.02); border:1px solid var(--line);
      color:var(--muted); line-height:1.9; font-size:14px;
    }

    .canvas-wrap{
      background:rgba(8,24,35,.9); border:1px solid var(--line); border-radius:18px;
      overflow:hidden;
    }
    canvas{
      width:100%; height:auto; display:block; background:#091823; aspect-ratio:16/9;
    }

    .toolbar{
      display:flex; flex-wrap:wrap; gap:10px; margin-top:16px;
    }
    .toolbar button{
      flex:1 1 150px; min-width:140px;
      border:1px solid var(--line);
      background:rgba(255,255,255,.02);
      color:var(--text);
      border-radius:12px;
      padding:11px 14px;
      cursor:pointer; font-weight:700;
    }
    .toolbar .accent{
      background:linear-gradient(135deg,var(--cyan),var(--cyan2));
      color:#071b25; border:none;
    }

    .form-grid{
      display:grid; grid-template-columns:repeat(2,minmax(0,1fr)); gap:16px; margin-top:16px;
    }
    .field{
      display:flex; flex-direction:column; gap:8px;
    }
    .field label{
      color:var(--muted); font-size:13px; font-weight:600;
    }
    .field input, .field select{
      width:100%; background:#0d1f2d; border:1px solid var(--line);
      color:var(--text); border-radius:12px; padding:12px 14px;
      outline:none;
    }
    .field input:focus, .field select:focus{
      border-color:rgba(79,225,255,.6);
      box-shadow:0 0 0 3px rgba(79,225,255,.08);
    }

    .room-list{
      margin-top:18px; display:grid; gap:12px;
    }
    .room-item{
      display:flex; align-items:center; justify-content:space-between; gap:12px;
      background:rgba(255,255,255,.02); border:1px solid var(--line);
      border-radius:14px; padding:12px 14px; cursor:pointer;
    }
    .room-item.active{
      border-color:rgba(79,225,255,.4); background:rgba(79,225,255,.05);
    }
    .room-info{
      display:flex; align-items:center; gap:10px;
    }
    .room-swatch{
      width:14px;height:14px;border-radius:4px;background:var(--cyan);
      box-shadow:0 0 18px rgba(79,225,255,.4);
    }
    .room-name{font-weight:700}
    .room-meta{color:var(--muted); font-size:12px}
    .mini{
      border:1px solid var(--line); background:rgba(255,255,255,.02);
      color:var(--text); border-radius:10px; padding:8px 10px; cursor:pointer;
    }
    .mini.danger{
      color:var(--gold); border-color:rgba(240,191,102,.35);
      background:rgba(240,191,102,.04);
    }

    @media (max-width:900px){
      .hero, .grid-2, .cards, .metrics, .form-grid{grid-template-columns:1fr}
      .hero{grid-template-columns:1fr}
    }
  </style>
</head>
<body>
  <header>
    <div class="topbar">
      <div class="brand">
        <div class="logo">T</div>
        <div>
          TIMEX APPLICATIONS INDUSTRIES
          <small>ENGINEERING & DESIGN</small>
        </div>
      </div>
      <div class="chip">نسخة تجريبية عربية</div>
    </div>

    <nav>
      <button class="active" data-tab="home">الرئيسية</button>
      <button data-tab="plan">التخطيط 2D</button>
      <button data-tab="view">العرض 3D</button>
      <button data-tab="calc">الحسابات</button>
      <button data-tab="report">التقارير</button>
    </nav>
  </header>

  <div class="container">
    <main>
      <section id="home" class="screen">
        <div class="hero">
          <div class="panel hero-main">
            <span class="eyebrow">نظام تصميم ذكي</span>
            <h1>حلول هندسية ذكية للمشاريع</h1>
            <p class="lead">
              منصة عربية متكاملة لتصميم المساحات، إنشاء المخططات الأولية، وعرض التصاميم بطريقة عملية وسريعة.
              مناسبة للمشاريع السكنية، التجارية، الإداريّة، والمستودعات.
            </p>

            <div class="cta">
              <button class="btn primary" data-go="plan">ابدأ التخطيط</button>
              <button class="btn secondary" data-go="calc">حساب التكلفة</button>
            </div>
          </div>

          <div class="panel stats-box">
            <div class="mini-stat">
              <span class="label">المساحة الإجمالية</span>
              <strong id="totalAreaLabel">96 م²</strong>
              <small>مقاس أولي</small>
            </div>

            <div class="mini-stat">
              <span class="label">التكلفة التقديرية</span>
              <strong id="totalCostLabel">115,200</strong>
              <small>حسب السعر الحالي</small>
            </div>

            <div class="mini-stat">
              <span class="label">عدد الغرف</span>
              <strong id="roomCountLabel">3</strong>
              <small>تصميم أساسي</small>
            </div>
          </div>
        </div>

        <div class="grid-2">
          <div class="panel section">
            <div class="section-head">
              <h2>مميزات النظام</h2>
              <span class="tag">مميزة</span>
            </div>

            <div class="cards">
              <div class="feature-card">
                <div class="icon">▦</div>
                <h3>تخطيط 2D</h3>
                <p>إنشاء مخططات أولية بسرعة مع إمكانية تحريك الغرف وتحديد الأبعاد وحجم المساحات.</p>
              </div>

              <div class="feature-card">
                <div class="icon">◈</div>
                <h3>عرض 3D</h3>
                <p>عرض منظوري مبسط لمفهوم المبنى يساعد في فهم المساحات والاتجاهات بشكل أوضح.</p>
              </div>

              <div class="feature-card">
                <div class="icon">⌁</div>
                <h3>حسابات تقديرية</h3>
                <p>إدخال الطول والعرض مع حساب المساحة والتكلفة على الفور وفق نوع المشروع.</p>
              </div>

              <div class="feature-card">
                <div class="icon">⚙</div>
                <h3>تصدير البيانات</h3>
                <p>يمكنك حفظ المشروع محليًا أو تصدير بياناته بصيغة JSON أو صورة PNG.</p>
              </div>
            </div>
          </div>

          <div class="panel section">
            <div class="section-head">
              <h2>ملخص المشروع</h2>
              <span class="tag">مؤشرات</span>
            </div>

            <div class="metrics">
              <div class="metric">
                <span class="name">الطول</span>
                <strong id="metricLength">12 م</strong>
                <small>طول المبنى</small>
              </div>

              <div class="metric">
                <span class="name">العرض</span>
                <strong id="metricWidth">8 م</strong>
                <small>عرض المبنى</small>
              </div>

              <div class="metric">
                <span class="name">المساحة</span>
                <strong id="metricArea">96 م²</strong>
                <small>إجمالي المساحة</small>
              </div>
            </div>

            <div class="notes">
              هذه نسخة أولية تفاعلية تهدف إلى تقديم تجربة تصميم عملية وسريعة. لا تُعد هذه النسخة بديلًا عن المخطط الهندسي المعتمد.
            </div>
          </div>
        </div>
      </section>

      <section id="plan" class="screen" hidden>
        <div class="panel section">
          <div class="section-head">
            <h2>مخطط 2D</h2>
            <span class="tag">محرر الغرف</span>
          </div>

          <div class="canvas-wrap">
            <canvas id="planCanvas" width="1000" height="560"></canvas>
          </div>

          <div class="toolbar">
            <button class="accent" id="addRoom">إضافة غرفة</button>
            <button id="deleteRoom">حذف الغرفة</button>
            <button id="resetPlan">إعادة الترتيب</button>
            <button id="saveLocal">حفظ المشروع</button>
            <button id="loadLocal">استعادة</button>
            <button id="exportPlan">تصدير PNG</button>
          </div>

          <div class="room-list" id="roomList"></div>
        </div>
      </section>

      <section id="view" class="screen" hidden>
        <div class="panel section">
          <div class="section-head">
            <h2>العرض الثلاثي الأبعاد</h2>
            <span class="tag">منظور مبسط</span>
          </div>

          <div class="canvas-wrap">
            <canvas id="viewCanvas" width="1000" height="560"></canvas>
          </div>

          <div class="toolbar">
            <button id="rotateLeft">تدوير يسار</button>
            <button id="rotateRight">تدوير يمين</button>
            <button class="accent" id="refresh3d">تحديث المشهد</button>
          </div>
        </div>
      </section>

      <section id="calc" class="screen" hidden>
        <div class="panel section">
          <div class="section-head">
            <h2>حسابات المشروع</h2>
            <span class="tag">تقدير أولي</span>
          </div>

          <div class="form-grid">
            <div class="field">
              <label for="length">طول المبنى (متر)</label>
              <input id="length" type="number" min="0" step="0.1" value="12" />
            </div>

            <div class="field">
              <label for="width">عرض المبنى (متر)</label>
              <input id="width" type="number" min="0" step="0.1" value="8" />
            </div>

            <div class="field">
              <label for="rate">السعر للمتر المربع</label>
              <input id="rate" type="number" min="0" step="1" value="1200" />
            </div>

            <div class="field">
              <label for="kind">نوع المشروع</label>
              <select id="kind">
                <option>سكني</option>
                <option>تجاري</option>
                <option>مكتب هندسي</option>
                <option>تصميم داخلي</option>
                <option>مستودع</option>
              </select>
            </div>
          </div>

          <div class="metrics">
            <div class="metric">
              <span class="name">المساحة</span>
              <strong id="area">96</strong>
              <small>م²</small>
            </div>

            <div class="metric">
              <span class="name">التكلفة</span>
              <strong id="cost">115,200</strong>
              <small>تقدير أولي</small>
            </div>

            <div class="metric">
              <span class="name">نوع المشروع</span>
              <strong id="projectTypeLabel">سكني</strong>
              <small>تصنيف</small>
            </div>
          </div>
          
          <div class="toolbar">
            <button class="accent" id="exportProject">تصدير بيانات المشروع</button>
          </div>
        </div>
      </section>

      <section id="report" class="screen" hidden>
        <div class="panel section">
          <div class="section-head">
            <h2>التقارير</h2>
            <span class="tag">ملخص التنفيذ</span>
          </div>

          <div class="notes">
            المشروع الحالي يحتوي على <strong id="reportRoomCount">3</strong> غرف، بمساحة إجمالية قدرها <strong id="reportArea">96 م²</strong>، وتكلفة تقديرية <strong id="reportCost">115,200</strong>.
            <br><br>
            يتم حفظ البيانات محليًا داخل المتصفح، ويمكن تصديرها في أي وقت بصيغة JSON أو صورة PNG.
          </div>
        </div>
      </section>
    </main>
  </div>

  <script>
    const $ = id => document.getElementById(id);

    let rooms = [
      { x: 90, y: 90, w: 250, h: 140, name: "غرفة معيشة" },
      { x: 360, y: 90, w: 200, h: 140, name: "غرفة نوم" },
      { x: 90, y: 250, w: 210, h: 150, name: "مطبخ" }
    ];

    let selected = 0;
    let drag = null;
    let angle = 0;

    function updateRoomList() {
      const list = $('roomList');
      list.innerHTML = '';

      rooms.forEach((room, index) => {
        const item = document.createElement('div');
        item.className = 'room-item' + (index === selected ? ' active' : '');
        item.innerHTML = `
          <div class="room-info">
            <span class="room-swatch" style="background:${index % 2 === 0 ? '#4fe1ff' : '#f0bf66'}"></span>
            <div>
              <div class="room-name">${room.name}</div>
              <div class="room-meta">${Math.round(room.w / 20)} × ${Math.round(room.h / 20)} م</div>
            </div>
          </div>
          <div class="room-actions">
            <button class="mini" data-index="${index}" data-action="select">تحديد</button>
            <button class="mini danger" data-index="${index}" data-action="delete">حذف</button>
          </div>
        `;

        item.querySelector('[data-action="select"]').addEventListener('click', () => {
          selected = index;
          updateRoomList();
          drawPlan();
        });

        item.querySelector('[data-action="delete"]').addEventListener('click', () => {
          if (rooms.length <= 1) {
            alert('يجب أن تبقى غرفة واحدة على الأقل في المشروع.');
            return;
          }
          rooms.splice(index, 1);
          selected = Math.max(0, rooms.length - 1);
          updateRoomList();
          drawPlan();
          refreshSummary();
        });

        list.appendChild(item);
      });
    }

    function openTab(tab) {
      document.querySelectorAll('.screen').forEach(s => s.hidden = s.id !== tab);
      document.querySelectorAll('nav button').forEach(b => b.classList.toggle('active', b.dataset.tab === tab));
      if (tab === 'plan') drawPlan();
      if (tab === 'view') draw3D();
      if (tab === 'calc') calculateProject();
      if (tab === 'report') refreshSummary();
    }

    document.querySelectorAll('[data-tab]').forEach(btn => {
      btn.addEventListener('click', () => openTab(btn.dataset.tab));
    });

    document.querySelectorAll('[data-go]').forEach(btn => {
      btn.addEventListener('click', () => openTab(btn.dataset.go));
    });

    function drawPlan() {
      const canvas = $('planCanvas');
      const ctx = canvas.getContext('2d');
      ctx.clearRect(0, 0, canvas.width, canvas.height);

      ctx.fillStyle = '#091823';
      ctx.fillRect(0, 0, canvas.width, canvas.height);

      ctx.strokeStyle = 'rgba(158,243,255,0.08)';
      ctx.lineWidth = 1;

      for (let x = 0; x < canvas.width; x += 30) {
        ctx.beginPath();
        ctx.moveTo(x, 0);
        ctx.lineTo(x, canvas.height);
        ctx.stroke();
      }
      for (let y = 0; y < canvas.height; y += 30) {
        ctx.beginPath();
        ctx.moveTo(0, y);
        ctx.lineTo(canvas.width, y);
        ctx.stroke();
      }

      rooms.forEach((room, i) => {
        ctx.fillStyle = i === selected ? '#1c5971' : '#123548';
        ctx.strokeStyle = i === selected ? '#4fe1ff' : '#88b9d0';
        ctx.lineWidth = i === selected ? 4 : 2;

        ctx.fillRect(room.x, room.y, room.w, room.h);
        ctx.strokeRect(room.x, room.y, room.w, room.h);

        ctx.fillStyle = '#ebf7ff';
        ctx.font = '700 18px Segoe UI';
        ctx.fillText(room.name, room.x + 16, room.y + 28);

        ctx.font = '600 13px Segoe UI';
        ctx.fillStyle = '#bfeaf8';
        ctx.fillText(`${Math.round(room.w / 20)} × ${Math.round(room.h / 20)} م`, room.x + 16, room.y + 52);
      });

      ctx.fillStyle = '#4fe1ff';
      ctx.font = '700 16px Segoe UI';
      ctx.fillText('مخطط تصميم أولي', 20, canvas.height - 20);
    }

    function canvasPoint(evt, canvas) {
      const rect = canvas.getBoundingClientRect();
      return {
        x: ((evt.clientX - rect.left) / rect.width) * canvas.width,
        y: ((evt.clientY - rect.top) / rect.height) * canvas.height
      };
    }

    const planCanvas = $('planCanvas');

    planCanvas.addEventListener('pointerdown', e => {
      const p = canvasPoint(e, planCanvas);
      const idx = rooms.findIndex(room =>
        p.x >= room.x && p.x <= room.x + room.w &&
        p.y >= room.y && p.y <= room.y + room.h
      );

      if (idx >= 0) {
        selected = idx;
        drag = { x: p.x - rooms[idx].x, y: p.y - rooms[idx].y };
        updateRoomList();
        drawPlan();
      }
    });

    planCanvas.addEventListener('pointermove', e => {
      if (!drag) return;
      const p = canvasPoint(e, planCanvas);
      const room = rooms[selected];
      room.x = Math.max(20, Math.min(planCanvas.width - room.w - 20, p.x - drag.x));
      room.y = Math.max(20, Math.min(planCanvas.height - room.h - 20, p.y - drag.y));
      drawPlan();
      refreshSummary();
    });

    planCanvas.addEventListener('pointerup', () => drag = null);
    planCanvas.addEventListener('pointerleave', () => drag = null);

    function addRoom() {
      const names = ['غرفة نوم', 'مكتب', 'غرفة ضيوف', 'حمام', 'غرفة استقبال', 'مكتبة'];
      const name = names[rooms.length % names.length];
      rooms.push({
        x: 80 + (rooms.length % 3) * 130,
        y: 80 + (rooms.length % 2) * 120,
        w: 150,
        h: 110,
        name
      });
      selected = rooms.length - 1;
      updateRoomList();
      drawPlan();
      refreshSummary();
    }

    function deleteSelectedRoom() {
      if (rooms.length <= 1) {
        alert('يجب أن يبقى غرفة واحدة على الأقل في المشروع.');
        return;
      }
      rooms.splice(selected, 1);
      selected = Math.max(0, selected - 1);
      updateRoomList();
      drawPlan();
      refreshSummary();
    }

    function resetPlan() {
      rooms = [
        { x: 90, y: 90, w: 250, h: 140, name: 'غرفة معيشة' },
        { x: 360, y: 90, w: 200, h: 140, name: 'غرفة نوم' },
        { x: 90, y: 250, w: 210, h: 150, name: 'مطبخ' }
      ];
      selected = 0;
      updateRoomList();
      drawPlan();
      refreshSummary();
    }

    function calculateProject() {
      const length = Number($('length').value) || 0;
      const width = Number($('width').value) || 0;
      const rate = Number($('rate').value) || 0;
      const area = length * width;
      const cost = area * rate;

      $('area').textContent = area.toLocaleString('en-US', { maximumFractionDigits: 2 });
      $('cost').textContent = cost.toLocaleString('en-US', { maximumFractionDigits: 2 });
      $('projectTypeLabel').textContent = $('kind').value;

      $('metricLength').textContent = `${length} م`;
      $('metricWidth').textContent = `${width} م`;
      $('metricArea').textContent = `${area.toLocaleString('en-US')} م²`;

      $('totalAreaLabel').textContent = `${area.toLocaleString('en-US')} م²`;
      $('totalCostLabel').textContent = cost.toLocaleString('en-US');
      $('roomCountLabel').textContent = rooms.length;

      $('reportRoomCount').textContent = rooms.length;
      $('reportArea').textContent = `${area.toLocaleString('en-US')} م²`;
      $('reportCost').textContent = cost.toLocaleString('en-US');
    }

    function refreshSummary() {
      const length = Number($('length').value) || 0;
      const width = Number($('width').value) || 0;
      const rate = Number($('rate').value) || 0;
      const area = length * width;
      const cost = area * rate;

      $('totalAreaLabel').textContent = `${area.toLocaleString('en-US')} م²`;
      $('totalCostLabel').textContent = cost.toLocaleString('en-US');
      $('roomCountLabel').textContent = rooms.length;
      $('reportRoomCount').textContent = rooms.length;
      $('reportArea').textContent = `${area.toLocaleString('en-US')} م²`;
      $('reportCost').textContent = cost.toLocaleString('en-US');
    }

    function saveLocal() {
      const data = {
        projectType: $('kind').value,
        length: $('length').value,
        width: $('width').value,
        rate: $('rate').value,
        rooms
      };
      localStorage.setItem('timex-engineer-project', JSON.stringify(data));
      alert('تم حفظ المشروع محليًا بنجاح.');
    }

    function loadLocal() {
      const raw = localStorage.getItem('timex-engineer-project');
      if (!raw) {
        alert('لا يوجد مشروع محفوظ.');
        return;
      }

      try {
        const data = JSON.parse(raw);
        if (data.length) $('length').value = data.length;
        if (data.width) $('width').value = data.width;
        if (data.rate) $('rate').value = data.rate;
        if (data.projectType) $('kind').value = data.projectType;
        if (Array.isArray(data.rooms) && data.rooms.length) rooms = data.rooms;

        selected = 0;
        updateRoomList();
        drawPlan();
        calculateProject();
        alert('تم استعادة المشروع المحفوظ.');
      } catch {
        alert('تعذر قراءة الملف المحفوظ.');
      }
    }

    function exportPlan() {
      const canvas = $('planCanvas');
      canvas.toBlob(blob => {
        if (!blob) {
          alert('تعذر تصدير الصورة.');
          return;
        }
        const url = URL.createObjectURL(blob);
        const a = document.createElement('a');
        a.href = url;
        a.download = 'TIMEX-PLAN.png';
        document.body.appendChild(a);
        a.click();
        a.remove();
        URL.revokeObjectURL(url);
      }, 'image/png');
    }

    function exportProject() {
      const data = {
        app: 'TIMEX ENGINEER',
        version: '1.0.0',
        projectType: $('kind').value,
        length: Number($('length').value),
        width: Number($('width').value),
        rate: Number($('rate').value),
        area: Number($('length').value) * Number($('width').value),
        cost: Number($('length').value) * Number($('width').value) * Number($('rate').value),
        rooms,
        exportedAt: new Date().toISOString()
      };

      const blob = new Blob([JSON.stringify(data, null, 2)], { type: 'application/json' });
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url;
      a.download = 'TIMEX-PROJECT.json';
      document.body.appendChild(a);
      a.click();
      a.remove();
      URL.revokeObjectURL(url);
    }

    function draw3D() {
      const canvas = $('viewCanvas');
      const ctx = canvas.getContext('2d');
      ctx.clearRect(0, 0, canvas.width, canvas.height);

      ctx.fillStyle = '#081a27';
      ctx.fillRect(0, 0, canvas.width, canvas.height);

      const cx = canvas.width / 2;
      const cy = canvas.height / 2;

      function project(a, b, z) {
        const x = (a * Math.cos(angle) - b * Math.sin(angle)) * 26;
        const y = (a * Math.sin(angle) + b * Math.cos(angle)) * 14 - z * 26;
        return { x: cx + x, y: cy + y };
      }

      const prism = [
        [0,0,0],[14,0,0],[14,8,0],[0,8,0],
        [0,0,3],[14,0,3],[14,8,3],[0,8,3]
      ];

      const points = prism.map(([x,y,z]) => project(x,y,z));

      const edges = [
        [0,1],[1,2],[2,3],[3,0],
        [4,5],[5,6],[6,7],[7,4],
        [0,4],[1,5],[2,6],[3,7]
      ];

      ctx.strokeStyle = '#7bcbe7';
      ctx.lineWidth = 2;
      edges.forEach(([a,b]) => {
        ctx.beginPath();
        ctx.moveTo(points[a].x, points[a].y);
        ctx.lineTo(points[b].x, points[b].y);
        ctx.stroke();
      });

      ctx.fillStyle = 'rgba(79,225,255,0.12)';
      ctx.beginPath();
      ctx.moveTo(points[0].x, points[0].y);
      ctx.lineTo(points[1].x, points[1].y);
      ctx.lineTo(points[2].x, points[2].y);
      ctx.lineTo(points[3].x, points[3].y);
      ctx.closePath();
      ctx.fill();

      ctx.fillStyle = 'rgba(240,191,102,0.18)';
      ctx.beginPath();
      ctx.moveTo(points[4].x, points[4].y);
      ctx.lineTo(points[5].x, points[5].y);
      ctx.lineTo(points[6].x, points[6].y);
      ctx.lineTo(points[7].x, points[7].y);
      ctx.closePath();
      ctx.fill();

      ctx.fillStyle = '#ebf7ff';
      ctx.font = '700 18px Segoe UI';
      ctx.fillText('إظهار هندسي مبسط', 26, 34);
    }

    document.getElementById('addRoom').addEventListener('click', addRoom);
    document.getElementById('deleteRoom').addEventListener('click', deleteSelectedRoom);
    document.getElementById('resetPlan').addEventListener('click', resetPlan);
    document.getElementById('saveLocal').addEventListener('click', saveLocal);
    document.getElementById('loadLocal').addEventListener('click', loadLocal);
    document.getElementById('exportPlan').addEventListener('click', exportPlan);
    document.getElementById('exportProject').addEventListener('click', exportProject);

    document.getElementById('length').addEventListener('input', calculateProject);
    document.getElementById('width').addEventListener('input', calculateProject);
    document.getElementById('rate').addEventListener('input', calculateProject);
    document.getElementById('kind').addEventListener('change', calculateProject);

    document.getElementById('rotateLeft').addEventListener('click', () => {
      angle -= 0.18;
      draw3D();
    });

    document.getElementById('rotateRight').addEventListener('click', () => {
      angle += 0.18;
      draw3D();
    });

    document.getElementById('refresh3d').addEventListener('click', draw3D);

    updateRoomList();
    drawPlan();
    draw3D();
    calculateProject();
  </script>
</body>
</html># Timex-Applications-Industries-