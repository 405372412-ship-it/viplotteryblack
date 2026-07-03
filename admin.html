<!doctype html>
<html lang="zh-CN">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>VIP礼品直播抽奖后台</title>
  <style>
    :root {
      --bg: #0a0907;
      --panel: rgba(20, 17, 12, .88);
      --panel-2: rgba(35, 28, 17, .78);
      --gold: #f5c86a;
      --gold-2: #a9782b;
      --ink: #fff8e7;
      --muted: #c9b88d;
      --line: rgba(245, 200, 106, .22);
      --danger: #ff6f61;
      --ok: #57d68d;
      color-scheme: dark;
      font-family: "Microsoft YaHei", "PingFang SC", Arial, sans-serif;
    }

    * { box-sizing: border-box; }

    body {
      margin: 0;
      min-height: 100vh;
      color: var(--ink);
      background:
        linear-gradient(90deg, rgba(0,0,0,.72), rgba(0,0,0,.25), rgba(0,0,0,.72)),
        url("assets/vip-lottery-black-gold-bg.png") center / cover fixed,
        var(--bg);
    }

    body::before {
      content: "";
      position: fixed;
      inset: 0;
      pointer-events: none;
      background: repeating-linear-gradient(90deg, rgba(255,255,255,.03) 0 1px, transparent 1px 80px);
      opacity: .22;
    }

    .shell {
      position: relative;
      width: min(1440px, calc(100% - 32px));
      margin: 0 auto;
      padding: 24px 0 32px;
    }

    body.locked .shell {
      filter: blur(8px);
      pointer-events: none;
      user-select: none;
    }

    .login-gate {
      position: fixed;
      inset: 0;
      z-index: 50;
      display: none;
      place-items: center;
      padding: 20px;
      background:
        radial-gradient(circle at 50% 35%, rgba(245,200,106,.18), transparent 34%),
        rgba(4, 3, 2, .86);
      backdrop-filter: blur(16px);
    }

    body.locked .login-gate {
      display: grid;
    }

    .login-card {
      width: min(420px, 100%);
      border: 1px solid rgba(245,200,106,.35);
      border-radius: 8px;
      padding: 24px;
      background: linear-gradient(180deg, rgba(26, 20, 11, .96), rgba(8, 7, 5, .94));
      box-shadow: 0 28px 80px rgba(0,0,0,.48), inset 0 0 0 1px rgba(255,255,255,.05);
    }

    .login-card h2 {
      font-size: 24px;
      color: var(--gold);
    }

    .login-card p {
      margin-top: 8px;
      color: var(--muted);
      line-height: 1.6;
      font-size: 14px;
    }

    .login-card label {
      margin-top: 18px;
    }

    .login-error {
      min-height: 20px;
      margin-top: 10px;
      color: #ffd9d5;
      font-size: 13px;
    }

    header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 16px;
      padding: 18px 20px;
      border: 1px solid var(--line);
      border-radius: 8px;
      background: linear-gradient(135deg, rgba(15, 12, 8, .94), rgba(47, 37, 19, .76));
      box-shadow: 0 24px 70px rgba(0,0,0,.38);
    }

    h1, h2, h3, p { margin: 0; }
    h1 { font-size: 28px; font-weight: 800; }
    h2 { font-size: 18px; }
    h3 { font-size: 15px; color: var(--gold); }

    .top-meta {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
      justify-content: flex-end;
      color: var(--muted);
      font-size: 13px;
    }

    .layout {
      display: grid;
      grid-template-columns: 340px 1fr;
      gap: 16px;
      margin-top: 16px;
    }

    .panel {
      border: 1px solid var(--line);
      border-radius: 8px;
      background: var(--panel);
      box-shadow: 0 20px 54px rgba(0,0,0,.34);
      backdrop-filter: blur(18px);
      overflow: hidden;
    }

    .panel-head {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 12px;
      padding: 16px;
      border-bottom: 1px solid var(--line);
      background: linear-gradient(90deg, rgba(245,200,106,.12), transparent);
    }

    .panel-body { padding: 16px; }

    label {
      display: grid;
      gap: 8px;
      color: var(--muted);
      font-size: 13px;
      margin-bottom: 14px;
    }

    input, textarea, select {
      width: 100%;
      min-height: 42px;
      border: 1px solid rgba(245,200,106,.22);
      border-radius: 8px;
      padding: 10px 12px;
      color: var(--ink);
      background: rgba(4, 4, 3, .58);
      outline: none;
      font: inherit;
    }

    textarea { min-height: 140px; resize: vertical; line-height: 1.55; }
    input:focus, textarea:focus, select:focus { border-color: rgba(245,200,106,.72); box-shadow: 0 0 0 3px rgba(245,200,106,.13); }

    .btns { display: flex; gap: 10px; flex-wrap: wrap; }

    button, .link-btn {
      border: 1px solid rgba(245,200,106,.32);
      border-radius: 8px;
      min-height: 42px;
      padding: 0 14px;
      color: var(--ink);
      background: linear-gradient(180deg, rgba(95, 68, 25, .92), rgba(31, 25, 14, .95));
      cursor: pointer;
      font: inherit;
      font-weight: 700;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
    }

    button:hover, .link-btn:hover { border-color: var(--gold); transform: translateY(-1px); }
    button.primary { color: #17110a; background: linear-gradient(180deg, #ffe39a, #d49b37); }
    button.ghost { background: rgba(255,255,255,.04); }
    button.danger { border-color: rgba(255,111,97,.5); color: #ffd9d5; }
    button.ok { border-color: rgba(87,214,141,.5); color: #d9ffe8; }

    .round-list {
      display: grid;
      gap: 10px;
      max-height: calc(100vh - 420px);
      overflow: auto;
      padding-right: 3px;
    }

    .round-item {
      width: 100%;
      display: flex;
      align-items: center;
      gap: 10px;
      text-align: left;
      justify-content: space-between;
      min-height: 64px;
      border: 1px solid rgba(245,200,106,.32);
      border-radius: 8px;
      padding: 10px 12px;
      color: var(--ink);
      background: var(--panel-2);
      cursor: pointer;
      font: inherit;
      font-weight: 700;
    }

    .round-item:hover { border-color: var(--gold); transform: translateY(-1px); }
    .round-item.active { border-color: var(--gold); box-shadow: inset 0 0 0 1px rgba(245,200,106,.28); }
    .round-title { display: block; font-size: 14px; color: var(--ink); }
    .round-sub { display: block; margin-top: 4px; font-size: 12px; color: var(--muted); font-weight: 500; }

    .trash-btn {
      flex: 0 0 38px;
      width: 38px;
      min-width: 38px;
      height: 38px;
      min-height: 38px;
      padding: 0;
      border-color: rgba(255,111,97,.45);
      color: #ffd9d5;
      background: rgba(255,111,97,.08);
      font-size: 17px;
      line-height: 1;
    }

    .trash-btn:hover {
      border-color: var(--danger);
      color: #fff;
      background: rgba(255,111,97,.20);
    }

    .workspace {
      display: grid;
      grid-template-columns: minmax(0, 1fr) 330px;
      gap: 16px;
    }

    .grid-2 {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 14px;
    }

    .status-line {
      display: flex;
      align-items: center;
      gap: 10px;
      flex-wrap: wrap;
      color: var(--muted);
      font-size: 13px;
    }

    .pill {
      border: 1px solid var(--line);
      border-radius: 999px;
      padding: 6px 10px;
      color: var(--gold);
      background: rgba(245,200,106,.08);
      white-space: nowrap;
    }

    .preview {
      aspect-ratio: 16 / 10;
      border-radius: 8px;
      border: 1px solid var(--line);
      background: radial-gradient(circle at center, rgba(245,200,106,.16), rgba(0,0,0,.7));
      display: grid;
      place-items: center;
      overflow: hidden;
      min-height: 220px;
    }

    .preview img {
      max-width: 100%;
      max-height: 100%;
      object-fit: contain;
    }

    .gift-fallback {
      width: 150px;
      height: 150px;
      display: grid;
      place-items: center;
      border-radius: 8px;
      background: linear-gradient(135deg, #39230b, #d39a35 48%, #fff2b8 50%, #8b5a1e);
      box-shadow: 0 0 55px rgba(245,200,106,.28);
      font-size: 56px;
    }

    .winners {
      display: grid;
      gap: 10px;
      max-height: 300px;
      overflow: auto;
    }

    .winner-row {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 10px;
      padding: 10px 12px;
      border: 1px solid rgba(245,200,106,.16);
      border-radius: 8px;
      background: rgba(255,255,255,.04);
      color: var(--ink);
      font-size: 14px;
    }

    .empty {
      color: var(--muted);
      border: 1px dashed rgba(245,200,106,.28);
      border-radius: 8px;
      padding: 18px;
      text-align: center;
    }

    .toast {
      position: fixed;
      right: 24px;
      bottom: 24px;
      max-width: 360px;
      padding: 14px 16px;
      border: 1px solid rgba(245,200,106,.35);
      border-radius: 8px;
      background: rgba(16, 12, 7, .94);
      color: var(--ink);
      box-shadow: 0 18px 44px rgba(0,0,0,.42);
      opacity: 0;
      transform: translateY(12px);
      transition: .22s ease;
      pointer-events: none;
    }

    .toast.show { opacity: 1; transform: translateY(0); }

    @media (max-width: 1100px) {
      .layout, .workspace { grid-template-columns: 1fr; }
      .round-list { max-height: none; }
    }

    @media (max-width: 720px) {
      .shell { width: min(100% - 20px, 1440px); padding-top: 10px; }
      header { align-items: flex-start; flex-direction: column; }
      h1 { font-size: 22px; }
      .grid-2 { grid-template-columns: 1fr; }
      button, .link-btn { width: 100%; }
      .trash-btn { width: 38px; flex: 0 0 38px; }
    }
  </style>
</head>
<body class="locked">
  <section class="login-gate" id="loginGate" aria-label="后台登录">
    <form class="login-card" id="loginForm">
      <h2>后台管理验证</h2>
      <p>请输入管理密码。验证通过后，本设备将保持登录状态 30 天。</p>
      <label>管理密码
        <input id="adminPassword" type="password" autocomplete="current-password" placeholder="请输入密码">
      </label>
      <button class="primary" type="submit" style="width:100%">进入后台</button>
      <div class="login-error" id="loginError"></div>
    </form>
  </section>
  <main class="shell">
    <header>
      <div>
        <h1>VIP礼品直播抽奖后台</h1>
        <p class="status-line" style="margin-top:8px">多轮奖品、批量名单、内定中奖、前台大屏联动</p>
      </div>
      <div class="top-meta">
        <span class="pill" id="statePill">待准备</span>
        <a class="link-btn" href="screen.html" target="_blank" rel="noopener">打开前台抽奖页</a>
      </div>
    </header>

    <section class="layout">
      <aside class="panel">
        <div class="panel-head">
          <h2>活动与名单</h2>
          <button class="ghost" id="seedBtn" type="button">示例</button>
        </div>
        <div class="panel-body">
          <label>活动名称
            <input id="eventName" placeholder="例如：VIP客户专属礼遇抽奖夜">
          </label>
          <label>批量抽奖名单
            <textarea id="participants" placeholder="每行一个姓名，也支持逗号、顿号、空格分隔"></textarea>
          </label>
          <div class="btns">
            <button class="primary" id="saveEventBtn" type="button">保存活动</button>
            <button class="danger" id="resetBtn" type="button">重置全部</button>
          </div>
        </div>
      </aside>

      <section class="workspace">
        <div class="panel">
          <div class="panel-head">
            <h2>轮次配置</h2>
            <div class="btns">
              <button class="primary" id="saveRoundBtn" type="button">保存本轮</button>
            </div>
          </div>
          <div class="panel-body">
            <div class="grid-2">
              <label>本轮名称
                <input id="roundName" placeholder="第一轮">
              </label>
              <label>中奖人数
                <input id="winnerCount" type="number" min="1" value="1">
              </label>
            </div>
            <label>奖品名称
              <input id="prizeName" placeholder="100元礼品卡">
            </label>
            <label>奖品价值（元，可选）
              <input id="prizeValue" type="number" min="0" placeholder="不填写则不展示价值">
            </label>
            <div class="grid-2">
              <label>上传奖品图片
                <input id="prizeImage" type="file" accept="image/*">
              </label>
              <label>内定名单
                <textarea id="fixedWinners" placeholder="每行一个姓名；会优先进入本轮中奖名单"></textarea>
              </label>
            </div>
            <div class="status-line">
              <span class="pill" id="roundMeta">尚未选择轮次</span>
              <span id="saveHint">修改后请保存本轮</span>
            </div>
          </div>
        </div>

        <aside class="panel">
          <div class="panel-head">
            <h2>礼品预览</h2>
          </div>
          <div class="panel-body">
            <div class="preview" id="prizePreview"><div class="gift-fallback">礼</div></div>
            <h3 style="margin-top:14px" id="currentRoundTitle">未选择轮次</h3>
            <p class="status-line" style="margin-top:8px" id="currentPrizeText">请先配置奖品</p>
          </div>
        </aside>
      </section>
    </section>

    <section class="layout" style="grid-template-columns: 340px 1fr">
      <aside class="panel">
        <div class="panel-head">
          <h2>抽奖轮次</h2>
          <button class="ghost" id="addRoundBtn" type="button">新增轮次</button>
        </div>
        <div class="panel-body">
          <div class="round-list" id="roundList"></div>
        </div>
      </aside>

      <section class="panel">
        <div class="panel-head">
          <h2>中奖记录回溯</h2>
          <span class="pill" id="recordCount">0 条</span>
        </div>
        <div class="panel-body">
          <div class="winners" id="winnerRecords"></div>
        </div>
      </section>
    </section>
  </main>
  <div class="toast" id="toast"></div>

  <script>
    const STORE_KEY = "vip_lottery_data_v1";
    const STATE_KEY = "vip_lottery_live_state_v1";
    const ADMIN_AUTH_KEY = "vip_lottery_admin_auth_v1";
    const ADMIN_PASSWORD = "JIN10VIP13579";
    const ADMIN_AUTH_DAYS = 30;
    const $ = (id) => document.getElementById(id);

    function getAdminAuth() {
      try {
        return JSON.parse(localStorage.getItem(ADMIN_AUTH_KEY) || "null");
      } catch (error) {
        return null;
      }
    }

    function isAdminAuthed() {
      const auth = getAdminAuth();
      return Boolean(auth?.expiresAt && Date.now() < auth.expiresAt);
    }

    function unlockAdmin() {
      document.body.classList.remove("locked");
    }

    function setupAdminLogin() {
      if (isAdminAuthed()) {
        unlockAdmin();
        return;
      }
      const form = $("loginForm");
      const password = $("adminPassword");
      const error = $("loginError");
      setTimeout(() => password.focus(), 50);
      form.addEventListener("submit", (event) => {
        event.preventDefault();
        if (password.value === ADMIN_PASSWORD) {
          localStorage.setItem(ADMIN_AUTH_KEY, JSON.stringify({
            authedAt: Date.now(),
            expiresAt: Date.now() + ADMIN_AUTH_DAYS * 24 * 60 * 60 * 1000
          }));
          password.value = "";
          error.textContent = "";
          unlockAdmin();
          toast("后台登录成功，30 天内免登录");
        } else {
          error.textContent = "密码不正确，请重新输入";
          password.select();
        }
      });
    }

    const fallbackNames = ["林佳怡", "周明轩", "陈思雨", "王浩然", "李欣然", "赵子涵", "黄嘉豪", "吴雅婷", "郑宇航", "孙若曦", "胡梓晨", "郭雨桐", "何俊杰", "高诗涵", "罗一诺", "梁景行", "宋佳宁", "谢文博", "唐若琳", "许嘉泽", "邓依依", "冯子墨", "曹雨辰", "曾语汐", "彭睿哲", "潘可欣", "袁昊天", "董芷晴", "苏星辰", "吕安琪", "余锦程", "叶心语", "姚泽宇", "秦沐阳", "石婉清", "夏云帆", "姜知夏", "傅景宁", "邹奕辰", "程若熙", "孟嘉树", "龙诗琪", "戴辰逸", "乔安然", "贺嘉言", "田沐宸", "陆清欢", "范明哲", "江雨薇", "白亦航", "金思远", "任可心", "钟云舒", "韩予安", "邱泽霖", "康若宁", "尹星野", "毛嘉懿", "廖书瑶", "黎景澄"];

    let data = loadData();
    let selectedRoundId = data.rounds[0]?.id || "";

    function uid() {
      return Date.now().toString(36) + Math.random().toString(36).slice(2, 8);
    }

    function parseNames(value) {
      return [...new Set(String(value || "").split(/[\n,，、\s]+/).map((name) => name.trim()).filter(Boolean))];
    }

    function defaultData() {
      return {
        eventName: "VIP客户专属礼遇抽奖夜",
        participants: fallbackNames,
        rounds: [
          { id: uid(), name: "第一轮", prizeName: "电脑", prizeValue: "", winnerCount: 1, fixedWinners: [], prizeImage: "assets/vip-prize-computer.png", winners: [], finalizedAt: "" },
          { id: uid(), name: "第二轮", prizeName: "手表", prizeValue: "", winnerCount: 1, fixedWinners: [], prizeImage: "assets/vip-prize-watch.png", winners: [], finalizedAt: "" },
          { id: uid(), name: "第三轮", prizeName: "手机", prizeValue: "", winnerCount: 1, fixedWinners: [], prizeImage: "assets/vip-prize-phone.png", winners: [], finalizedAt: "" },
          { id: uid(), name: "第四轮", prizeName: "京东卡", prizeValue: "", winnerCount: 10, fixedWinners: [], prizeImage: "assets/vip-prize-jd-card.png", winners: [], finalizedAt: "" }
        ],
        records: [],
        updatedAt: Date.now()
      };
    }

    function loadData() {
      try {
        const raw = localStorage.getItem(STORE_KEY);
        return raw ? JSON.parse(raw) : defaultData();
      } catch (error) {
        return defaultData();
      }
    }

    function saveData() {
      data.updatedAt = Date.now();
      localStorage.setItem(STORE_KEY, JSON.stringify(data));
    }

    function getRound() {
      return data.rounds.find((round) => round.id === selectedRoundId) || data.rounds[0];
    }

    function fillForm() {
      $("eventName").value = data.eventName || "";
      $("participants").value = data.participants.join("\n");
      const round = getRound();
      selectedRoundId = round?.id || "";
      $("roundName").value = round?.name || "";
      $("prizeName").value = round?.prizeName || "";
      $("prizeValue").value = round?.prizeValue || "";
      $("winnerCount").value = round?.winnerCount || 1;
      $("fixedWinners").value = (round?.fixedWinners || []).join("\n");
      $("roundMeta").textContent = round ? `${round.name} · ${buildPrizeMeta(round)} · ${round.prizeName}` : "尚未选择轮次";
      $("currentRoundTitle").textContent = round ? round.name : "未选择轮次";
      $("currentPrizeText").textContent = round ? `${round.prizeName} · ${buildPrizeMeta(round)}` : "请先配置奖品";
      $("saveHint").textContent = round?.finalizedAt ? `最终版已确认 · ${new Date(round.finalizedAt).toLocaleTimeString()}` : "草稿会自动保存，点击保存本轮确认最终版";
      renderPreview(round);
    }

    function buildPrizeMeta(round) {
      const value = String(round?.prizeValue || "").trim();
      const countText = `${round?.winnerCount || 1} 个中奖名额`;
      return value ? `价值${value}元 · ${countText}` : countText;
    }

    function renderPreview(round) {
      const box = $("prizePreview");
      box.innerHTML = "";
      if (round?.prizeImage) {
        const img = document.createElement("img");
        img.src = round.prizeImage;
        img.alt = round.prizeName || "奖品图片";
        box.appendChild(img);
      } else {
        const gift = document.createElement("div");
        gift.className = "gift-fallback";
        gift.textContent = "礼";
        box.appendChild(gift);
      }
    }

    function renderRounds() {
      const list = $("roundList");
      list.innerHTML = "";
      if (!data.rounds.length) {
        list.innerHTML = '<div class="empty">暂无轮次</div>';
        return;
      }
      data.rounds.forEach((round, index) => {
        const btn = document.createElement("div");
        btn.className = "round-item" + (round.id === selectedRoundId ? " active" : "");
        btn.setAttribute("role", "button");
        btn.tabIndex = 0;
        const stateText = round.finalizedAt ? "最终版" : "草稿";
        btn.innerHTML = `<span><span class="round-title">${index + 1}. ${round.name}</span><span class="round-sub">${round.prizeName || "未填奖品"} · ${buildPrizeMeta(round)} · ${stateText}</span></span><button class="trash-btn" type="button" title="删除本轮抽奖" aria-label="删除${round.name}">🗑</button>`;
        btn.addEventListener("click", () => {
          selectedRoundId = round.id;
          fillForm();
          renderRounds();
        });
        btn.addEventListener("keydown", (event) => {
          if (event.key === "Enter" || event.key === " ") {
            event.preventDefault();
            selectedRoundId = round.id;
            fillForm();
            renderRounds();
          }
        });
        btn.querySelector(".trash-btn").addEventListener("click", (event) => {
          event.stopPropagation();
          deleteRound(round.id);
        });
        list.appendChild(btn);
      });
    }

    function renderRecords() {
      const records = $("winnerRecords");
      const rows = (data.records || []).slice().reverse();
      const total = rows.reduce((sum, record) => sum + (record.winners || []).length, 0);
      $("recordCount").textContent = `${total} 条`;
      if (!rows.length) {
        records.innerHTML = '<div class="empty">前台完成开奖后，这里会保存每轮中奖名单</div>';
        return;
      }
      records.innerHTML = "";
      rows.forEach((record) => {
        const row = document.createElement("div");
        row.className = "winner-row";
        row.innerHTML = `<span><strong>${record.roundName || "未命名轮次"}</strong> · ${record.prizeName || "奖品"}<br><small>${(record.winners || []).join("、")}</small></span><span>${new Date(record.time).toLocaleTimeString()}</span>`;
        records.appendChild(row);
      });
    }

    function saveEvent() {
      data.eventName = $("eventName").value.trim() || "VIP礼品直播抽奖";
      data.participants = parseNames($("participants").value);
      saveData();
      toast(`活动已保存，共 ${data.participants.length} 人`);
    }

    function updateRoundFromForm(finalize = false) {
      const round = getRound();
      if (!round) return null;
      round.name = $("roundName").value.trim() || "未命名轮次";
      round.prizeName = $("prizeName").value.trim() || "神秘礼品";
      round.prizeValue = $("prizeValue").value.trim();
      round.winnerCount = Math.max(1, Number($("winnerCount").value) || 1);
      round.fixedWinners = parseNames($("fixedWinners").value);
      round.draftSavedAt = Date.now();
      if (finalize) {
        round.finalizedAt = Date.now();
      } else {
        round.finalizedAt = "";
      }
      return round;
    }

    function autoSaveDraft() {
      data.eventName = $("eventName").value.trim() || "VIP礼品直播抽奖";
      data.participants = parseNames($("participants").value);
      const round = updateRoundFromForm(false);
      if (!round) return;
      saveData();
      $("roundMeta").textContent = `${round.name} · ${buildPrizeMeta(round)} · ${round.prizeName}`;
      $("currentRoundTitle").textContent = round.name;
      $("currentPrizeText").textContent = `${round.prizeName} · ${buildPrizeMeta(round)}`;
      $("saveHint").textContent = `草稿已自动保存 · ${new Date(round.draftSavedAt).toLocaleTimeString()}，点击保存本轮确认最终版`;
      renderPreview(round);
      renderRounds();
    }

    function queueAutoSave() {
      clearTimeout(queueAutoSave.timer);
      queueAutoSave.timer = setTimeout(autoSaveDraft, 500);
    }

    function autoSaveEventDraft() {
      data.eventName = $("eventName").value.trim() || "VIP礼品直播抽奖";
      data.participants = parseNames($("participants").value);
      saveData();
      $("saveHint").textContent = `活动与名单已自动保存 · ${new Date().toLocaleTimeString()}`;
    }

    function queueAutoSaveEvent() {
      clearTimeout(queueAutoSaveEvent.timer);
      queueAutoSaveEvent.timer = setTimeout(autoSaveEventDraft, 500);
    }

    function saveRound() {
      const round = updateRoundFromForm(true);
      if (!round) return;
      data.eventName = $("eventName").value.trim() || "VIP礼品直播抽奖";
      data.participants = parseNames($("participants").value);
      saveData();
      fillForm();
      renderRounds();
      toast("本轮最终版已确认");
    }

    function addRound() {
      const round = { id: uid(), name: `第${data.rounds.length + 1}轮`, prizeName: "新奖品", prizeValue: "", winnerCount: 1, fixedWinners: [], prizeImage: "", winners: [], finalizedAt: "" };
      data.rounds.push(round);
      selectedRoundId = round.id;
      saveData();
      fillForm();
      renderRounds();
      toast("已新增轮次");
    }

    function deleteRound(roundId) {
      const round = data.rounds.find((item) => item.id === roundId);
      if (!round) return;
      if (!confirm(`确认删除「${round.name}」这轮抽奖？相关中奖记录也会一起删除。`)) return;
      const wasSelected = selectedRoundId === roundId;
      data.rounds = data.rounds.filter((item) => item.id !== roundId);
      data.records = (data.records || []).filter((record) => record.roundId !== roundId);
      if (!data.rounds.length) {
        const next = { id: uid(), name: "第一轮", prizeName: "新奖品", prizeValue: "", winnerCount: 1, fixedWinners: [], prizeImage: "", winners: [], finalizedAt: "" };
        data.rounds.push(next);
      }
      if (wasSelected || !data.rounds.some((item) => item.id === selectedRoundId)) {
        selectedRoundId = data.rounds[0].id;
      }
      saveData();
      localStorage.removeItem("vip_lottery_screen_state_v1");
      render();
      toast("已删除本轮抽奖");
    }

    function resetAll() {
      if (!confirm("确认重置全部活动、轮次和中奖记录？")) return;
      data = defaultData();
      selectedRoundId = data.rounds[0].id;
      saveData();
      localStorage.removeItem(STATE_KEY);
      localStorage.removeItem("vip_lottery_screen_state_v1");
      render();
      toast("已重置为初始示例");
    }

    function seed() {
      data = defaultData();
      selectedRoundId = data.rounds[0].id;
      saveData();
      render();
      toast("示例活动已载入");
    }

    function toast(message) {
      const box = $("toast");
      box.textContent = message;
      box.classList.add("show");
      clearTimeout(toast.timer);
      toast.timer = setTimeout(() => box.classList.remove("show"), 2200);
    }

    $("prizeImage").addEventListener("change", (event) => {
      const file = event.target.files[0];
      const round = getRound();
      if (!file || !round) return;
      const reader = new FileReader();
      reader.onload = () => {
        round.prizeImage = reader.result;
        round.draftSavedAt = Date.now();
        round.finalizedAt = "";
        saveData();
        renderPreview(round);
        renderRounds();
        $("saveHint").textContent = `图片已自动保存为草稿，点击保存本轮确认最终版`;
        toast("奖品图片已自动保存为草稿");
      };
      reader.readAsDataURL(file);
    });

    ["eventName", "participants"].forEach((id) => {
      $(id).addEventListener("input", queueAutoSaveEvent);
      $(id).addEventListener("change", queueAutoSaveEvent);
    });

    ["roundName", "prizeName", "prizeValue", "winnerCount", "fixedWinners"].forEach((id) => {
      $(id).addEventListener("input", queueAutoSave);
      $(id).addEventListener("change", queueAutoSave);
    });

    $("saveEventBtn").addEventListener("click", saveEvent);
    $("saveRoundBtn").addEventListener("click", saveRound);
    $("addRoundBtn").addEventListener("click", addRound);
    $("resetBtn").addEventListener("click", resetAll);
    $("seedBtn").addEventListener("click", seed);
    window.addEventListener("storage", (event) => {
      if (event.key === STORE_KEY) {
        data = loadData();
        render();
      }
    });

    function render() {
      fillForm();
      renderRounds();
      renderRecords();
      $("statePill").textContent = "配置模式";
    }

    if (!localStorage.getItem(STORE_KEY)) saveData();
    setupAdminLogin();
    render();
  </script>
</body>
</html>

