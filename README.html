<!doctype html>
<html lang="es">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Misión 3 — Mini-juegos: Detener Erupción Volcánica</title>
<style>
  :root{--bg:#08121a;--panel:#0f1b22;--accent:#ff7a3d;--safe:#3dd6b8;--danger:#ff6b6b;--muted:#9fb3bd}
  html,body{height:100%;margin:0;font-family:Inter,system-ui,Arial,sans-serif;background:linear-gradient(180deg,#07121a 0%, #0d1620 100%);color:#eaf6f4}
  .wrap{max-width:1100px;margin:22px auto;padding:18px}
  header{display:flex;align-items:center;gap:12px}
  h1{margin:0;font-size:20px}
  .subtitle{color:var(--muted);font-size:13px}
  .grid{display:grid;grid-template-columns:1fr 420px;gap:18px;margin-top:16px}
  .panel{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));padding:14px;border-radius:12px;box-shadow:0 8px 24px rgba(0,0,0,0.6)}
  .game{margin-bottom:12px}
  .row{display:flex;gap:8px}
  button{cursor:pointer;border:0;padding:10px 12px;border-radius:8px;background:rgba(255,255,255,0.03);color:inherit}
  .btn-primary{background:var(--accent);color:#102020}
  .small{font-size:13px;color:var(--muted)}
  canvas{display:block;border-radius:8px;background:linear-gradient(180deg,#071a13,#071a1a);width:100%}
  .valves{display:grid;grid-template-columns:repeat(4,1fr);gap:8px}
  .valve{height:56px;border-radius:8px;font-weight:700}
  .score{font-size:18px;font-weight:700}
  .route-buttons button{width:100%;padding:12px}
  input[type=range]{width:100%}
  .meter{height:18px;background:rgba(255,255,255,0.04);border-radius:999px;overflow:hidden}
  .meter > i{display:block;height:100%;width:0%}
  .status{padding:8px;border-radius:8px;background:rgba(255,255,255,0.02);font-size:13px}
  footer{margin-top:12px;color:var(--muted);font-size:13px}
  .hint{color:var(--muted);font-size:13px;margin-top:6px}
  .big-center{display:flex;align-items:center;justify-content:center;gap:12px}
</style>
</head>
<body>
<div class="wrap">
  <header>
    <div>
      <h1>🌋 Misión 3 — Mini-juegos (Volcán)</h1>
      <div class="subtitle">Solo mini-juegos: 4 pruebas rápidas, juega cada una y suma puntos.</div>
    </div>
    <div style="margin-left:auto;text-align:right">
      <div class="score" id="total-score">Puntuación: 0</div>
      <div class="small">Minijuegos independientes — sin pasos</div>
    </div>
  </header>

  <div class="grid">
    <!-- columna izquierda: juegos -->
    <div>
      <!-- Juego 1: Sismógrafo: detecta picos -->
      <section class="panel game">
        <h3 style="margin:0 0 8px 0">1) Sismógrafo — Detecta el pico</h3>
        <div class="small">Observa la onda. Haz click en <strong>Detectar</strong> cuando veas un pico grande.</div>
        <div style="margin-top:10px">
          <canvas id="sg-canvas" width="720" height="120"></canvas>
        </div>
        <div class="row" style="margin-top:8px;align-items:center">
          <button id="sg-detect" class="btn-primary">Detectar</button>
          <div class="small" id="sg-msg">Listo</div>
        </div>
        <div class="hint">Éxito: captura un pico mayor que el umbral. Reintentos ilimitados.</div>
      </section>

      <!-- Juego 2: Válvulas (Simon) -->
      <section class="panel game">
        <h3 style="margin:0 0 8px 0">2) Válvulas — Repite la secuencia</h3>
        <div class="small">Pulsa <strong>Mostrar</strong> para ver la secuencia. Luego repítela.</div>
        <div style="margin-top:10px" class="valves" id="valves">
          <button class="valve" data-id="0" style="background:#ff8b66">A</button>
          <button class="valve" data-id="1" style="background:#ffd166">B</button>
          <button class="valve" data-id="2" style="background:#06d6a0">C</button>
          <button class="valve" data-id="3" style="background:#4d96ff">D</button>
        </div>
        <div class="row" style="margin-top:8px">
          <button id="val-show" class="btn">Mostrar</button>
          <button id="val-reset" class="btn">Reiniciar</button>
          <div class="small" id="val-msg">Esperando</div>
        </div>
        <div class="hint">Acumula puntos por secuencias largas y sin errores.</div>
      </section>

      <!-- Juego 3: Rutas (elección rápida) -->
      <section class="panel game">
        <h3 style="margin:0 0 8px 0">3) Redirigir flujo — Elige la ruta segura</h3>
        <div class="small">Aparecen 3 rutas. Selecciona la más segura antes de que acabe el contador.</div>
        <div style="margin-top:10px" class="route-buttons">
          <div class="row">
            <button class="btn" data-route="ciudad">Ruta — Ciudad</button>
            <button class="btn" data-route="valle">Ruta — Valle</button>
            <button class="btn" data-route="ocean">Ruta — Océano</button>
          </div>
        </div>
        <div class="row" style="margin-top:8px;align-items:center">
          <div class="meter" style="flex:1"><i id="route-meter" style="width:0%;background:linear-gradient(90deg,#ffd166,#ff8b66);"></i></div>
          <button id="route-start" class="btn">Empezar</button>
        </div>
        <div class="small" id="route-msg">Pulsa "Empezar" para generar la ruta segura</div>
      </section>

      <!-- Juego 4: Enfriamiento (equilibrio) -->
      <section class="panel game">
        <h3 style="margin:0 0 8px 0">4) Enfriar cámara — Mantén el balance</h3>
        <div class="small">Mueve el slider al rango verde (30–70) y mantenlo estable 4 segundos mientras la temperatura fluctúa.</div>
        <div style="margin-top:10px">
          <input id="cool-slider" type="range" min="0" max="100" value="50">
          <div class="meter" style="margin-top:8px"><i id="cool-meter" style="width:50%;background:linear-gradient(90deg,#3dd6b8,#06d6a0)"></i></div>
        </div>
        <div class="row" style="margin-top:8px;align-items:center">
          <button id="cool-start" class="btn">Iniciar</button>
          <div class="small" id="cool-msg">Esperando</div>
        </div>
        <div class="hint">Si el slider sale del rango por demasiado tiempo, pierdes el intento.</div>
      </section>
    </div>

    <!-- columna derecha: panel de resultados -->
    <aside>
      <div class="panel">
        <h3 style="margin:0 0 8px 0">Panel de resultados</h3>
        <div class="small">Puntuación por juego (variable):</div>
        <ul class="small" style="margin-top:10px">
          <li>Sismógrafo: <span id="score-sg">0</span></li>
          <li>Válvulas: <span id="score-val">0</span></li>
          <li>Rutas: <span id="score-route">0</span></li>
          <li>Enfriamiento: <span id="score-cool">0</span></li>
        </ul>
        <div style="margin-top:12px">
          <button id="reset-all" class="btn">Reiniciar todo</button>
          <button id="export-log" class="btn">Exportar reporte (simulado)</button>
        </div>
        <div class="hint" style="margin-top:10px">Registro de eventos:</div>
        <div id="log" class="small" style="height:240px;overflow:auto;margin-top:8px;background:rgba(0,0,0,0.12);padding:8px;border-radius:8px">--</div>
      </div>
    </aside>
  </div>

  <footer>Prototipo de minijuegos — dime si quieres que los convierta en una sola secuencia o que aumente dificultad.</footer>
</div>

<script>
/* ----------------- helpers ----------------- */
function log(msg){ const el = document.getElementById('log'); el.innerText = `[${new Date().toLocaleTimeString()}] ${msg}\n` + el.innerText; }
function addScore(key, pts){ const el = document.getElementById('total-score'); const cur = Number(el.dataset.val || 0); const n = cur + pts; el.dataset.val = n; el.innerText = 'Puntuación: ' + n; document.getElementById('score-'+key).innerText = Number(document.getElementById('score-'+key).innerText) + pts; }

/* ------------- Juego 1: Sismógrafo ------------- */
(function(){
  const c = document.getElementById('sg-canvas'); const ctx = c.getContext('2d');
  const W = c.width = c.clientWidth; const H = c.height = 120;
  let t = 0; let spikeTimes = [];
  // generate random spikes schedule
  function scheduleSpikes(){ spikeTimes = []; let now = 0; for(let i=0;i<6;i++){ now += 30 + Math.floor(Math.random()*70); spikeTimes.push(now); } }
  scheduleSpikes();
  // draw
  function frame(){ ctx.clearRect(0,0,W,H);
    // baseline
    ctx.fillStyle = 'rgba(255,255,255,0.02)'; ctx.fillRect(0,0,W,H);
    ctx.strokeStyle = 'rgba(61,214,184,0.9)'; ctx.lineWidth = 2; ctx.beginPath();
    for(let x=0;x<W;x++){
      const time = t + x;
      // base noise
      let v = Math.sin((time)*0.02)*6 + Math.cos((time)*0.01)*3;
      // spikes
      let spike = 0;
      for(const s of spikeTimes){ const d = Math.abs(time - s); if(d < 24) spike += Math.exp(-d/6)*40; }
      v += spike;
      const y = H/2 - v;
      if(x===0) ctx.moveTo(x,y); else ctx.lineTo(x,y);
    }
    ctx.stroke();
    t += 1;
    requestAnimationFrame(frame);
  }
  frame();

  // detection: check if current viewport contains a spike > threshold
  const detectBtn = document.getElementById('sg-detect'); const msg = document.getElementById('sg-msg');
  detectBtn.addEventListener('click', ()=>{
    // we consider 'detected' if there is a spike within the next 40 px (approx)
    const currentTime = t + W - 60; // near right edge
    // check spikeTimes for any within [currentTime-40, currentTime+40]
    const found = spikeTimes.some(s => Math.abs(s - currentTime) < 40);
    if(found){ msg.innerText = '✅ Pico detectado'; addScore('sg', 20); log('Sismógrafo: pico detectado — +20');
      // remove nearest spike
      let minIdx = -1; let minD = 1e9; spikeTimes.forEach((s,i)=>{ const d = Math.abs(s-currentTime); if(d<minD){minD=d;minIdx=i;} }); if(minIdx>=0) spikeTimes.splice(minIdx,1);
    } else { msg.innerText = '❌ No había pico'; addScore('sg', -5); log('Sismógrafo: intento fallido — -5'); }
  });
})();

/* ------------- Juego 2: Válvulas (Simon) ------------- */
(function(){
  const showBtn = document.getElementById('val-show'); const resetBtn = document.getElementById('val-reset'); const msg = document.getElementById('val-msg');
  const valves = Array.from(document.querySelectorAll('.valve'));
  let sequence = []; let input = []; let playing = false; let allowInput = false;

  function randInt(n){ return Math.floor(Math.random()*n); }
  function genSequence(len){ sequence = []; for(let i=0;i<len;i++) sequence.push(randInt(valves.length)); }
  function flash(index){ const v = valves[index]; const prev = v.style.boxShadow; v.style.transform='scale(0.98)'; v.style.boxShadow='0 8px 18px rgba(0,0,0,0.4) inset'; setTimeout(()=>{ v.style.transform=''; v.style.boxShadow=prev; },350); }

  function playSequence(){ allowInput=false; msg.innerText='Mostrando secuencia...'; let i=0; (function next(){ if(i>=sequence.length){ allowInput=true; msg.innerText='Tu turno'; return;} flash(sequence[i]); i++; setTimeout(next,700); })(); }

  showBtn.addEventListener('click', ()=>{
    genSequence(3 + Math.floor(Math.random()*4)); input = []; addScore('val', 0); playing=true; playSequence(); log('Válvulas: secuencia generada (len='+sequence.length+')');
  });
  resetBtn.addEventListener('click', ()=>{ sequence=[]; input=[]; allowInput=false; msg.innerText='Reiniciado'; log('Válvulas: reiniciado'); });

  valves.forEach((btn,i)=>{ btn.addEventListener('click', ()=>{
    if(!allowInput) return; flash(i);
    input.push(i);
    // check prefix
    for(let k=0;k<input.length;k++){ if(input[k] !== sequence[k]){ // fail
      allowInput=false; msg.innerText='❌ Secuencia incorrecta'; addScore('val', -10); log('Válvulas: error en la secuencia — -10'); input=[]; setTimeout(()=>{ playSequence(); },900); return; } }
    // success
    if(input.length === sequence.length){ allowInput=false; msg.innerText='✅ Secuencia correcta'; const pts = 10 + (sequence.length-3)*5; addScore('val', pts); log('Válvulas: secuencia completada — +'+pts); input=[]; setTimeout(()=>{ genSequence(sequence.length+1); playSequence(); },900); }
  }); });
})();

/* ------------- Juego 3: Rutas ------------- */
(function(){
  const startBtn = document.getElementById('route-start'); const meter = document.getElementById('route-meter'); const msg = document.getElementById('route-msg');
  const buttons = Array.from(document.querySelectorAll('[data-route]'));
  let safeRoute = null; let countdown = null; let pct = 0;

  function startRound(){ // choose safe route randomly
    safeRoute = ['ciudad','valle','ocean'][Math.floor(Math.random()*3)]; pct = 0; meter.style.width = '0%'; msg.innerText = 'Selecciona la ruta segura';
    // animate meter for 5s
    const start = Date.now(); countdown = setInterval(()=>{
      const elapsed = Date.now() - start; pct = Math.min(100, (elapsed/5000)*100); meter.style.width = pct+'%';
      if(pct>=100){ clearInterval(countdown); msg.innerText = 'Tiempo agotado'; addScore('route', -10); log('Rutas: tiempo agotado — -10'); }
    },80);
  }

  startBtn.addEventListener('click', ()=>{ startRound(); log('Rutas: ronda iniciada'); });
  buttons.forEach(b=>{ b.addEventListener('click', ()=>{
    if(pct>=100){ msg.innerText='Ya no puedes elegir'; return; }
    clearInterval(countdown);
    const chosen = b.dataset.route;
    if(chosen === safeRoute){ msg.innerText='✅ Ruta segura elegida'; addScore('route', 15); log('Rutas: elección segura — +15 ('+chosen+')'); }
    else { msg.innerText='❌ Ruta insegura — impacto'; addScore('route', -8); log('Rutas: elección insegura — -8 ('+chosen+')'); }
    pct = 100; meter.style.width = '100%';
  }); });
})();

/* ------------- Juego 4: Enfriamiento ------------- */
(function(){
  const slider = document.getElementById('cool-slider'); const startBtn = document.getElementById('cool-start'); const msg = document.getElementById('cool-msg'); const meter = document.getElementById('cool-meter');
  let running = false; let stableTime = 0; let interval = null;
  function stopRun(success){ running=false; clearInterval(interval); if(success){ addScore('cool', 20); msg.innerText='✅ Estable durante 4s — +20'; log('Enfriamiento: éxito — +20'); } else { addScore('cool', -7); msg.innerText='❌ Fallaste'; log('Enfriamiento: fallido — -7'); } }
  startBtn.addEventListener('click', ()=>{
    if(running) return; running=true; stableTime=0; msg.innerText='Mantén en 30–70% por 4s'; interval = setInterval(()=>{
      // simulate small disturbance by moving target slightly
      const targetDrift = Math.sin(Date.now()/600)*6; // visual wobble
      const val = Number(slider.value) + targetDrift*0.1;
      meter.style.width = (slider.value)+'%';
      // check range
      if(slider.value >=30 && slider.value <=70){ stableTime += 0.2; } else { stableTime = Math.max(0, stableTime - 0.6); }
      if(stableTime >= 4){ stopRun(true); }
    },200);
  });
})();

/* ------------- panel controls ------------- */
document.getElementById('reset-all').addEventListener('click', ()=>{ location.reload(); });
document.getElementById('export-log').addEventListener('click', ()=>{ alert('Reporte simulado:\n'+document.getElementById('log').innerText.slice(0,200)); });

</script>
</body>
</html>
