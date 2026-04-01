<!doctype html>
<html lang="ko">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>모찌서버 법률 계산기</title>
  <style>
    :root {
      --bg: #f8f9fa; --panel: rgba(255, 255, 255, 0.9); --card: #ffffff; --accent: #d4a373; 
      --text: #2d2d2d; --muted: #7d7d7d; --border: #ececec; --danger: #ff4d4d; --success: #27ae60;
      --shadow: 0 4px 20px rgba(0,0,0,0.05);
    }
    [data-theme="dark"] {
      --bg: #0a0a0a; --panel: rgba(15, 15, 15, 0.85); --card: #161616; --accent: #ffffff;
      --text: #e0e0e0; --muted: #888888; --border: #262626; --danger: #ff5e5e; --success: #2ecc71;
      --shadow: 0 4px 20px rgba(0,0,0,0.4);
    }

    * { box-sizing: border-box; -webkit-font-smoothing: antialiased; }
    body { 
      margin: 0; font-family: "Pretendard Variable", -apple-system, sans-serif; 
      background: var(--bg); color: var(--text); display: flex; flex-direction: column; 
      height: 100vh; overflow: hidden; transition: 0.3s;
    }
    
    header { 
      padding: 0 2rem; height: 55px; border-bottom: 1px solid var(--border); 
      display: flex; justify-content: space-between; align-items: center; 
      background: var(--panel); backdrop-filter: blur(10px); z-index: 100; flex-shrink: 0;
    }
    .logo-group h1 { margin: 0; font-size: 1.1rem; font-weight: 900; letter-spacing: -0.5px; }
    .logo-group span { color: var(--accent); }

    .main-container { flex: 1; display: flex; overflow: hidden; }
    
    .left-section { flex: 1; display: flex; flex-direction: column; padding: 1.2rem 2rem; overflow: hidden; }
    .nav-bar { display: flex; justify-content: space-between; align-items: center; margin-bottom: 1.5rem; gap: 1rem; }
    .tabs { display: flex; gap: 6px; overflow-x: auto; scrollbar-width: none; }
    .tab { 
      padding: 8px 14px; border-radius: 8px; border: 1px solid var(--border); 
      background: var(--card); color: var(--muted); cursor: pointer; 
      font-size: 0.8rem; font-weight: 700; white-space: nowrap; transition: 0.2s;
    }
    .tab.active { background: var(--accent); color: #000; border-color: var(--accent); }
    
    .search-bar { width: 220px; }
    .search-bar input { 
      width: 100%; padding: 8px 12px; border-radius: 8px; border: 1px solid var(--border); 
      background: var(--card); color: var(--text); outline: none; font-size: 0.85rem;
    }

    .item-grid { 
      flex: 1; overflow-y: auto; display: grid; 
      grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); 
      gap: 16px; align-content: start; padding-top: 5px;
    }
    .item-card { 
      background: var(--card); border: 1px solid var(--border); border-radius: 12px; 
      padding: 16px; cursor: pointer; position: relative; transition: 0.2s;
    }
    .item-card:hover { transform: translateY(-3px); box-shadow: var(--shadow); border-color: var(--accent); }
    .item-card.selected { border-color: var(--accent); background: var(--panel); box-shadow: 0 0 0 1px var(--accent); }
    .item-card .name { font-size: 0.9rem; font-weight: 800; margin-bottom: 4px; }
    .item-card .price { font-size: 0.8rem; color: var(--muted); font-weight: 600; }
    .item-card .etc { font-size: 0.7rem; color: var(--accent); margin-top: 8px; opacity: 0.8; font-weight: 600; }
    .qty-badge { 
      position: absolute; top: 12px; right: 12px; background: var(--accent); 
      color: #000; font-size: 0.7rem; font-weight: 900; padding: 2px 8px; border-radius: 5px; 
    }

    .right-section { 
      width: 22vw; min-width: 320px; max-width: 400px; 
      background: var(--panel); backdrop-filter: blur(20px); 
      padding: 1.5rem; display: flex; flex-direction: column; gap: 1rem; 
      overflow-y: auto; border-left: 1px solid var(--border);
    }
    .res-card { background: var(--card); border: 1px solid var(--border); padding: 16px; border-radius: 14px; box-shadow: var(--shadow); }
    .res-label { font-size: 0.7rem; color: var(--muted); font-weight: 800; margin-bottom: 5px; }
    .res-val { font-size: 1.5rem; font-weight: 900; color: var(--accent); }
    .res-ko { font-size: 0.8rem; color: var(--muted); margin-top: 4px; }

    .calc-list { flex: 1; border-top: 1px solid var(--border); padding-top: 1rem; overflow-y: auto; }
    .calc-item { display: flex; justify-content: space-between; margin-bottom: 8px; font-size: 0.8rem; font-weight: 600; }

    .btn-group { display: flex; flex-direction: column; gap: 8px; }
    .btn { padding: 12px; border-radius: 10px; font-size: 0.85rem; font-weight: 800; border: none; cursor: pointer; transition: 0.2s; }
    .btn-copy { background: var(--accent); color: #000; }
    .btn-convert { background: var(--text); color: var(--bg); }
    .btn-reset { background: transparent; color: var(--danger); border: 1px solid var(--danger); padding: 8px; }

    .overlay { position: fixed; inset: 0; background: rgba(0,0,0,0.5); backdrop-filter: blur(4px); display: none; justify-content: center; align-items: center; z-index: 9999; }
    .modal { background: var(--card); padding: 2rem; border-radius: 20px; width: 350px; box-shadow: var(--shadow); border: 1px solid var(--border); }
    .modal h2 { font-size: 1rem; margin-bottom: 1.2rem; text-align: center; }
    .modal input { width: 100%; padding: 12px; background: var(--bg); border: 1px solid var(--border); color: var(--text); border-radius: 10px; margin-bottom: 10px; text-align: center; outline: none; }

    .theme-switch { position: fixed; bottom: 20px; left: 20px; z-index: 1000; display: flex; gap: 8px; }
    .t-btn { width: 38px; height: 38px; border-radius: 10px; border: 1px solid var(--border); cursor: pointer; background: var(--card); display: flex; align-items: center; justify-content: center; font-size: 16px; }

    #toast { position: fixed; top: 20px; left: 50%; transform: translateX(-50%); background: var(--text); color: var(--bg); padding: 10px 20px; border-radius: 8px; font-size: 0.8rem; font-weight: 700; visibility: hidden; opacity: 0; transition: 0.3s; z-index: 10001; }
    #toast.show { visibility: visible; opacity: 1; transform: translate(-50%, 10px); }
  </style>
</head>
<body data-theme="dark">

  <div class="theme-switch">
    <button class="t-btn" onclick="setT('dark')">🌑</button>
    <button class="t-btn" onclick="setT('light')">🍦</button>
  </div>

  <div id="infoModal" class="overlay">
    <div class="modal" onkeydown="if(event.key==='Enter') executeCopy()">
      <h2>📋 사건 보고서 작성</h2>
      <input type="text" id="modalId" placeholder="Discord Name">
      <input type="text" id="modalName" placeholder="피의자 성함">
      <input type="text" id="modalEtc" placeholder="비고 (특이사항)">
      <div style="display:flex; gap:10px; margin-top:5px;">
        <button class="btn btn-copy" style="flex:1.5" onclick="executeCopy()">복사 (Enter)</button>
        <button class="btn" style="flex:1; background:var(--border); color:var(--text)" onclick="closeModal()">취소</button>
      </div>
    </div>
  </div>

  <div id="qtyModal" class="overlay">
    <div class="modal" style="width:300px;">
      <h2 id="mTitle" style="color:var(--accent);">수량 설정</h2>
      <input type="number" id="mInput" value="1" onfocus="this.select()" onkeydown="if(event.key==='Enter') confirmQty()">
      <div style="display:flex; gap:10px;">
        <button class="btn btn-copy" style="flex:1.5" onclick="confirmQty()">확인</button>
        <button class="btn" style="flex:1; color:var(--danger); border:1px solid var(--danger); background:transparent;" onclick="removeIdx()">제거</button>
      </div>
    </div>
  </div>

  <header>
    <div class="logo-group"><h1> <span style="color: #95F44D;">MOCHI</span> <span> 법률 계산기</span></h1></div>
    <div style="font-size:0.7rem; font-weight:800; color:var(--accent);">ADMIN SYSTEM</div>
  </header>

  <div class="main-container">
    <section class="left-section">
      <div class="nav-bar">
        <div class="tabs" id="tabs"></div>
        <div class="search-bar"><input type="text" id="searchInput" placeholder="죄목 검색..." oninput="renderList()"></div>
      </div>
      <div class="item-grid" id="itemList"></div>
    </section>

    <aside class="right-section">
      <div class="res-card">
        <div class="res-label">Total Fine</div>
        <div class="res-val" id="resFine">0원</div>
        <div class="res-ko" id="resFineKo">영 원</div>
      </div>
      <div class="res-card">
        <div class="res-label">Detention</div>
        <div class="res-val" id="resTime">0분</div>
        <div id="limitWarn" style="color:var(--danger); font-size:0.7rem; font-weight:800; margin-top:5px; display:none;">⚠️ 최대 120분 초과</div>
      </div>
      
      <div class="input-row" style="display:flex; flex-direction:column; gap:5px;">
        <label style="font-size:0.7rem; font-weight:800; color:var(--muted);">보석금 감면 (1분/500만)</label>
        <input type="number" id="bailIn" value="0" oninput="update()" style="background:var(--card); border:1px solid var(--border); padding:10px; border-radius:8px; color:var(--text); font-size:1rem; font-weight:700; outline:none;">
      </div>

      <div class="calc-list" id="calcRows"></div>

      <div class="btn-group">
        <button class="btn btn-convert" onclick="convertToTime()">벌금 미납 → 구금 전환</button>
        <button class="btn btn-copy" onclick="openInfoModal()">보고서 복사</button>
        <button class="btn btn-reset" onclick="resetAll()">초기화</button>
      </div>
    </aside>
  </div>

  <div id="toast">복사되었습니다.</div>

<script>
  const DATA = {
    "경범죄": [
      { name: "소음공해", fine: 10000000, time: 0 }, { name: "불법 주정차", fine: 10000000, time: 0 },
      { name: "속도 위반", fine: 10000000, time: 0 }, { name: "신호 위반", fine: 10000000, time: 0 },
      { name: "불법 유턴", fine: 10000000, time: 0 }, { name: "역주행", fine: 10000000, time: 0 },
      { name: "인도 주행", fine: 10000000, time: 0 }, { name: "공공기물 파손", fine: 10000000, time: 0 },
      { name: "스턴트", fine: 20000000, time: 0 }, { name: "차량파손", fine: 50000000, time: 10 },
      { name: "뺑소니", fine: 100000000, time: 20 }, { name: "폭주", fine: 50000000, time: 20 },
      { name: "항공기 저공 비행", fine: 300000000, time: 60 }, { name: "보복운전", fine: 200000000, time: 30 },
      { name: "무허가 항공기", fine: 300000000, time: 60 }
    ],
    "중범죄": [
      { name: "공범죄", fine: 0, time: 0, etc: "주범과 동일" },
      { name: "난폭운전", fine: 50000000, time: 30 },
      { name: "명예훼손", fine: 20000000, time: 10 },
      { name: "폭행", fine: 100000000, time: 20 },
      { name: "불법 물건 소지", fine: 80000000, time: 20 },
      { name: "불법 총기 소지", fine: 150000000, time: 20 },
      { name: "무기 언급", fine: 100000000, time: 20 },
      { name: "증거 인멸", fine: 200000000, time: 20 },
      { name: "차량 절도", fine: 100000000, time: 30 },
      { name: "시민 살인", fine: 300000000, time: 30 }
    ],
    "공무원법": [
      { name: "공무차량 절도시도", fine: 100000000, time: 0 }, { name: "공무원 명예훼손", fine: 200000000, time: 10 },
      { name: "공무차량 파손", fine: 100000000, time: 20 }, { name: "공무원 사칭", fine: 50000000, time: 20 },
      { name: "공무집행 방해", fine: 150000000, time: 30 }, { name: "침입죄", fine: 400000000, time: 10 },
      { name: "공무원 폭행", fine: 300000000, time: 30 }, { name: "공무차량 절도", fine: 400000000, time: 30 },
      { name: "공무원 살인", fine: 400000000, time: 40 }
    ],
    "스토리RP": [
      { name: "건샵", fine: 150000000, time: 0, etc: "무기 압수" },
      { name: "닭공장 털이", fine: 350000000, time: 30, etc: "인당 / 무기 압수 / 최소 10분" },
      { name: "보석상 털이", fine: 250000000, time: 20, etc: "인당 / 무기 압수 / 최소 10분" },
      { name: "북부은행", fine: 450000000, time: 20, etc: "인당 / 무기 압수 / 최소 10분" },
      { name: "남부은행", fine: 350000000, time: 20, etc: "인당 / 무기 압수 / 최소 10분" },
      { name: "편의점 털이", fine: 80000000, time: 10, etc: "인당 / 무기 압수(경관 재량)" },
      { name: "ATM 털이", fine: 50000000, time: 10, etc: "인당 / 무기 압수(경관 재량)" },
      { name: "빈집 털이", fine: 50000000, time: 10, etc: "인당 / 무기 압수(경관 재량)" },
      { name: "납치", fine: 300000000, time: 10, etc: "인당 / 대상자 석방" },
      { name: "영장", fine: 300000000, time: 30, etc: "인당 / 불법 물건 및 무기 압수" },
      { name: "최초 수배자", fine: 600000000, time: 40, etc: "불법 물건 및 무기 압수" },
      { name: "수배 참여", fine: 200000000, time: 20, etc: "무기 압수 / 최소 10분" },
      { name: "즉흥", fine: 200000000, time: 20, etc: "무기 압수 / 최소 10분" },
      { name: "도주", fine: 0, time: 0, etc: "관련 법률 추가 적용" }
    ]
  };

  let activeTab = "경범죄", curKey = null, isFineConverted = false, isAutoReckless = false;
  const state = new Map();

  window.addEventListener('keydown', (e) => { if (e.key === "Escape") closeModal(); });

  function setT(t) { document.body.setAttribute("data-theme", t); }
  function showT(m) { const t = document.getElementById("toast"); t.textContent = m; t.classList.add("show"); setTimeout(()=>t.classList.remove("show"), 2000); }

  function renderList() {
    const $l = document.getElementById("itemList"), query = document.getElementById("searchInput").value;
    $l.innerHTML = "";
    DATA[activeTab].forEach(item => {
      if(query && !item.name.includes(query)) return;
      const key = `${activeTab}::${item.name}`;
      if(!state.has(key)) state.set(key, {checked:false, qty:0, item});
      const s = state.get(key);
      const div = document.createElement("div");
      div.className = `item-card ${s.checked?'selected':''}`;
      div.innerHTML = `<div class="name">${item.name}</div>
        <div class="price">${item.fine>0?(item.fine/10000).toLocaleString()+'만':'가변'} / ${item.time}분</div>
        ${item.etc ? `<div class="etc">${item.etc}</div>` : ''}
        ${s.checked?`<div class="qty-badge">${s.qty}</div>`:''}`;
      div.onclick = () => openQty(activeTab, item);
      $l.appendChild(div);
    });
  }

  function checkReckless() {
    const recklessKey = "중범죄::난폭운전";
    const recklessItem = DATA["중범죄"].find(i => i.name === "난폭운전");
    let lightCrimeCount = 0;
    state.forEach((v, k) => { if(k.startsWith("경범죄") && v.checked) lightCrimeCount += v.qty; });
    const s = state.get(recklessKey) || {checked:false, qty:0, item:recklessItem};
    if(lightCrimeCount >= 3) {
      if(!s.checked) {
        state.set(recklessKey, {checked:true, qty:1, item:recklessItem});
        isAutoReckless = true;
        showT("경범죄 3개 이상: 난폭운전 자동 추가");
      }
    } else {
      if(s.checked && isAutoReckless) {
        state.set(recklessKey, {checked:false, qty:0, item:recklessItem});
        isAutoReckless = false;
      }
    }
  }

  function openQty(cat, item) {
    curKey = `${cat}::${item.name}`; const s = state.get(curKey);
    if(s.checked) { 
      s.checked = false; s.qty = 0; isFineConverted = false; 
      if(curKey === "중범죄::난폭운전") isAutoReckless = false;
      checkReckless(); renderList(); update(); 
    }
    else { 
      document.getElementById("mTitle").textContent = item.name; 
      document.getElementById("qtyModal").style.display = "flex"; 
      document.getElementById("mInput").value = 1; 
      setTimeout(()=>document.getElementById("mInput").focus(), 100); 
    }
  }

  function confirmQty() { 
    const v = parseInt(document.getElementById("mInput").value); 
    if(v > 0) { 
      const s = state.get(curKey); s.checked = true; s.qty = v; isFineConverted = false; 
      if(curKey === "중범죄::난폭운전") isAutoReckless = false;
    } 
    closeModal(); checkReckless(); renderList(); update(); 
  }

  function convertToTime() {
    let bf = 0; state.forEach(s => { if(s.checked) bf += s.item.fine * s.qty; });
    if(bf === 0) { showT("전환할 벌금이 없습니다."); return; }
    isFineConverted = true; update(); showT("벌금이 구금 시간으로 전환되었습니다.");
  }

  function update() {
    let baseFine = 0, baseTime = 0, rows = "", hasPrisonTimeItem = false;
    state.forEach(s => { if(s.checked) { 
      baseFine += s.item.fine * s.qty; baseTime += s.item.time * s.qty;
      if(s.item.time > 0) hasPrisonTimeItem = true;
      rows += `<div class="calc-item"><span>${s.item.name} x${s.qty}</span><span>${(s.item.fine*s.qty/10000).toLocaleString()}만</span></div>`; 
    }});

    const bailInValue = parseInt(document.getElementById("bailIn").value)||0;
    let maxBailableTime = hasPrisonTimeItem ? Math.max(0, baseTime - 10) : baseTime;
    let actualBailTime = Math.min(bailInValue, maxBailableTime);
    let bailAddFine = actualBailTime * 5000000;
    let totalFine = baseFine + bailAddFine;
    let totalTime = Math.max(0, baseTime - actualBailTime);

    if(hasPrisonTimeItem) { rows += `<div class="calc-item" style="color:var(--danger); font-size:0.7rem; background:rgba(255,0,0,0.05); padding:5px; border-radius:5px; margin-top:5px;">최소 구금 10분 보장 적용</div>`; }
    if(isFineConverted && totalFine > 0) {
      const convTime = Math.floor(totalFine / 5000000);
      rows += `<div class="calc-item" style="color:var(--success)"><span>벌금 미납 환산 (+${convTime}분)</span><span>0원</span></div>`;
      totalTime += convTime; totalFine = 0;
    } else if(!isFineConverted && actualBailTime > 0) {
      rows += `<div class="calc-item" style="color:var(--success)"><span>보석금 감면 (-${actualBailTime}분)</span><span>+${(bailAddFine/10000).toLocaleString()}만</span></div>`;
    }

    document.getElementById("resFine").textContent = totalFine.toLocaleString() + "원";
    document.getElementById("resFineKo").textContent = numberToKo(totalFine) + " 원";
    document.getElementById("resTime").textContent = totalTime + "분";
    
    const warnMsg = document.getElementById("limitWarn");
    if(totalTime > 120 && !isFineConverted) { document.getElementById("resTime").style.color = "var(--danger)"; warnMsg.style.display = "block"; }
    else { document.getElementById("resTime").style.color = "var(--accent)"; warnMsg.style.display = "none"; }
    document.getElementById("calcRows").innerHTML = rows || '<div style="text-align:center; color:var(--muted); padding-top:20px; font-size:0.75rem;">항목을 선택해주세요.</div>';
  }

  function numberToKo(n) {
    if (n === 0) return "영";
    const big = ["", "만", "억", "조"], nums = ["", "일", "이", "삼", "사", "오", "육", "칠", "팔", "구"], units = ["", "십", "백", "천"];
    let res = "", s = n.toString();
    for (let i = 0; i < s.length; i++) {
      let num = s[s.length - 1 - i], l = i % 4, bl = Math.floor(i / 4);
      if (num !== "0") {
        let c = nums[parseInt(num)] + units[l]; if (l === 0 && bl > 0) c += big[bl]; res = c + " " + res;
      } else if (l === 0 && bl > 0 && s.slice(Math.max(0, s.length-i-4), s.length-i).search(/[1-9]/) > -1) res = big[bl] + " " + res;
    }
    return res.trim();
  }

  function renderTabs() { 
    const $t = document.getElementById("tabs"); $t.innerHTML = "";
    Object.keys(DATA).forEach(c => {
      const btn = document.createElement("button"); btn.className = `tab ${c===activeTab?'active':''}`;
      btn.textContent = c; btn.onclick = () => { activeTab = c; renderTabs(); renderList(); };
      $t.appendChild(btn);
    });
  }

  function openInfoModal() { document.getElementById("infoModal").style.display = "flex"; setTimeout(()=>document.getElementById("modalId").focus(), 100); }
  function closeModal() { document.querySelectorAll('.overlay').forEach(el => el.style.display = 'none'); }
  function removeIdx() { const s = state.get(curKey); s.checked = false; s.qty = 0; if(curKey === "중범죄::난폭운전") isAutoReckless = false; closeModal(); renderList(); update(); }
  function resetAll() { state.forEach(s => { s.checked = false; s.qty = 0; }); isAutoReckless = false; document.getElementById("bailIn").value = 0; isFineConverted = false; renderList(); update(); }

  function executeCopy() {
    const id = document.getElementById("modalId").value || "N/A", name = document.getElementById("modalName").value || "N/A", etc = document.getElementById("modalEtc").value || "없음";
    let txt = `[ 모찌서버 법률 집행 보고서 ]\n담당자: ${id}\n피의자: ${name}\n비고: ${etc}\n\n[ 위반 내역 ]\n`;
    let bf = 0, bt = 0, hasP = false;
    state.forEach(s => { if(s.checked) { 
      txt += `• ${s.item.name} x${s.qty} : ${(s.item.fine*s.qty).toLocaleString()}원\n`;
      bf += s.item.fine * s.qty; bt += s.item.time * s.qty; if(s.item.time > 0) hasP = true;
    }});
    const bailInVal = parseInt(document.getElementById("bailIn").value)||0;
    let maxBail = hasP ? Math.max(0, bt - 10) : bt;
    let actBail = Math.min(bailInVal, maxBail);
    let ef = actBail * 5000000, ff = bf + ef, ft = Math.max(0, bt - actBail);
    if(hasP && ft < 10) ft = 10;
    if(isFineConverted) { const conv = Math.floor(ff / 5000000); ft += conv; ff = 0; txt += `\n[ 특이사항 ]\n벌금 미납으로 인한 구금 전환 (+${conv}분)\n`; }
    else if(actBail > 0) { txt += `\n[ 보석금 정산 ]\n감면 시간: ${actBail}분 / 추가 벌금: ${ef.toLocaleString()}원\n`; }
    txt += `\n최종 벌금: ${ff.toLocaleString()}원 (${numberToKo(ff)} 원)\n최종 구금시간: ${ft}분\n────────────────`;
    const el = document.createElement('textarea'); el.value = txt; document.body.appendChild(el); el.select(); document.execCommand('copy'); document.body.removeChild(el);
    showT("성공적으로 복사되었습니다!"); closeModal();
  }

  renderTabs(); renderList(); update();
</script>
</body>
</html>
