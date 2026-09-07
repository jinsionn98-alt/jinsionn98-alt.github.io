<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>팬사인회 응모 정리</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Unbounded:wght@600;800&display=swap" rel="stylesheet">
<link rel="stylesheet" as="style" crossorigin href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/variable/pretendardvariable-dynamic-subset.css" />

<!-- Firebase (3명이 같이 쓰는 저장소) -->
<script src="https://www.gstatic.com/firebasejs/10.12.2/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/10.12.2/firebase-firestore-compat.js"></script>

<style>
  :root{
    --bg:#FFFFFF;
    --surface:#F8F7FB;
    --border:#E8E6F0;
    --ink:#17151F;
    --muted:#7A7787;
    --accent:#4F46E5;
    --accent-soft:#EEEDFC;
    --green:#12B76A;
    --green-soft:#E7F8EF;
    --red:#E5484D;
    --gray-chip:#EDEBF3;
  }
  *{box-sizing:border-box;}
  html,body{margin:0;padding:0;}
  body{
    background:var(--bg);
    color:var(--ink);
    font-family:'Pretendard Variable', Pretendard, -apple-system, sans-serif;
    line-height:1.6;
  }
  .wrap{ max-width:820px; margin:0 auto; padding:64px 24px 120px; }

  .eyebrow{ display:flex; align-items:center; gap:8px; color:var(--accent); font-size:13px; font-weight:700; margin-bottom:16px; }
  .eyebrow .dot{ width:6px;height:6px;border-radius:50%; background:var(--accent); }
  h1{ font-family:'Unbounded', sans-serif; font-weight:800; font-size:clamp(30px, 5vw, 42px); margin:0 0 12px; letter-spacing:-0.01em; }
  .lede{ color:var(--muted); font-size:15px; max-width:54ch; margin:0 0 24px; }

  .toprow{ display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:12px; margin-bottom:40px; }
  .stats{ display:flex; gap:10px; }
  .stat{ display:flex; align-items:baseline; gap:6px; background:var(--surface); border:1px solid var(--border); border-radius:10px; padding:10px 16px; font-size:13px; color:var(--muted); font-weight:600; }
  .stat b{ font-family:'Unbounded', sans-serif; font-size:18px; color:var(--ink); font-weight:800; }
  .stat.on b{ color:var(--accent); }

  .btn{ display:inline-flex; align-items:center; gap:6px; font-size:14px; font-weight:700; padding:11px 18px; border-radius:10px; border:none; cursor:pointer; }
  .btn.primary{ background:var(--accent); color:#fff; }
  .btn.ghost{ background:transparent; color:var(--ink); border:1px solid var(--border); }
  .btn.small{ padding:6px 12px; font-size:12px; }
  .btn.danger{ background:transparent; color:var(--red); border:1px solid rgba(229,72,77,0.3); }

  /* 새 응모 추가 폼 */
  .add-panel{
    display:none;
    background:var(--surface);
    border:1px solid var(--border);
    border-radius:16px;
    padding:24px;
    margin-bottom:40px;
  }
  .add-panel.open{ display:block; }
  .add-panel h2{ font-size:16px; margin:0 0 18px; }
  .form-grid{ display:grid; grid-template-columns:1fr 1fr; gap:14px 16px; }
  .form-grid .full{ grid-column:1 / -1; }
  .field label{ display:block; font-size:12px; font-weight:700; color:var(--muted); margin-bottom:6px; }
  .field input, .field select, .field textarea{
    width:100%; padding:10px 12px; border:1px solid var(--border); border-radius:8px;
    font-size:14px; font-family:inherit; background:#fff; color:var(--ink);
  }
  .field textarea{ resize:vertical; min-height:60px; }
  .form-actions{ display:flex; gap:8px; margin-top:18px; }

  .event{ border:1px solid var(--border); border-radius:14px; margin-bottom:20px; overflow:hidden; }
  .event-head{ padding:20px 24px 18px; border-bottom:1px solid var(--border); }
  .row-top{ display:flex; justify-content:space-between; align-items:flex-start; gap:12px; margin-bottom:8px; }
  .event h3{ margin:0; font-size:17px; font-weight:700; }
  .head-right{ display:flex; align-items:center; gap:8px; }

  .status{ flex-shrink:0; font-size:12px; font-weight:700; padding:5px 10px; border-radius:999px; white-space:nowrap; border:none; cursor:pointer; }
  .status.open{ background:var(--accent-soft); color:var(--accent); }
  .status.closed{ background:var(--surface); color:var(--muted); }
  .status.done{ background:var(--green-soft); color:var(--green); }

  .info{ display:grid; grid-template-columns:repeat(auto-fit, minmax(140px,1fr)); gap:10px 20px; font-size:13px; }
  .info dt{ color:var(--muted); margin-bottom:2px; }
  .info dd{ margin:0; font-weight:600; }

  .members{ padding:18px 24px 22px; }
  .chips{ display:grid; grid-template-columns:repeat(5, 1fr); gap:8px; }
  .chip{
    text-align:center; font-size:13px; font-weight:600; padding:9px 4px; border-radius:8px;
    background:var(--gray-chip); color:var(--muted); border:1px solid transparent;
    cursor:pointer; user-select:none; transition:background .12s ease, color .12s ease, border-color .12s ease;
  }
  .chip.on{ background:var(--green-soft); color:var(--green); border-color:rgba(18,183,106,0.25); }

  .legend{ display:flex; gap:18px; font-size:13px; color:var(--muted); margin-bottom:32px; }
  .legend span{ display:flex; align-items:center; gap:6px; }
  .legend i{ width:12px;height:12px;border-radius:4px; display:inline-block; }
  .legend .on i{ background:var(--green); }
  .legend .off i{ background:var(--gray-chip); border:1px solid var(--border); }

  .empty{ color:var(--muted); font-size:14px; padding:40px 0; text-align:center; }
  footer{ margin-top:56px; padding-top:20px; border-top:1px solid var(--border); font-size:13px; color:var(--muted); }

  @media (max-width:520px){
    .chips{ grid-template-columns:repeat(4, 1fr); }
    .form-grid{ grid-template-columns:1fr; }
  }
</style>
</head>
<body>
<div class="wrap">

  <div class="eyebrow"><span class="dot"></span>MY FANSIGN TRACKER</div>
  <h1>팬사인회 응모 현황</h1>
  <p class="lede">응모 중인 팬사인회와 멤버별 참여 여부를 3명이 함께 실시간으로 관리해요.</p>

  <div class="toprow">
    <div class="stats">
      <div class="stat on"><b id="countOpen">0</b>응모중</div>
      <div class="stat"><b id="countClosed">0</b>마감/완료</div>
    </div>
    <button class="btn primary" id="toggleAddBtn">＋ 새 응모 추가</button>
  </div>

  <div class="add-panel" id="addPanel">
    <h2>새 응모 추가</h2>
    <div class="form-grid">
      <div class="field"><label>제목 *</label><input id="f-title" placeholder="예: 정규 3집 팬사인회"></div>
      <div class="field"><label>유형</label>
        <select id="f-type"><option>대면</option><option>영통</option><option>포토</option></select>
      </div>
      <div class="field"><label>음반사/앨범</label><input id="f-agency" placeholder="예: 위버스샵"></div>
      <div class="field"><label>회차</label><input id="f-round" placeholder="예: 1차"></div>
      <div class="field"><label>응모기간</label><input id="f-apply" placeholder="예: 9/5 ~ 9/10"></div>
      <div class="field"><label>당첨자발표</label><input id="f-announce" placeholder="예: 9/11(금)"></div>
      <div class="field"><label>팬사인회 날짜</label><input id="f-date" placeholder="예: 9/12(토)"></div>
      <div class="field"><label>시간</label><input id="f-time" placeholder="예: 오후 3:00"></div>
      <div class="field"><label>상태</label>
        <select id="f-status"><option value="open">응모중</option><option value="closed">마감</option><option value="done">참여완료</option></select>
      </div>
      <div class="field full"><label>비고</label><textarea id="f-note" placeholder="개인영통 / 단체영통 / 미공포 / 앨범 버전 다름 등"></textarea></div>
    </div>
    <div class="form-actions">
      <button class="btn primary" id="saveBtn">저장</button>
      <button class="btn ghost" id="cancelBtn">취소</button>
    </div>
  </div>

  <div class="legend">
    <span class="on"><i></i>참여</span>
    <span class="off"><i></i>불참여</span>
  </div>

  <div id="eventList"></div>

  <footer>이 페이지는 GitHub Pages + Firebase로 3명이 실시간 공유합니다.</footer>
</div>

<script>
  // ▼▼▼ 여기에 Firebase 콘솔에서 복사한 firebaseConfig를 통째로 붙여넣으세요 ▼▼▼
  const firebaseConfig = {
    apiKey: "AIzaSyAJm4x8119MbQ1iOwb4OwewmtloLIaDSvo",
    authDomain: "idntt-fansign.firebaseapp.com",
    projectId: "idntt-fansign",
    storageBucket: "idntt-fansign.firebasestorage.app",
    messagingSenderId: "914863581388",
    appId: "1:914863581388:web:b7d4cfd50a15b717857a69"
  };
  // ▲▲▲ 여기까지 ▲▲▲

  firebase.initializeApp(firebaseConfig);
  const db = firebase.firestore();
  const col = db.collection('events');

  const MEMBERS = ["토와","김희주","조은찬","김도훈","이규혁","박누리","김은성","곽기웅","최경빈","김주호","김성준","이청명","이환희","이재영","남지운","양경호","한예준","이주헌","황은수","최태인"];

  const statusLabel = { open: '응모 중', closed: '마감', done: '참여완료' };

  // 새 응모 추가 패널 열고 닫기
  document.getElementById('toggleAddBtn').addEventListener('click', () => {
    document.getElementById('addPanel').classList.toggle('open');
  });
  document.getElementById('cancelBtn').addEventListener('click', () => {
    document.getElementById('addPanel').classList.remove('open');
  });

  document.getElementById('saveBtn').addEventListener('click', async () => {
    const title = document.getElementById('f-title').value.trim();
    if(!title){ alert('제목을 입력해주세요'); return; }

    const members = {};
    MEMBERS.forEach(m => members[m] = false);

    await col.add({
      title,
      type: document.getElementById('f-type').value,
      agency: document.getElementById('f-agency').value,
      round: document.getElementById('f-round').value,
      apply: document.getElementById('f-apply').value,
      announce: document.getElementById('f-announce').value,
      date: document.getElementById('f-date').value,
      time: document.getElementById('f-time').value,
      status: document.getElementById('f-status').value,
      note: document.getElementById('f-note').value,
      members,
      createdAt: firebase.firestore.FieldValue.serverTimestamp()
    });

    ['f-title','f-agency','f-round','f-apply','f-announce','f-date','f-time','f-note'].forEach(id => document.getElementById(id).value = '');
    document.getElementById('addPanel').classList.remove('open');
  });

  function renderEvent(doc){
    const d = doc.data();
    const el = document.createElement('div');
    el.className = 'event';

    const chipsHtml = MEMBERS.map(m => {
      const on = d.members && d.members[m];
      return `<div class="chip ${on ? 'on' : ''}" data-member="${m}">${m}</div>`;
    }).join('');

    el.innerHTML = `
      <div class="event-head">
        <div class="row-top">
          <h3>${d.title || ''}</h3>
          <div class="head-right">
            <select class="status ${d.status}" data-role="status">
              <option value="open" ${d.status==='open'?'selected':''}>응모 중</option>
              <option value="closed" ${d.status==='closed'?'selected':''}>마감</option>
              <option value="done" ${d.status==='done'?'selected':''}>참여완료</option>
            </select>
            <button class="btn small danger" data-role="delete">삭제</button>
          </div>
        </div>
        <dl class="info">
          <div><dt>유형</dt><dd>${d.type || '-'}</dd></div>
          <div><dt>음반사</dt><dd>${d.agency || '-'}</dd></div>
          <div><dt>회차</dt><dd>${d.round || '-'}</dd></div>
          <div><dt>응모기간</dt><dd>${d.apply || '-'}</dd></div>
          <div><dt>당첨자발표</dt><dd>${d.announce || '-'}</dd></div>
          <div><dt>팬사인회 날짜</dt><dd>${d.date || '-'} ${d.time || ''}</dd></div>
        </dl>
        ${d.note ? `<div style="margin-top:10px;font-size:13px;color:var(--muted)">${d.note}</div>` : ''}
      </div>
      <div class="members">
        <div class="chips">${chipsHtml}</div>
      </div>
    `;

    // 상태 변경
    el.querySelector('[data-role="status"]').addEventListener('change', (e) => {
      col.doc(doc.id).update({ status: e.target.value });
    });

    // 삭제
    el.querySelector('[data-role="delete"]').addEventListener('click', () => {
      if(confirm('이 응모 기록을 삭제할까요?')) col.doc(doc.id).delete();
    });

    // 멤버 참여 토글
    el.querySelectorAll('.chip').forEach(chip => {
      chip.addEventListener('click', () => {
        const member = chip.dataset.member;
        const nowOn = chip.classList.contains('on');
        col.doc(doc.id).update({ [`members.${member}`]: !nowOn });
      });
    });

    return el;
  }

  // 실시간 반영
  col.orderBy('createdAt', 'desc').onSnapshot(snapshot => {
    const list = document.getElementById('eventList');
    list.innerHTML = '';
    let openCount = 0, restCount = 0;

    if(snapshot.empty){
      list.innerHTML = '<div class="empty">아직 등록된 응모가 없어요. 위의 "＋ 새 응모 추가" 버튼으로 시작해보세요.</div>';
    }

    snapshot.forEach(doc => {
      list.appendChild(renderEvent(doc));
      const s = doc.data().status;
      if(s === 'open') openCount++; else restCount++;
    });

    document.getElementById('countOpen').textContent = openCount;
    document.getElementById('countClosed').textContent = restCount;
  }, err => {
    document.getElementById('eventList').innerHTML =
      '<div class="empty">연결에 실패했어요. firebaseConfig 값을 다시 확인해주세요.<br>(' + err.message + ')</div>';
  });
</script>
</body>
</html>
