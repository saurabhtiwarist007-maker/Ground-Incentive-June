<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Ground Team · Incentive League — June</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@500;600;700;800&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
:root{
  --field:#143A28; --field2:#1C5238; --gold:#F2A516; --gold-deep:#B9740A;
  --sprout:#74B017; --warm:#D7D2C4; --clay:#D1495B; --paper:#FBF7EC;
  --panel:#FFFFFF; --ink:#15211A; --muted:#6E776B; --line:#ECE6D7;
}
*{box-sizing:border-box;margin:0;padding:0}
html{-webkit-text-size-adjust:100%}
body{font-family:Inter,system-ui,sans-serif;background:var(--paper);color:var(--ink);
  line-height:1.45;-webkit-font-smoothing:antialiased;padding-bottom:48px}
.wrap{max-width:520px;margin:0 auto}
.num{font-family:"Barlow Condensed",sans-serif;font-variant-numeric:tabular-nums;letter-spacing:.01em}

/* ---------- HERO ---------- */
.hero{background:
   radial-gradient(120% 90% at 85% -10%, rgba(242,165,22,.30), transparent 55%),
   linear-gradient(165deg,var(--field2),var(--field) 70%);
  color:#fff;padding:26px 22px 30px;position:relative;overflow:hidden}
.hero::after{content:"";position:absolute;left:0;right:0;bottom:0;height:6px;
  background:linear-gradient(90deg,var(--sprout),var(--gold))}
.eyebrow{font-family:"Barlow Condensed";text-transform:uppercase;letter-spacing:.18em;
  font-weight:600;font-size:13px;color:#CDEBC6;display:flex;align-items:center;gap:8px}
.eyebrow b{color:var(--gold);font-weight:700}
.hero h1{font-family:"Barlow Condensed";font-weight:800;font-size:31px;line-height:1.02;
  margin:6px 0 2px;text-transform:uppercase;letter-spacing:.01em}
.hero .sub{color:#BFE0B8;font-size:13.5px;font-weight:500}
.pot{margin-top:20px;display:flex;align-items:flex-end;gap:10px}
.pot .rs{font-family:"Barlow Condensed";font-weight:700;font-size:30px;color:var(--gold);line-height:1}
.pot .big{font-family:"Barlow Condensed";font-weight:800;font-size:58px;color:var(--gold);
  line-height:.85;text-shadow:0 2px 14px rgba(242,165,22,.30)}
.pot .cap{color:#CDEBC6;font-size:12.5px;font-weight:600;text-transform:uppercase;
  letter-spacing:.08em;padding-bottom:7px}
.stats{margin-top:18px;display:grid;grid-template-columns:repeat(3,1fr);gap:1px;
  background:rgba(255,255,255,.16);border-radius:13px;overflow:hidden}
.stat{background:rgba(8,28,18,.30);padding:11px 12px}
.stat .v{font-family:"Barlow Condensed";font-weight:700;font-size:25px;color:#fff;line-height:1}
.stat .l{font-size:10.5px;color:#B9DDB2;text-transform:uppercase;letter-spacing:.06em;
  margin-top:3px;font-weight:600}
.stat .v small{font-size:14px;color:var(--gold)}

/* ---------- CONTROLS ---------- */
.bar{position:sticky;top:0;z-index:20;background:var(--paper);
  padding:12px 14px;border-bottom:1px solid var(--line)}
.search{width:100%;border:1.5px solid var(--line);background:#fff;border-radius:12px;
  padding:11px 13px 11px 38px;font-size:15px;font-family:inherit;color:var(--ink);
  background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='18' height='18' viewBox='0 0 24 24' fill='none' stroke='%236E776B' stroke-width='2.2' stroke-linecap='round'%3E%3Ccircle cx='11' cy='11' r='7'/%3E%3Cpath d='m21 21-4.3-4.3'/%3E%3C/svg%3E");
  background-repeat:no-repeat;background-position:13px center}
.search:focus{outline:none;border-color:var(--sprout);box-shadow:0 0 0 3px rgba(116,176,23,.15)}
.seg{display:flex;gap:6px;margin-top:10px}
.seg button{flex:1;border:1.5px solid var(--line);background:#fff;border-radius:10px;
  padding:8px 6px;font-family:"Barlow Condensed";font-weight:600;font-size:14px;
  text-transform:uppercase;letter-spacing:.04em;color:var(--muted);cursor:pointer}
.seg button[aria-pressed=true]{background:var(--field);border-color:var(--field);color:#fff}

/* ---------- VERGE STRIP ---------- */
.section-h{display:flex;align-items:baseline;justify-content:space-between;
  padding:20px 16px 9px}
.section-h h2{font-family:"Barlow Condensed";font-weight:700;font-size:19px;
  text-transform:uppercase;letter-spacing:.04em}
.section-h span{font-size:11.5px;color:var(--muted);font-weight:600}
.verge{display:flex;gap:10px;overflow-x:auto;padding:2px 16px 6px;scroll-snap-type:x mandatory;
  -webkit-overflow-scrolling:touch}
.verge::-webkit-scrollbar{display:none}
.vcard{scroll-snap-align:start;flex:0 0 158px;border-radius:15px;padding:13px 14px;
  background:linear-gradient(160deg,#fff,#FFF6E3);border:1.5px solid #F3E3BC;
  box-shadow:0 4px 14px rgba(185,116,10,.07)}
.vcard .nm{font-weight:700;font-size:13.5px;white-space:nowrap;overflow:hidden;
  text-overflow:ellipsis}
.vcard .togo{font-family:"Barlow Condensed";font-weight:800;font-size:30px;color:var(--clay);
  line-height:.95;margin-top:7px}
.vcard .togo small{font-size:13px;color:var(--muted);font-weight:600;letter-spacing:0}
.vcard .unl{margin-top:6px;font-size:11.5px;color:var(--gold-deep);font-weight:700}
.vcard .unl b{font-family:"Barlow Condensed";font-size:15px}

/* ---------- LEADERBOARD ---------- */
.board{padding:0 12px}
.row{display:grid;grid-template-columns:34px 1fr auto;gap:11px;align-items:center;
  background:#fff;border:1px solid var(--line);border-radius:15px;padding:12px 13px;
  margin-bottom:9px;cursor:pointer;transition:border-color .15s}
.row:hover{border-color:#D9D2C0}
.row.me{border-color:var(--gold);box-shadow:0 0 0 2px rgba(242,165,22,.18)}
.rank{font-family:"Barlow Condensed";font-weight:800;font-size:22px;color:var(--muted);
  text-align:center;line-height:1}
.row.t1 .rank,.row.t2 .rank,.row.t3 .rank{width:32px;height:32px;border-radius:50%;
  display:flex;align-items:center;justify-content:center;color:#fff;font-size:17px;margin:0 auto}
.row.t1 .rank{background:linear-gradient(150deg,#FFD66B,var(--gold-deep))}
.row.t2 .rank{background:linear-gradient(150deg,#D7DCE0,#9AA4AC)}
.row.t3 .rank{background:linear-gradient(150deg,#E6A878,#B06A38)}
.mid{min-width:0}
.mid .nm{font-weight:700;font-size:15px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
.mid .ords{font-size:11.5px;color:var(--muted);font-weight:600;margin-top:1px}
.mid .ords b{color:var(--field2);font-family:"Barlow Condensed";font-size:14px}
/* unlock meter */
.meter{position:relative;height:9px;border-radius:6px;background:var(--warm);margin-top:8px;overflow:hidden}
.meter .warm{position:absolute;left:0;top:0;bottom:0;width:20%;
  background:repeating-linear-gradient(135deg,#CFC9BA,#CFC9BA 4px,#C5BFAF 4px,#C5BFAF 8px)}
.meter .fill{position:absolute;left:0;top:0;bottom:0;width:0;border-radius:6px;
  background:linear-gradient(90deg,var(--sprout),#9ACD2E);transition:width 1.1s cubic-bezier(.2,.8,.2,1)}
.meter.done .fill{background:linear-gradient(90deg,var(--gold),#FFCF5C)}
.meter .tick{position:absolute;top:-3px;bottom:-3px;width:2px;background:#fff;
  box-shadow:0 0 0 1px rgba(0,0,0,.06)}
.right{text-align:right;min-width:78px}
.amt{font-family:"Barlow Condensed";font-weight:800;font-size:25px;color:var(--gold-deep);line-height:.9}
.amt .rs{font-size:15px;color:var(--gold-deep);font-weight:700}
.amt.zero{color:#BBB6A6}
.chip{display:inline-block;margin-top:5px;font-size:10.5px;font-weight:700;
  padding:3px 8px;border-radius:20px;letter-spacing:.02em}
.chip.gap{background:#FBE9EC;color:var(--clay)}
.chip.gap b{font-family:"Barlow Condensed";font-size:12px}
.chip.on{background:#FEF1D6;color:var(--gold-deep)}

/* expand */
.exp{grid-column:1/-1;overflow:hidden;max-height:0;transition:max-height .3s ease}
.row.open .exp{max-height:160px}
.exp-in{border-top:1px dashed var(--line);margin-top:11px;padding-top:11px;
  display:flex;align-items:flex-end;justify-content:space-between;gap:12px}
.exp-in .lab{font-size:11px;color:var(--muted);font-weight:600}
.exp-in .lab b{color:var(--ink);font-weight:700;display:block;font-size:13px}
.spark{flex:1;display:flex;align-items:flex-end;gap:3px;height:42px}
.spark i{flex:1;background:var(--sprout);border-radius:2px 2px 0 0;min-height:2px;opacity:.85}
.spark i.z{background:#E3DECF}
.empty{text-align:center;padding:30px 16px;color:var(--muted);font-size:14px}

/* legend */
.legend{margin:26px 16px 8px;background:#fff;border:1px solid var(--line);
  border-radius:16px;padding:16px 17px}
.legend h3{font-family:"Barlow Condensed";font-weight:700;font-size:17px;
  text-transform:uppercase;letter-spacing:.04em;margin-bottom:11px}
.legend .lr{display:flex;gap:11px;align-items:flex-start;font-size:13px;
  color:#43493F;margin-bottom:10px}
.legend .lr:last-child{margin-bottom:0}
.dot{flex:0 0 11px;height:11px;border-radius:50%;margin-top:4px}
.legend b{color:var(--ink)}
.foot{text-align:center;color:var(--muted);font-size:11.5px;padding:18px 16px 6px}
.foot b{color:var(--field2)}
@media (prefers-reduced-motion:reduce){*{transition:none!important;animation:none!important}}
</style>
</head>
<body>
<div class="wrap">

  <header class="hero">
    <div class="eyebrow">Ground Team · <b>Incentive League</b></div>
    <h1>The Climb to ₹</h1>
    <div class="sub">June 2026 · every order takes you higher</div>
    <div class="pot">
      <span class="big" id="pot">0</span>
      <span class="cap">on the table<br>this month</span>
    </div>
    <div class="stats">
      <div class="stat"><div class="v num" id="s-ord">0</div><div class="l">orders so far</div></div>
      <div class="stat"><div class="v num" id="s-ag">0</div><div class="l">in the race</div></div>
      <div class="stat"><div class="v num" id="s-days">0</div><div class="l">days left</div></div>
    </div>
  </header>

  <div class="bar">
    <input class="search" id="q" placeholder="Find your name…" autocomplete="off">
    <div class="seg" id="seg">
      <button data-k="tentative" aria-pressed="true">₹ to earn</button>
      <button data-k="orders" aria-pressed="false">Orders</button>
      <button data-k="gap" aria-pressed="false">Closest</button>
    </div>
  </div>

  <div id="vergeWrap">
    <div class="section-h"><h2>On the verge 🔥</h2><span>nearest to unlocking</span></div>
    <div class="verge" id="verge"></div>
  </div>

  <div class="section-h" id="boardH"><h2>Leaderboard</h2><span id="boardSub"></span></div>
  <div class="board" id="board"></div>

  <div class="legend">
    <h3>How your incentive works</h3>
    <div class="lr"><span class="dot" style="background:var(--warm)"></span>
      <div>Your <b>first 5 orders</b> are the warm-up — no payout yet.</div></div>
    <div class="lr"><span class="dot" style="background:var(--sprout)"></span>
      <div>From order 6 onward you start <b>building incentive</b> (only orders above ₹2,000 count).</div></div>
    <div class="lr"><span class="dot" style="background:var(--gold)"></span>
      <div>Cross <b>25 orders</b> and it all <b>unlocks</b> — your tentative amount becomes payable.</div></div>
    <div class="lr"><span class="dot" style="background:var(--clay)"></span>
      <div>Below 25? The red number is how many orders you still need.</div></div>
  </div>
  <div class="foot">Updated as of <b>9 June 2026</b> · figures are tentative and shown before deductions (zero-order days, RTO, active-day rules still apply).</div>
</div>

<script id="DATA" type="application/json">{"eligibility": 25, "threshold": 5, "totals": {"agents": 91, "active": 91, "orders": 498, "tentative": 98150, "earned": 0, "eligible_ct": 0, "last_day": 9}, "agents": [{"emp": "REP-2017", "name": "Harikesh", "asm": 0, "orders": 4, "tentative": 0, "earned": 0, "eligible": false, "gap": 21, "daily": [0, 0, 0, 1, 1, 1, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "13 Feb 2026"}, {"emp": "REP-2503", "name": "Arjun tiwari", "asm": 0, "orders": 12, "tentative": 5050, "earned": 0, "eligible": false, "gap": 13, "daily": [3, 1, 2, 2, 4, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "06 Apr 2026"}, {"emp": "REP-2724", "name": "Aman Kumar Dhiman", "asm": 0, "orders": 2, "tentative": 400, "earned": 0, "eligible": false, "gap": 23, "daily": [0, 1, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "22 May 2026"}, {"emp": "REP-1798", "name": "ADARSH Kumar Awasthi", "asm": 0, "orders": 11, "tentative": 4050, "earned": 0, "eligible": false, "gap": 14, "daily": [0, 1, 0, 2, 1, 2, 0, 2, 3, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "14 Nov 2025"}, {"emp": "REP-2024", "name": "Gourab das", "asm": 0, "orders": 23, "tentative": 18000, "earned": 0, "eligible": false, "gap": 2, "daily": [0, 3, 2, 3, 4, 6, 0, 5, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "13 Feb 2026"}, {"emp": "REP-2636", "name": "Sanjay Kori", "asm": 0, "orders": 1, "tentative": 0, "earned": 0, "eligible": false, "gap": 24, "daily": [0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "08 May 2026"}, {"emp": "REP-2538", "name": "Satyam Yadav", "asm": 0, "orders": 10, "tentative": 1300, "earned": 0, "eligible": false, "gap": 15, "daily": [0, 1, 2, 2, 1, 1, 0, 2, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "14 Apr 2026"}, {"emp": "REP-2777", "name": "Govind Rathore", "asm": 0, "orders": 1, "tentative": 200, "earned": 0, "eligible": false, "gap": 24, "daily": [0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "29 May 2026"}, {"emp": "REP-0871", "name": "Brijesh2", "asm": 0, "orders": 8, "tentative": 3000, "earned": 0, "eligible": false, "gap": 17, "daily": [0, 0, 1, 0, 3, 0, 0, 1, 3, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "20 May 2025"}, {"emp": "REP-2600", "name": "Kuljeet Rajpoot", "asm": 0, "orders": 9, "tentative": 1100, "earned": 0, "eligible": false, "gap": 16, "daily": [1, 2, 2, 1, 0, 1, 0, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "01 May 2026"}, {"emp": "REP-1612", "name": "Jitendra Kumar", "asm": 0, "orders": 5, "tentative": 0, "earned": 0, "eligible": false, "gap": 20, "daily": [0, 1, 1, 2, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "07 Jan 2025"}, {"emp": "REP-2515", "name": "Shekhar kumar", "asm": 0, "orders": 5, "tentative": 0, "earned": 0, "eligible": false, "gap": 20, "daily": [1, 1, 0, 0, 0, 0, 0, 1, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "07 Apr 2026"}, {"emp": "REP-2076", "name": "Jawahar singh", "asm": 0, "orders": 8, "tentative": 600, "earned": 0, "eligible": false, "gap": 17, "daily": [2, 2, 1, 0, 1, 1, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "17 Feb 2026"}, {"emp": "REP-2510", "name": "Mohit Singh Thakur", "asm": 0, "orders": 6, "tentative": 200, "earned": 0, "eligible": false, "gap": 19, "daily": [1, 0, 1, 1, 0, 1, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "07 Apr 2026"}, {"emp": "REP-2622", "name": "Radhacharan gurjar", "asm": 0, "orders": 8, "tentative": 3000, "earned": 0, "eligible": false, "gap": 17, "daily": [1, 0, 1, 1, 0, 0, 0, 1, 4, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "05 May 2026"}, {"emp": "REP-2624", "name": "Vishnu Gurjar", "asm": 0, "orders": 4, "tentative": 0, "earned": 0, "eligible": false, "gap": 21, "daily": [0, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "08 May 2026"}, {"emp": "A00724", "name": "Anil Kumar", "asm": 0, "orders": 4, "tentative": 0, "earned": 0, "eligible": false, "gap": 21, "daily": [0, 1, 0, 1, 0, 1, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "08 Oct 2022"}, {"emp": "REP-0043", "name": "Abhishek Kumar 2", "asm": 0, "orders": 5, "tentative": 0, "earned": 0, "eligible": false, "gap": 20, "daily": [0, 0, 0, 1, 0, 1, 0, 0, 3, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "20 Jan 2025"}, {"emp": "REP-2652", "name": "Mahendra Prajapati", "asm": 0, "orders": 10, "tentative": 2200, "earned": 0, "eligible": false, "gap": 15, "daily": [0, 3, 1, 1, 2, 1, 0, 0, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "12 May 2026"}, {"emp": "REP-2301", "name": "Udit", "asm": 0, "orders": 8, "tentative": 900, "earned": 0, "eligible": false, "gap": 17, "daily": [2, 1, 1, 0, 1, 1, 0, 0, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "16 Mar 2026"}, {"emp": "REP-2739", "name": "Mithelesh vyas", "asm": 0, "orders": 7, "tentative": 1400, "earned": 0, "eligible": false, "gap": 18, "daily": [1, 0, 0, 1, 2, 1, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "22 May 2026"}, {"emp": "A00731", "name": "Rohit Kumar", "asm": 0, "orders": 8, "tentative": 750, "earned": 0, "eligible": false, "gap": 17, "daily": [1, 0, 3, 2, 1, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "24 Mar 2022"}, {"emp": "REP-2431", "name": "lal singh", "asm": 0, "orders": 8, "tentative": 1050, "earned": 0, "eligible": false, "gap": 17, "daily": [0, 1, 1, 0, 2, 2, 0, 0, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "24 Mar 2026"}, {"emp": "REP-2507", "name": "Nihal Ravindra beldar", "asm": 0, "orders": 10, "tentative": 3400, "earned": 0, "eligible": false, "gap": 15, "daily": [1, 2, 0, 0, 2, 1, 0, 3, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "07 Apr 2026"}, {"emp": "REP-0005", "name": "Brijesh Kumar", "asm": 0, "orders": 9, "tentative": 1100, "earned": 0, "eligible": false, "gap": 16, "daily": [0, 2, 2, 1, 1, 0, 0, 1, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "02 Jan 2025"}, {"emp": "REP-1504", "name": "Rahul Kumar", "asm": 0, "orders": 7, "tentative": 400, "earned": 0, "eligible": false, "gap": 18, "daily": [0, 1, 0, 1, 1, 2, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "23 Jun 2025"}, {"emp": "REP-2066", "name": "Piyush Kumar", "asm": 0, "orders": 4, "tentative": 0, "earned": 0, "eligible": false, "gap": 21, "daily": [1, 0, 1, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "17 Feb 2026"}, {"emp": "REP-1299", "name": "Rajneekant", "asm": 0, "orders": 4, "tentative": 0, "earned": 0, "eligible": false, "gap": 21, "daily": [0, 0, 1, 0, 1, 1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "12 Jun 2025"}, {"emp": "REP-2781", "name": "Tarachand Sharma", "asm": 0, "orders": 3, "tentative": 600, "earned": 0, "eligible": false, "gap": 22, "daily": [0, 0, 0, 0, 0, 0, 0, 0, 3, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "29 May 2026"}, {"emp": "REP-2295", "name": "Ritesh vithal pable", "asm": 0, "orders": 11, "tentative": 1800, "earned": 0, "eligible": false, "gap": 14, "daily": [0, 1, 2, 2, 2, 1, 0, 2, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "16 Mar 2026"}, {"emp": "REP-2430", "name": "Amit Kumar Pandey", "asm": 0, "orders": 2, "tentative": 0, "earned": 0, "eligible": false, "gap": 23, "daily": [0, 1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "24 Mar 2026"}, {"emp": "REP-2479", "name": "Hemant kumar kulshrestha", "asm": 0, "orders": 7, "tentative": 700, "earned": 0, "eligible": false, "gap": 18, "daily": [1, 1, 1, 1, 0, 1, 0, 0, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "27 Mar 2026"}, {"emp": "REP-2573", "name": "VAIBHAV KUMAR", "asm": 0, "orders": 9, "tentative": 1100, "earned": 0, "eligible": false, "gap": 16, "daily": [0, 0, 0, 4, 1, 1, 0, 1, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "24 Apr 2026"}, {"emp": "REP-1758", "name": "Mithilesh Kumar", "asm": 0, "orders": 2, "tentative": 0, "earned": 0, "eligible": false, "gap": 23, "daily": [0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "17 Oct 2025"}, {"emp": "REP-2528", "name": "Pawan bharatrao", "asm": 0, "orders": 11, "tentative": 1800, "earned": 0, "eligible": false, "gap": 14, "daily": [1, 1, 2, 1, 2, 1, 0, 2, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "10 Apr 2026"}, {"emp": "REP-2277", "name": "Rahul dnyneshwar talekar", "asm": 0, "orders": 10, "tentative": 1600, "earned": 0, "eligible": false, "gap": 15, "daily": [1, 1, 2, 1, 2, 0, 0, 1, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "16 Mar 2026"}, {"emp": "REP-1989", "name": "Himanshu", "asm": 0, "orders": 5, "tentative": 0, "earned": 0, "eligible": false, "gap": 20, "daily": [0, 0, 1, 1, 0, 2, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "06 Feb 2026"}, {"emp": "REP-2013", "name": "Bhimsen", "asm": 0, "orders": 8, "tentative": 750, "earned": 0, "eligible": false, "gap": 17, "daily": [0, 1, 1, 1, 1, 2, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "13 Feb 2026"}, {"emp": "REP-2316", "name": "Ahemad Raza Khan", "asm": 0, "orders": 6, "tentative": 200, "earned": 0, "eligible": false, "gap": 19, "daily": [0, 1, 0, 2, 1, 1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "20 Mar 2026"}, {"emp": "A01066", "name": "Abhishek Tiwari", "asm": 0, "orders": 4, "tentative": 0, "earned": 0, "eligible": false, "gap": 21, "daily": [0, 1, 0, 0, 1, 1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "25 Jun 2024"}, {"emp": "REP-2216", "name": "Mohd Jawed Mohd Firoj Deshmukh", "asm": 0, "orders": 6, "tentative": 200, "earned": 0, "eligible": false, "gap": 19, "daily": [2, 1, 1, 1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "13 Mar 2026"}, {"emp": "REP-1897", "name": "Amit Kumar", "asm": 0, "orders": 7, "tentative": 400, "earned": 0, "eligible": false, "gap": 18, "daily": [1, 1, 0, 1, 1, 1, 1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "05 Jan 2026"}, {"emp": "REP-2187", "name": "Jagesh Kumar", "asm": 0, "orders": 6, "tentative": 1000, "earned": 0, "eligible": false, "gap": 19, "daily": [0, 0, 1, 1, 1, 3, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "09 Mar 2026"}, {"emp": "REP-2525", "name": "Durgesh Kumar Vishwakarma", "asm": 0, "orders": 6, "tentative": 200, "earned": 0, "eligible": false, "gap": 19, "daily": [1, 1, 0, 1, 1, 1, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "10 Apr 2026"}, {"emp": "REP-2598", "name": "Pankaj savera", "asm": 0, "orders": 5, "tentative": 0, "earned": 0, "eligible": false, "gap": 20, "daily": [1, 1, 0, 0, 0, 1, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "01 May 2026"}, {"emp": "REP-2496", "name": "Ravi", "asm": 0, "orders": 5, "tentative": 0, "earned": 0, "eligible": false, "gap": 20, "daily": [1, 0, 0, 1, 2, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "03 Apr 2026"}, {"emp": "REP-2752", "name": "Ashutosa Sethi", "asm": 0, "orders": 1, "tentative": 200, "earned": 0, "eligible": false, "gap": 24, "daily": [1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "26 May 2026"}, {"emp": "REP-2225", "name": "Ankush kumar", "asm": 0, "orders": 18, "tentative": 9600, "earned": 0, "eligible": false, "gap": 7, "daily": [2, 2, 3, 3, 2, 1, 0, 2, 3, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "13 Mar 2026"}, {"emp": "REP-2736", "name": "PANKAJ KUMAR", "asm": 0, "orders": 4, "tentative": 800, "earned": 0, "eligible": false, "gap": 21, "daily": [1, 1, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "22 May 2026"}, {"emp": "REP-2470", "name": "subinoy das", "asm": 0, "orders": 10, "tentative": 3400, "earned": 0, "eligible": false, "gap": 15, "daily": [2, 0, 2, 1, 1, 3, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "24 Mar 2026"}, {"emp": "REP-2042", "name": "Deepak", "asm": 0, "orders": 5, "tentative": 0, "earned": 0, "eligible": false, "gap": 20, "daily": [0, 0, 1, 1, 1, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "17 Feb 2026"}, {"emp": "REP-2723", "name": "Lokendra singh rajput", "asm": 0, "orders": 4, "tentative": 800, "earned": 0, "eligible": false, "gap": 21, "daily": [1, 1, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "22 May 2026"}, {"emp": "REP-1661", "name": "Pritam Prabhat", "asm": 0, "orders": 5, "tentative": 0, "earned": 0, "eligible": false, "gap": 20, "daily": [1, 0, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "18 Aug 2025"}, {"emp": "REP-2587", "name": "Abhinav Srivastav", "asm": 0, "orders": 7, "tentative": 400, "earned": 0, "eligible": false, "gap": 18, "daily": [1, 1, 0, 2, 1, 1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "28 Apr 2026"}, {"emp": "REP-2595", "name": "Krishan Kant Dandotiya", "asm": 0, "orders": 13, "tentative": 6400, "earned": 0, "eligible": false, "gap": 12, "daily": [4, 1, 1, 3, 1, 0, 0, 3, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "01 May 2026"}, {"emp": "A00715", "name": "Alok Kumar Tripathi", "asm": 0, "orders": 12, "tentative": 7000, "earned": 0, "eligible": false, "gap": 13, "daily": [0, 0, 0, 0, 4, 4, 0, 0, 4, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "06 Apr 2022"}, {"emp": "REP-1803", "name": "Satyam Patel", "asm": 0, "orders": 5, "tentative": 0, "earned": 0, "eligible": false, "gap": 20, "daily": [0, 0, 1, 3, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "20 Nov 2025"}, {"emp": "REP-2154", "name": "mohd imran alam", "asm": 0, "orders": 2, "tentative": 0, "earned": 0, "eligible": false, "gap": 23, "daily": [0, 0, 0, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "02 Mar 2026"}, {"emp": "REP-0209", "name": "Pankaj Kumar Bairagi", "asm": 0, "orders": 3, "tentative": 0, "earned": 0, "eligible": false, "gap": 22, "daily": [0, 0, 0, 1, 0, 1, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "24 Feb 2025"}, {"emp": "REP-2038", "name": "Devi Das", "asm": 0, "orders": 7, "tentative": 700, "earned": 0, "eligible": false, "gap": 18, "daily": [1, 0, 1, 1, 0, 2, 0, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "13 Feb 2026"}, {"emp": "REP-2052", "name": "Andeep kumar", "asm": 0, "orders": 3, "tentative": 0, "earned": 0, "eligible": false, "gap": 22, "daily": [0, 1, 0, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "13 Feb 2026"}, {"emp": "REP-1816", "name": "Alok Singh Tomar", "asm": 0, "orders": 4, "tentative": 0, "earned": 0, "eligible": false, "gap": 21, "daily": [1, 2, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "28 Nov 2024"}, {"emp": "REP-2633", "name": "AKASH GARDIA", "asm": 0, "orders": 2, "tentative": 0, "earned": 0, "eligible": false, "gap": 23, "daily": [1, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "08 May 2026"}, {"emp": "REP-2542", "name": "Sachin", "asm": 0, "orders": 1, "tentative": 0, "earned": 0, "eligible": false, "gap": 24, "daily": [0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "14 Apr 2026"}, {"emp": "REP-2008", "name": "Ratnesh Mishra", "asm": 0, "orders": 15, "tentative": 6600, "earned": 0, "eligible": false, "gap": 10, "daily": [2, 1, 1, 3, 2, 3, 0, 1, 2, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "06 Feb 2026"}, {"emp": "REP-2750", "name": "Shahriyar alam", "asm": 0, "orders": 1, "tentative": 200, "earned": 0, "eligible": false, "gap": 24, "daily": [1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "26 May 2026"}, {"emp": "REP-1855", "name": "Kriti Nandan Kumar Lal", "asm": 0, "orders": 1, "tentative": 0, "earned": 0, "eligible": false, "gap": 24, "daily": [1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "26 Dec 2025"}, {"emp": "REP-2718", "name": "Surya Tarun Mallick", "asm": 0, "orders": 2, "tentative": 400, "earned": 0, "eligible": false, "gap": 23, "daily": [1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "22 May 2026"}, {"emp": "REP-2764", "name": "Khemraj choudhary", "asm": 0, "orders": 5, "tentative": 1000, "earned": 0, "eligible": false, "gap": 20, "daily": [1, 1, 0, 1, 0, 1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "26 May 2026"}, {"emp": "REP-2606", "name": "DEV RAJ", "asm": 0, "orders": 4, "tentative": 0, "earned": 0, "eligible": false, "gap": 21, "daily": [1, 1, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "01 May 2026"}, {"emp": "REP-2139", "name": "Bablu Kumar yadav", "asm": 0, "orders": 3, "tentative": 0, "earned": 0, "eligible": false, "gap": 22, "daily": [1, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "27 Feb 2026"}, {"emp": "REP-2651", "name": "Sadab khan", "asm": 0, "orders": 2, "tentative": 200, "earned": 0, "eligible": false, "gap": 23, "daily": [0, 1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "12 May 2026"}, {"emp": "REP-2229", "name": "Dinesh", "asm": 0, "orders": 5, "tentative": 0, "earned": 0, "eligible": false, "gap": 20, "daily": [0, 1, 1, 0, 1, 1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "13 Mar 2026"}, {"emp": "REP-2647", "name": "Debiprasad samal", "asm": 0, "orders": 2, "tentative": 200, "earned": 0, "eligible": false, "gap": 23, "daily": [1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "12 May 2026"}, {"emp": "REP-2487", "name": "Ajeet Kumar Mehra", "asm": 0, "orders": 3, "tentative": 0, "earned": 0, "eligible": false, "gap": 22, "daily": [0, 0, 1, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "31 Mar 2026"}, {"emp": "A00716", "name": "Ashwani Jaiswal", "asm": 0, "orders": 3, "tentative": 0, "earned": 0, "eligible": false, "gap": 22, "daily": [0, 0, 1, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "12 Apr 2022"}, {"emp": "REP-2547", "name": "Ajay singh indolia", "asm": 0, "orders": 1, "tentative": 0, "earned": 0, "eligible": false, "gap": 24, "daily": [0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "17 Apr 2026"}, {"emp": "REP-2635", "name": "Mohit gupta", "asm": 0, "orders": 4, "tentative": 0, "earned": 0, "eligible": false, "gap": 21, "daily": [0, 1, 0, 0, 1, 0, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "08 May 2026"}, {"emp": "REP-1993", "name": "Asmaul Ansari", "asm": 0, "orders": 1, "tentative": 0, "earned": 0, "eligible": false, "gap": 24, "daily": [0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "06 Feb 2026"}, {"emp": "REP-2799", "name": "NAMAN DIXIT", "asm": 0, "orders": 3, "tentative": 600, "earned": 0, "eligible": false, "gap": 22, "daily": [0, 0, 0, 0, 0, 1, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "02 Jun 2026"}, {"emp": "REP-2812", "name": "Pratik Patidar", "asm": 0, "orders": 3, "tentative": 600, "earned": 0, "eligible": false, "gap": 22, "daily": [0, 0, 0, 0, 0, 1, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "02 Jun 2026"}, {"emp": "REP-2303", "name": "Krishna Vishwas", "asm": 0, "orders": 3, "tentative": 0, "earned": 0, "eligible": false, "gap": 22, "daily": [0, 0, 1, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "16 Mar 2026"}, {"emp": "REP-2195", "name": "DIVAKAR CHODHARY", "asm": 0, "orders": 2, "tentative": 0, "earned": 0, "eligible": false, "gap": 23, "daily": [0, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "09 Mar 2026"}, {"emp": "REP-2603", "name": "Amar Kalakar", "asm": 0, "orders": 2, "tentative": 0, "earned": 0, "eligible": false, "gap": 23, "daily": [0, 0, 0, 0, 0, 1, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "01 May 2026"}, {"emp": "REP-1977", "name": "Ajad Kumar", "asm": 0, "orders": 4, "tentative": 0, "earned": 0, "eligible": false, "gap": 21, "daily": [1, 0, 0, 0, 1, 0, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "30 Jan 2026"}, {"emp": "REP-1913", "name": "Ashutosh Kumar", "asm": 0, "orders": 4, "tentative": 0, "earned": 0, "eligible": false, "gap": 21, "daily": [0, 0, 0, 0, 1, 1, 0, 1, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "09 Jan 2026"}, {"emp": "REP-2731", "name": "SHUBHAM DASHRATH RATHOD", "asm": 0, "orders": 1, "tentative": 200, "earned": 0, "eligible": false, "gap": 24, "daily": [1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "22 May 2026"}, {"emp": "REP-2537", "name": "Kavindra kumar", "asm": 0, "orders": 1, "tentative": 0, "earned": 0, "eligible": false, "gap": 24, "daily": [0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "14 Apr 2026"}, {"emp": "REP-2488", "name": "NEETESH MEHRA", "asm": 0, "orders": 1, "tentative": 0, "earned": 0, "eligible": false, "gap": 24, "daily": [1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "31 Mar 2026"}, {"emp": "REP-2806", "name": "Bharat pakar", "asm": 0, "orders": 1, "tentative": 200, "earned": 0, "eligible": false, "gap": 24, "daily": [0, 0, 0, 0, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "02 Jun 2026"}, {"emp": "REP-2725", "name": "Piyush Rahangdale", "asm": 0, "orders": 1, "tentative": 200, "earned": 0, "eligible": false, "gap": 24, "daily": [0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0], "doj": "22 May 2026"}]}</script>
<script>
const D = JSON.parse(document.getElementById('DATA').textContent);
const ELIG = D.eligibility, THRESH = D.threshold, A = D.agents;
const T = D.totals;
const rupee = n => n.toLocaleString('en-IN');

/* hero count-up */
function countUp(el, target, dur=1100, prefix=''){
  const start=performance.now();
  function tick(now){
    let p=Math.min(1,(now-start)/dur); p=1-Math.pow(1-p,3);
    el.textContent=prefix+Math.round(target*p).toLocaleString('en-IN');
    if(p<1) requestAnimationFrame(tick);
  }
  requestAnimationFrame(tick);
}
const reduce = matchMedia('(prefers-reduced-motion: reduce)').matches;
if(reduce){
  document.getElementById('pot').textContent='₹'+rupee(T.tentative);
  document.getElementById('s-ord').textContent=rupee(T.orders);
  document.getElementById('s-ag').textContent=T.active;
  document.getElementById('s-days').textContent=(30-T.last_day);
}else{
  countUp(document.getElementById('pot'),T.tentative,1300,'₹');
  countUp(document.getElementById('s-ord'),T.orders,1000);
  countUp(document.getElementById('s-ag'),T.active,1000);
  countUp(document.getElementById('s-days'),30-T.last_day,1000);
}

let sortKey='tentative', query='';
const cmp = {
  tentative:(a,b)=> b.tentative-a.tentative || b.orders-a.orders,
  orders:(a,b)=> b.orders-a.orders || b.tentative-a.tentative,
  gap:(a,b)=> (a.eligible-b.eligible) || a.gap-b.gap || b.tentative-a.tentative
};

/* rank by tentative is the canonical rank shown on every row */
const baseRank = new Map();
[...A].sort(cmp.tentative).forEach((a,i)=>baseRank.set(a.emp,i+1));

function spark(a){
  const days=a.daily.slice(0,T.last_day);
  const mx=Math.max(1,...days);
  return '<div class="spark">'+days.map(v=>
    `<i class="${v?'':'z'}" style="height:${Math.max(8,Math.round(v/mx*100))}%"></i>`).join('')+'</div>';
}

function rowHTML(a){
  const r=baseRank.get(a.emp);
  const tcls=r<=3?('t'+r):'';
  const pct=Math.min(100,Math.round(a.orders/ELIG*100));
  const done=a.eligible;
  const right = done
    ? `<div class="amt"><span class="rs">₹</span>${rupee(a.tentative)}</div><span class="chip on">UNLOCKED</span>`
    : `<div class="amt ${a.tentative?'':'zero'}"><span class="rs">₹</span>${rupee(a.tentative)}</div>`+
      `<span class="chip gap"><b>${a.gap}</b> to unlock</span>`;
  return `<div class="row ${tcls}" data-emp="${a.emp}">
    <div class="rank">${r}</div>
    <div class="mid">
      <div class="nm">${a.name||'—'}</div>
      <div class="ords"><b>${a.orders}</b> orders · ${done?'eligible':'tentative'}</div>
      <div class="meter ${done?'done':''}">
        <div class="warm"></div>
        <div class="tick" style="left:${THRESH/ELIG*100}%"></div>
        <div class="fill" data-w="${pct}"></div>
      </div>
    </div>
    <div class="right">${right}</div>
    <div class="exp"><div class="exp-in">
      <div class="lab">Daily orders<br><b>June 1–${T.last_day}</b></div>
      ${spark(a)}
      <div class="lab" style="text-align:right">Joined<br><b>${a.doj||'—'}</b></div>
    </div></div>
  </div>`;
}

function render(){
  // verge strip (only when no search & sort not 'gap' makes it redundant but keep)
  const verge=A.filter(a=>!a.eligible && a.gap>0 && a.orders>0)
    .sort((x,y)=> x.gap-y.gap || y.tentative-x.tentative).slice(0,8);
  document.getElementById('verge').innerHTML = verge.map(a=>`
    <div class="vcard" data-emp="${a.emp}">
      <div class="nm">${a.name}</div>
      <div class="togo">${a.gap}<small> to go</small></div>
      <div class="unl">unlocks <b>₹${rupee(a.tentative)}</b></div>
    </div>`).join('');

  let list=[...A];
  if(query){
    const q=query.toLowerCase();
    list=list.filter(a=>(a.name||'').toLowerCase().includes(q));
  }
  list.sort(cmp[sortKey]);
  const board=document.getElementById('board');
  board.innerHTML = list.length?list.map(rowHTML).join('')
    :'<div class="empty">No agent matches “'+query+'”.</div>';
  document.getElementById('boardSub').textContent = list.length+' agents';
  document.getElementById('vergeWrap').style.display = query?'none':'';
  // animate meter fills
  requestAnimationFrame(()=>board.querySelectorAll('.fill').forEach(f=>{
    f.style.width=(reduce?1:1)*f.dataset.w+'%';
  }));
}

document.getElementById('seg').addEventListener('click',e=>{
  const b=e.target.closest('button'); if(!b)return;
  sortKey=b.dataset.k;
  [...e.currentTarget.children].forEach(x=>x.setAttribute('aria-pressed', x===b));
  render();
});
let qt; document.getElementById('q').addEventListener('input',e=>{
  clearTimeout(qt); qt=setTimeout(()=>{query=e.target.value.trim();render();},120);
});
document.getElementById('board').addEventListener('click',e=>{
  const row=e.target.closest('.row'); if(row) row.classList.toggle('open');
});
document.getElementById('verge').addEventListener('click',e=>{
  const c=e.target.closest('.vcard'); if(!c)return;
  document.getElementById('q').value=''; query=''; sortKey='tentative';
  [...document.getElementById('seg').children].forEach((x,i)=>x.setAttribute('aria-pressed', i===0));
  render();
  const row=document.querySelector('.row[data-emp="'+c.dataset.emp+'"]');
  if(row){row.classList.add('open','me');row.scrollIntoView({behavior:reduce?'auto':'smooth',block:'center'});}
});
render();
</script>
</body>
</html>
