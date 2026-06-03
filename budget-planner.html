<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Budget Planner</title>
<link href="https://fonts.googleapis.com/css2?family=Lora:ital,wght@0,400;0,600;1,400&family=DM+Mono:wght@300;400&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  body { background: #fdf6f0; font-family: 'Georgia', serif; color: #4a3f3a; min-height: 100vh; }
  #app { max-width: 480px; margin: 0 auto; min-height: 100vh; display: flex; flex-direction: column; }
  ::-webkit-scrollbar { width: 4px; }
  ::-webkit-scrollbar-thumb { background: #e8d5c8; border-radius: 4px; }

  .header { background: #fff8f5; padding: 24px 24px 0; border-bottom: 1px solid #f0e4dc; position: sticky; top: 0; z-index: 10; }
  .header-top { display: flex; align-items: center; justify-content: space-between; margin-bottom: 18px; }
  .logo-title { font-family: 'Lora', serif; font-size: 24px; font-weight: 600; color: #7a5060; line-height: 1; }
  .logo-sub { font-family: 'DM Mono', monospace; font-size: 9px; color: #c4a8b8; letter-spacing: 3px; margin-top: 3px; }
  .month-nav { display: flex; align-items: center; gap: 10px; background: #f5ebe5; border-radius: 20px; padding: 6px 14px; }
  .month-nav button { background: none; border: none; color: #c4a8a0; cursor: pointer; font-size: 16px; line-height: 1; }
  .month-nav button:hover { color: #b07090; }
  .month-label { font-family: 'DM Mono', monospace; font-size: 10px; color: #9a7878; letter-spacing: 2px; min-width: 54px; text-align: center; }
  .tabs { display: flex; align-items: center; }
  .tab { background: none; border: none; border-bottom: 2px solid transparent; cursor: pointer; padding: 10px 16px; font-family: 'DM Mono', monospace; font-size: 10px; letter-spacing: 2px; color: #c4a89a; transition: all 0.2s; }
  .tab.active { color: #b07090; border-bottom-color: #b07090; }
  .saving-badge { margin-left: auto; font-family: 'DM Mono', monospace; font-size: 9px; color: #c4a8b8; letter-spacing: 2px; padding-bottom: 10px; }

  .content { padding: 0 20px 100px; flex: 1; }

  /* Summary */
  .summary-grid { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 10px; margin: 20px 0; }
  .summary-card { border-radius: 14px; padding: 16px 12px; }
  .summary-label { font-family: 'DM Mono', monospace; font-size: 8px; letter-spacing: 2px; color: #9a8888; margin-bottom: 7px; }
  .summary-value { font-family: 'DM Mono', monospace; font-size: 11px; }

  /* Section label */
  .section-label { font-family: 'DM Mono', monospace; font-size: 9px; color: #c4a8b8; letter-spacing: 3px; margin-bottom: 14px; margin-top: 4px; }

  /* Standalone category row */
  .cat-row { margin-bottom: 16px; }
  .cat-row-top { display: flex; justify-content: space-between; align-items: center; }
  .cat-name { display: flex; align-items: center; gap: 8px; font-size: 13px; color: #6a5858; }
  .cat-icon-circle { width: 28px; height: 28px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 12px; flex-shrink: 0; }
  .cat-amount { font-family: 'DM Mono', monospace; font-size: 11px; color: #9a8888; }
  .cat-amount.over { color: #d07888; }
  .prog-bar { height: 5px; background: #f0e4dc; border-radius: 3px; margin-top: 7px; overflow: hidden; }
  .prog-fill { height: 5px; border-radius: 3px; transition: width 0.5s; }

  /* Group */
  .group-block { margin-bottom: 20px; background: #fff8f5; border-radius: 14px; overflow: hidden; border: 1px solid #f0e4dc; }
  .group-header { display: flex; justify-content: space-between; align-items: center; padding: 12px 14px 8px; }
  .group-title { display: flex; align-items: center; gap: 8px; font-size: 13px; font-weight: 600; color: #5a4858; }
  .group-icon { width: 28px; height: 28px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 12px; }
  .group-total { font-family: 'DM Mono', monospace; font-size: 11px; color: #9a8888; }
  .group-prog { height: 4px; background: #f0e4dc; margin: 0 14px 2px; border-radius: 2px; overflow: hidden; }
  .group-prog-fill { height: 4px; border-radius: 2px; transition: width 0.5s; }
  .sub-rows { padding: 4px 14px 12px; }
  .sub-row { display: flex; justify-content: space-between; align-items: center; padding: 8px 0; border-bottom: 1px solid #f8f0ec; }
  .sub-row:last-child { border-bottom: none; }
  .sub-name { display: flex; align-items: center; gap: 8px; font-size: 12px; color: #7a6868; }
  .sub-icon { width: 22px; height: 22px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 10px; flex-shrink: 0; }
  .sub-right { display: flex; flex-direction: column; align-items: flex-end; gap: 4px; }
  .sub-amount { font-family: 'DM Mono', monospace; font-size: 10px; color: #9a8888; }
  .sub-amount.over { color: #d07888; }
  .sub-prog { width: 80px; height: 4px; background: #f0e4dc; border-radius: 2px; overflow: hidden; }
  .sub-prog-fill { height: 4px; border-radius: 2px; transition: width 0.5s; }

  /* Transactions */
  .tx-row { display: flex; align-items: center; gap: 12px; padding: 12px 8px; border-bottom: 1px solid #f5ebe5; cursor: pointer; border-radius: 8px; transition: background 0.15s; }
  .tx-row:hover { background: #fdf0f5; }
  .tx-icon { width: 30px; height: 30px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 13px; flex-shrink: 0; }
  .tx-info { flex: 1; min-width: 0; }
  .tx-note { font-size: 13px; color: #6a5858; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
  .tx-meta { font-family: 'DM Mono', monospace; font-size: 9px; color: #c4a8a0; margin-top: 2px; }
  .tx-amount { font-family: 'DM Mono', monospace; font-size: 12px; flex-shrink: 0; }
  .tx-del { background: none; border: none; color: #ddc8c0; cursor: pointer; font-size: 18px; padding: 0 4px; transition: color 0.2s; line-height: 1; }
  .tx-del:hover { color: #e07888; }

  /* Empty */
  .empty { text-align: center; padding: 48px 0; }
  .empty-title { font-family: 'Lora', serif; font-style: italic; font-size: 20px; color: #c4b0b8; margin-bottom: 8px; }
  .empty-sub { font-family: 'DM Mono', monospace; font-size: 9px; color: #d8c8c0; letter-spacing: 2px; }

  /* Form */
  .panel { padding-top: 24px; }
  .panel-title { display: flex; align-items: center; gap: 10px; margin-bottom: 22px; }
  .panel-title h2 { font-family: 'Lora', serif; font-style: italic; font-size: 20px; color: #9a7888; font-weight: 400; }
  .edit-badge { font-family: 'DM Mono', monospace; font-size: 9px; background: #fdeef5; color: #c090a8; padding: 2px 8px; border-radius: 10px; letter-spacing: 1px; }
  .field { margin-bottom: 16px; }
  .field-label { font-family: 'DM Mono', monospace; font-size: 9px; color: #c4a8b8; letter-spacing: 2px; margin-bottom: 8px; }
  .input-field { background: #fff8f5; border: 1.5px solid #e8d5c8; color: #4a3f3a; padding: 10px 14px; font-family: 'DM Mono', monospace; font-size: 13px; width: 100%; outline: none; border-radius: 8px; transition: border 0.2s; }
  .input-field:focus { border-color: #c9a0b8; }
  select.input-field { appearance: none; cursor: pointer; }

  .type-toggle { display: flex; background: #f5ebe5; border-radius: 10px; padding: 4px; gap: 4px; }
  .type-opt { flex: 1; padding: 9px; background: none; border: none; cursor: pointer; font-family: 'DM Mono', monospace; font-size: 10px; letter-spacing: 1.5px; border-radius: 7px; color: #b09088; transition: all 0.2s; }
  .type-opt.sel-expense { background: #fff0f3; color: #d07090; }
  .type-opt.sel-income { background: #f0fff4; color: #5a9e70; }

  /* Category picker */
  .cat-picker { background: #fff8f5; border: 1.5px solid #e8d5c8; border-radius: 10px; overflow: hidden; max-height: 240px; overflow-y: auto; }
  .cat-group-label { font-family: 'DM Mono', monospace; font-size: 8px; letter-spacing: 2px; color: #c4a8b8; padding: 8px 14px 4px; background: #fdf0f8; border-bottom: 1px solid #f0e4dc; }
  .cat-option { display: flex; align-items: center; gap: 10px; padding: 9px 14px; cursor: pointer; transition: background 0.15s; border-bottom: 1px solid #f8f0ec; }
  .cat-option:last-child { border-bottom: none; }
  .cat-option:hover { background: #fdf0f5; }
  .cat-option.selected { background: #fdeef5; }
  .cat-option-icon { width: 24px; height: 24px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 11px; flex-shrink: 0; }
  .cat-option-label { font-size: 13px; color: #6a5858; }
  .cat-option.selected .cat-option-label { color: #b07090; }
  .check { margin-left: auto; color: #c9a0b8; font-size: 14px; }

  /* Buttons */
  .btn-row { display: flex; gap: 10px; margin-top: 24px; }
  .primary-btn { background: linear-gradient(135deg, #e8a0b8, #c890a8); color: #fff; border: none; padding: 13px 24px; font-family: 'DM Mono', monospace; font-size: 11px; letter-spacing: 2px; cursor: pointer; border-radius: 10px; flex: 2; transition: opacity 0.2s; }
  .primary-btn:hover { opacity: 0.88; }
  .ghost-btn { background: none; border: 1.5px solid #e8d5c8; color: #b09088; padding: 11px 24px; font-family: 'DM Mono', monospace; font-size: 11px; letter-spacing: 2px; cursor: pointer; border-radius: 10px; flex: 1; transition: all 0.2s; }
  .ghost-btn:hover { border-color: #c9a0b8; color: #b07090; }
  .delete-link { background: none; border: none; color: #e0a0a8; font-family: 'DM Mono', monospace; font-size: 10px; letter-spacing: 1px; cursor: pointer; width: 100%; padding: 10px 0; margin-top: 6px; text-align: center; display: block; }

  /* Settings */
  .settings-group { background: #fff8f5; border: 1px solid #f0e4dc; border-radius: 12px; margin-bottom: 16px; overflow: hidden; }
  .settings-group-label { font-family: 'DM Mono', monospace; font-size: 9px; letter-spacing: 2px; color: #c4a8b8; padding: 10px 14px 6px; background: #fdf0f8; border-bottom: 1px solid #f0e4dc; }
  .settings-field { padding: 10px 14px; border-bottom: 1px solid #f5ece8; }
  .settings-field:last-child { border-bottom: none; }
  .settings-field-label { font-family: 'DM Mono', monospace; font-size: 9px; color: #b09088; letter-spacing: 1px; margin-bottom: 6px; display: flex; align-items: center; gap: 6px; }
  .settings-icon { width: 18px; height: 18px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 9px; flex-shrink: 0; }
</style>
</head>
<body>
<div id="app">
  <div class="header">
    <div class="header-top">
      <div>
        <div class="logo-title">Budget</div>
        <div class="logo-sub">PLANNER</div>
      </div>
      <div class="month-nav">
        <button onclick="changeMonth(-1)">‹</button>
        <div class="month-label" id="month-label"></div>
        <button onclick="changeMonth(1)">›</button>
      </div>
    </div>
    <div class="tabs">
      <button class="tab active" data-tab="overview" onclick="switchTab('overview')">OVERVIEW</button>
      <button class="tab" data-tab="add" onclick="openAdd()">ADD</button>
      <button class="tab" data-tab="settings" onclick="openSettings()">SETTINGS</button>
      <div class="saving-badge" id="saving-badge" style="display:none">saving…</div>
    </div>
  </div>
  <div class="content" id="content"></div>
</div>

<script>
// ── Data model ──────────────────────────────────────────────
const STANDALONE = [
  { id: "housing",   label: "Housing",   icon: "⌂", color: "#b5cce8" },
  { id: "groceries", label: "Groceries", icon: "◈", color: "#f5c6d0" },
  { id: "transport", label: "Transport", icon: "◎", color: "#c8e6c9" },
  { id: "health",    label: "Health",    icon: "✦", color: "#f8d7a0" },
  { id: "savings",   label: "Savings",   icon: "△", color: "#b8dfd8" },
  { id: "other",     label: "Other",     icon: "○", color: "#f0d9c0" },
];

const GROUPS = [
  {
    id: "leisure", label: "Leisure", icon: "◇", color: "#d4b8e0",
    subs: [
      { id: "eating-out", label: "Eating Out",       icon: "◈", color: "#e8c4d4" },
      { id: "shopping",   label: "Shopping",          icon: "◇", color: "#d4b8e0" },
      { id: "hobbies",    label: "Personal Hobbies",  icon: "△", color: "#c8c4e8" },
      { id: "travel",     label: "Travel",             icon: "◎", color: "#b8d4e8" },
    ]
  },
  {
    id: "personal-care", label: "Personal Care", icon: "✦", color: "#f5c8d8",
    subs: [
      { id: "salon",      label: "Haircut & Salon",        icon: "✦", color: "#f5c8d8" },
      { id: "skincare",   label: "Skincare & Cosmetics",   icon: "○", color: "#f8d8c8" },
      { id: "toiletries", label: "Toiletries",              icon: "△", color: "#e8f0d8" },
    ]
  }
];

const ALL_CATS = [...STANDALONE, ...GROUPS.flatMap(g => g.subs)];
const MONTHS = ["Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Sep","Oct","Nov","Dec"];
const fmt = n => new Intl.NumberFormat("en-IN",{style:"currency",currency:"INR",maximumFractionDigits:0}).format(n);

function catById(id) { return ALL_CATS.find(c => c.id === id); }

// ── State ────────────────────────────────────────────────────
let currentMonth = new Date().getMonth();
let currentYear  = new Date().getFullYear();
let currentView  = "overview";
let editingId    = null;
let formState    = { type: "expense", amount: "", category: "groceries", note: "" };

// ── Storage ──────────────────────────────────────────────────
function storageKey() { return `budget2-${currentYear}-${currentMonth}`; }

function defaultBudget() {
  const limits = {};
  ALL_CATS.forEach(c => limits[c.id] = 0);
  return { income: 0, limits, transactions: [] };
}

function loadBudget() {
  try {
    const raw = localStorage.getItem(storageKey());
    if (!raw) return defaultBudget();
    const b = JSON.parse(raw);
    // ensure all keys exist
    ALL_CATS.forEach(c => { if (b.limits[c.id] == null) b.limits[c.id] = 0; });
    return b;
  } catch { return defaultBudget(); }
}

function saveBudget(budget) {
  const badge = document.getElementById("saving-badge");
  badge.style.display = "";
  localStorage.setItem(storageKey(), JSON.stringify(budget));
  setTimeout(() => badge.style.display = "none", 700);
}

// ── Navigation ───────────────────────────────────────────────
function changeMonth(dir) {
  currentMonth += dir;
  if (currentMonth < 0)  { currentMonth = 11; currentYear--; }
  if (currentMonth > 11) { currentMonth = 0;  currentYear++; }
  render();
}

function switchTab(tab) {
  currentView = tab;
  document.querySelectorAll(".tab").forEach(t => t.classList.toggle("active", t.dataset.tab === tab));
  render();
}

function openAdd() {
  editingId = null;
  formState = { type: "expense", amount: "", category: "groceries", note: "" };
  switchTab("add");
}

function openEdit(id) {
  const budget = loadBudget();
  const tx = budget.transactions.find(t => t.id === id);
  if (!tx) return;
  editingId = id;
  formState = { type: tx.type, amount: String(tx.amount), category: tx.category || "groceries", note: tx.note || "" };
  switchTab("add");
}

function openSettings() { switchTab("settings"); }

// ── Actions ──────────────────────────────────────────────────
function selectCategory(id) {
  formState.category = id;
  render();
}

function setType(type) {
  formState.type = type;
  render();
}

function deleteTransaction(id) {
  const b = loadBudget();
  b.transactions = b.transactions.filter(t => t.id !== id);
  saveBudget(b);
  render();
}

function saveTransaction() {
  const amountEl = document.getElementById("f-amount");
  const noteEl   = document.getElementById("f-note");
  const amount = parseFloat(amountEl?.value);
  if (!amount || isNaN(amount)) { amountEl?.focus(); return; }
  const note     = noteEl?.value || "";
  const category = formState.type === "income" ? null : formState.category;
  const b = loadBudget();
  if (editingId) {
    b.transactions = b.transactions.map(t =>
      t.id === editingId ? { ...t, type: formState.type, amount, category, note } : t
    );
  } else {
    b.transactions.unshift({ id: Date.now(), type: formState.type, amount, category, note, date: new Date().toISOString() });
  }
  saveBudget(b);
  editingId = null;
  formState = { type: "expense", amount: "", category: "groceries", note: "" };
  switchTab("overview");
}

function deleteEditingEntry() {
  if (!editingId) return;
  deleteTransaction(editingId);
  editingId = null;
  formState = { type: "expense", amount: "", category: "groceries", note: "" };
  switchTab("overview");
}

function cancelForm() {
  editingId = null;
  formState = { type: "expense", amount: "", category: "groceries", note: "" };
  switchTab("overview");
}

function saveSettings() {
  const b = loadBudget();
  b.income = parseFloat(document.getElementById("s-income")?.value) || 0;
  ALL_CATS.forEach(c => {
    const el = document.getElementById("s-" + c.id);
    if (el) b.limits[c.id] = parseFloat(el.value) || 0;
  });
  saveBudget(b);
  switchTab("overview");
}

// ── Helpers ──────────────────────────────────────────────────
function spentOn(expenses, id) {
  return expenses.filter(t => t.category === id).reduce((s,t) => s + t.amount, 0);
}

function progFillColor(cat, pct, over) {
  return over ? "#e8a0a8" : pct > 0.8 ? "#f0c080" : cat.color;
}

function progBarHTML(pct, color, height="5px", marginLeft="0") {
  return `<div class="prog-bar" style="margin-left:${marginLeft};height:${height}">
    <div class="prog-fill" style="width:${Math.min(pct,1)*100}%;background:${color};height:${height}"></div>
  </div>`;
}

// ── Render ───────────────────────────────────────────────────
function render() {
  document.getElementById("month-label").textContent = `${MONTHS[currentMonth]} ${currentYear}`;
  const b = loadBudget();
  const txns    = b.transactions || [];
  const expenses = txns.filter(t => t.type === "expense");
  const incomes  = txns.filter(t => t.type === "income");
  const totalSpent  = expenses.reduce((s,t) => s + t.amount, 0);
  const totalIncome = b.income + incomes.reduce((s,t) => s + t.amount, 0);
  const balance     = totalIncome - totalSpent;
  const content = document.getElementById("content");

  // ── OVERVIEW ────────────────────────────────────────────────
  if (currentView === "overview") {
    // standalone rows (housing, groceries, transport, health, savings)
    const standaloneOrder = ["housing","groceries","transport","health"];
    let standaloneHTML = standaloneOrder.map(id => {
      const cat   = STANDALONE.find(c => c.id === id);
      const spent = spentOn(expenses, id);
      const limit = b.limits[id] || 0;
      const pct   = limit > 0 ? spent/limit : 0;
      const over  = limit > 0 && spent > limit;
      return `
        <div class="cat-row">
          <div class="cat-row-top">
            <div class="cat-name">
              <div class="cat-icon-circle" style="background:${cat.color}55">${cat.icon}</div>
              ${cat.label}
            </div>
            <div class="cat-amount ${over?'over':''}">
              ${fmt(spent)}${limit>0?`<span style="color:#d8c8c0"> / ${fmt(limit)}</span>`:''}
            </div>
          </div>
          ${limit>0 ? progBarHTML(pct, progFillColor(cat,pct,over), "5px", "36px") : ''}
        </div>`;
    }).join("");

    // group blocks
    let groupsHTML = GROUPS.map(g => {
      const groupSpent = g.subs.reduce((s,sub) => s + spentOn(expenses, sub.id), 0);
      const groupLimit = g.subs.reduce((s,sub) => s + (b.limits[sub.id]||0), 0);
      const groupPct   = groupLimit > 0 ? groupSpent/groupLimit : 0;
      const groupOver  = groupLimit > 0 && groupSpent > groupLimit;
      const subsHTML = g.subs.map(sub => {
        const spent = spentOn(expenses, sub.id);
        const limit = b.limits[sub.id] || 0;
        const pct   = limit > 0 ? spent/limit : 0;
        const over  = limit > 0 && spent > limit;
        return `
          <div class="sub-row">
            <div class="sub-name">
              <div class="sub-icon" style="background:${sub.color}55">${sub.icon}</div>
              ${sub.label}
            </div>
            <div class="sub-right">
              <div class="sub-amount ${over?'over':''}">
                ${fmt(spent)}${limit>0?`<span style="color:#d8c8c0"> / ${fmt(limit)}</span>`:''}
              </div>
              ${limit>0?`<div class="sub-prog"><div class="sub-prog-fill" style="width:${Math.min(pct,1)*100}%;background:${progFillColor(sub,pct,over)}"></div></div>`:''}
            </div>
          </div>`;
      }).join("");
      return `
        <div class="group-block">
          <div class="group-header">
            <div class="group-title">
              <div class="group-icon" style="background:${g.color}55">${g.icon}</div>
              ${g.label}
            </div>
            <div class="group-total ${groupOver?'over':''}">
              ${fmt(groupSpent)}${groupLimit>0?`<span style="color:#d8c8c0"> / ${fmt(groupLimit)}</span>`:''}
            </div>
          </div>
          ${groupLimit>0?`<div class="group-prog"><div class="group-prog-fill" style="width:${Math.min(groupPct,1)*100}%;background:${progFillColor(g,groupPct,groupOver)}"></div></div>`:''}
          <div class="sub-rows">${subsHTML}</div>
        </div>`;
    }).join("");

    // savings + other
    const savingsHTML = ["savings","other"].map(id => {
      const cat   = STANDALONE.find(c => c.id === id);
      const spent = spentOn(expenses, id);
      const limit = b.limits[id] || 0;
      const pct   = limit > 0 ? spent/limit : 0;
      const over  = limit > 0 && spent > limit;
      return `
        <div class="cat-row">
          <div class="cat-row-top">
            <div class="cat-name">
              <div class="cat-icon-circle" style="background:${cat.color}55">${cat.icon}</div>
              ${cat.label}
            </div>
            <div class="cat-amount ${over?'over':''}">
              ${fmt(spent)}${limit>0?`<span style="color:#d8c8c0"> / ${fmt(limit)}</span>`:''}
            </div>
          </div>
          ${limit>0 ? progBarHTML(pct, progFillColor(cat,pct,over), "5px", "36px") : ''}
        </div>`;
    }).join("");

    // transactions
    let txHTML = "";
    if (txns.length > 0) {
      txHTML = `<div class="section-label" style="margin-top:8px">RECENT</div>` +
        txns.slice(0,30).map(tx => {
          const cat = catById(tx.category);
          const d   = new Date(tx.date);
          const icon   = tx.type === "income" ? "↑" : (cat?.icon || "○");
          const iconBg = tx.type === "income" ? "#e8f5ec" : ((cat?.color||"#e8d5c8")+"55");
          const amtCol = tx.type === "income" ? "#5a9e70" : "#d07888";
          const sign   = tx.type === "income" ? "+" : "−";
          const label  = tx.note || cat?.label || (tx.type==="income"?"Income":"Entry");
          return `
            <div class="tx-row" onclick="openEdit(${tx.id})">
              <div class="tx-icon" style="background:${iconBg}">${icon}</div>
              <div class="tx-info">
                <div class="tx-note">${label}</div>
                <div class="tx-meta">${d.getDate()} ${MONTHS[d.getMonth()]} · tap to edit</div>
              </div>
              <div class="tx-amount" style="color:${amtCol}">${sign}${fmt(tx.amount)}</div>
              <button class="tx-del" onclick="event.stopPropagation();deleteTransaction(${tx.id})">×</button>
            </div>`;
        }).join("");
    } else {
      txHTML = `<div class="empty">
        <div class="empty-title">No entries yet</div>
        <div class="empty-sub">TAP ADD TO BEGIN</div>
      </div>`;
    }

    content.innerHTML = `
      <div class="summary-grid">
        <div class="summary-card" style="background:#e8f5ec">
          <div class="summary-label">INCOME</div>
          <div class="summary-value" style="color:#5a9e70">${fmt(totalIncome)}</div>
        </div>
        <div class="summary-card" style="background:#fdeef2">
          <div class="summary-label">SPENT</div>
          <div class="summary-value" style="color:#d07888">${fmt(totalSpent)}</div>
        </div>
        <div class="summary-card" style="background:${balance>=0?'#fef5e8':'#fdeef2'}">
          <div class="summary-label">LEFT</div>
          <div class="summary-value" style="color:${balance>=0?'#c0804a':'#d07888'}">${fmt(balance)}</div>
        </div>
      </div>
      <div class="section-label">CATEGORIES</div>
      ${standaloneHTML}
      ${groupsHTML}
      ${savingsHTML}
      ${txHTML}`;
  }

  // ── ADD / EDIT ───────────────────────────────────────────────
  else if (currentView === "add") {
    // Category picker grouped
    const pickerHTML = formState.type === "expense" ? `
      <div class="field">
        <div class="field-label">CATEGORY</div>
        <div class="cat-picker">
          <div class="cat-group-label">GENERAL</div>
          ${STANDALONE.map(c => `
            <div class="cat-option ${formState.category===c.id?'selected':''}" onclick="selectCategory('${c.id}')">
              <div class="cat-option-icon" style="background:${c.color}55">${c.icon}</div>
              <div class="cat-option-label">${c.label}</div>
              ${formState.category===c.id?'<div class="check">✓</div>':''}
            </div>`).join('')}
          ${GROUPS.map(g => `
            <div class="cat-group-label">${g.label.toUpperCase()}</div>
            ${g.subs.map(sub => `
              <div class="cat-option ${formState.category===sub.id?'selected':''}" onclick="selectCategory('${sub.id}')">
                <div class="cat-option-icon" style="background:${sub.color}55">${sub.icon}</div>
                <div class="cat-option-label">${sub.label}</div>
                ${formState.category===sub.id?'<div class="check">✓</div>':''}
              </div>`).join('')}`).join('')}
        </div>
      </div>` : '';

    content.innerHTML = `
      <div class="panel">
        <div class="panel-title">
          <h2>${editingId ? "Edit entry" : "New entry"}</h2>
          ${editingId ? '<span class="edit-badge">EDITING</span>' : ''}
        </div>
        <div class="field">
          <div class="type-toggle">
            <button class="type-opt ${formState.type==='expense'?'sel-expense':''}" onclick="setType('expense')">EXPENSE</button>
            <button class="type-opt ${formState.type==='income'?'sel-income':''}" onclick="setType('income')">INCOME</button>
          </div>
        </div>
        <div class="field">
          <div class="field-label">AMOUNT (₹)</div>
          <input id="f-amount" class="input-field" type="number" placeholder="0" value="${formState.amount}" oninput="formState.amount=this.value"/>
        </div>
        ${pickerHTML}
        <div class="field">
          <div class="field-label">NOTE (optional)</div>
          <input id="f-note" class="input-field" placeholder="e.g. Zomato order" value="${formState.note}" oninput="formState.note=this.value"/>
        </div>
        <div class="btn-row">
          <button class="ghost-btn" onclick="cancelForm()">CANCEL</button>
          <button class="primary-btn" onclick="saveTransaction()">${editingId?"SAVE CHANGES":"ADD ENTRY"}</button>
        </div>
        ${editingId?`<button class="delete-link" onclick="deleteEditingEntry()">delete this entry</button>`:''}
      </div>`;
  }

  // ── SETTINGS ─────────────────────────────────────────────────
  else if (currentView === "settings") {
    const standaloneFields = (ids) => ids.map(id => {
      const cat = STANDALONE.find(c => c.id === id);
      return `
        <div class="settings-field">
          <div class="settings-field-label">
            <div class="settings-icon" style="background:${cat.color}55">${cat.icon}</div>
            ${cat.label}
          </div>
          <input id="s-${cat.id}" class="input-field" type="number" placeholder="0 = no limit" value="${b.limits[cat.id]||''}"/>
        </div>`;
    }).join("");

    const groupFields = GROUPS.map(g => `
      <div class="settings-group">
        <div class="settings-group-label">${g.label.toUpperCase()}</div>
        ${g.subs.map(sub => `
          <div class="settings-field">
            <div class="settings-field-label">
              <div class="settings-icon" style="background:${sub.color}55">${sub.icon}</div>
              ${sub.label}
            </div>
            <input id="s-${sub.id}" class="input-field" type="number" placeholder="0 = no limit" value="${b.limits[sub.id]||''}"/>
          </div>`).join('')}
      </div>`).join("");

    content.innerHTML = `
      <div class="panel">
        <div class="panel-title"><h2>Monthly setup</h2></div>
        <div class="settings-group">
          <div class="settings-group-label">INCOME</div>
          <div class="settings-field">
            <div class="settings-field-label">Base Income (₹)</div>
            <input id="s-income" class="input-field" type="number" placeholder="0" value="${b.income||''}"/>
          </div>
        </div>
        <div class="settings-group">
          <div class="settings-group-label">GENERAL</div>
          ${standaloneFields(["housing","groceries","transport","health"])}
        </div>
        ${groupFields}
        <div class="settings-group">
          <div class="settings-group-label">OTHER</div>
          ${standaloneFields(["savings","other"])}
        </div>
        <div class="btn-row">
          <button class="ghost-btn" onclick="switchTab('overview')">CANCEL</button>
          <button class="primary-btn" onclick="saveSettings()">SAVE</button>
        </div>
      </div>`;
  }
}

render();
</script>
</body>
</html>
