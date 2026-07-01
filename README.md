<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<script src="./support.js"></script>
</head>
<body>
<x-dc>
<helmet>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500;600;700&family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  *{box-sizing:border-box}
  html,body{margin:0;padding:0;background:#0d1220;font-family:'IBM Plex Sans',system-ui,sans-serif;-webkit-font-smoothing:antialiased}
  ::selection{background:rgba(73,224,172,.28)}
  *::-webkit-scrollbar{width:10px;height:10px}
  *::-webkit-scrollbar-thumb{background:#26324a;border-radius:20px}
  *::-webkit-scrollbar-track{background:transparent}
  @keyframes basalPulse{0%{transform:scale(1);opacity:.85}70%{transform:scale(2.6);opacity:0}100%{opacity:0}}
  @keyframes basalFlow{to{stroke-dashoffset:-44}}
  @keyframes basalRise{from{opacity:0;transform:translateY(7px)}to{opacity:1;transform:none}}
</style>
</helmet>
<div style="--bg:#0d1220;--card:#141d2c;--card2:#1b2537;--bd:#27324a;--bds:rgba(255,255,255,.055);--hi:#eef2f8;--mid:#98a6bd;--lo:#6a7890;--acc:#49e0ac;--acc2:#6ea8ff;--amb:#f2c14e;--cor:#ff7a6b;display:flex;height:100vh;width:100%;overflow:hidden;background:var(--bg);color:var(--hi)">

  <aside style="width:236px;flex:none;border-right:1px solid var(--bd);display:flex;flex-direction:column;padding:20px 14px;background:linear-gradient(180deg,#111a28,#0d1220)">
    <div style="display:flex;align-items:center;gap:11px;padding:4px 8px 22px">
      <div style="width:30px;height:30px;border-radius:9px;background:linear-gradient(135deg,var(--acc),var(--acc2));display:flex;align-items:center;justify-content:center;box-shadow:0 4px 16px rgba(73,224,172,.35)"><div style="width:11px;height:11px;background:#0d1220;transform:rotate(45deg);border-radius:2px"></div></div>
      <div><div style="font-family:'Space Grotesk';font-weight:700;font-size:17px;letter-spacing:1px;line-height:1">BASAL</div><div style="font-family:'IBM Plex Mono';font-size:9px;color:var(--lo);letter-spacing:.5px;margin-top:2px">FINANCE CO-PILOT</div></div>
    </div>
    <div style="font-family:'IBM Plex Mono';font-size:9.5px;color:var(--lo);letter-spacing:1px;padding:6px 10px 8px">MENU</div>
    <a style="display:flex;align-items:center;gap:11px;padding:9px 11px;border-radius:10px;font-size:13.5px;font-weight:500;color:var(--hi);background:var(--card2);border:1px solid var(--bd);margin-bottom:3px;cursor:pointer"><svg width="17" height="17" viewBox="0 0 18 18" fill="none" stroke="var(--acc)" stroke-width="1.6"><rect x="2.2" y="2.2" width="5.6" height="5.6" rx="1.4"/><rect x="10.2" y="2.2" width="5.6" height="5.6" rx="1.4"/><rect x="2.2" y="10.2" width="5.6" height="5.6" rx="1.4"/><rect x="10.2" y="10.2" width="5.6" height="5.6" rx="1.4"/></svg>Overview</a>
    <a style="display:flex;align-items:center;gap:11px;padding:9px 11px;border-radius:10px;font-size:13.5px;font-weight:500;color:var(--mid);margin-bottom:3px;cursor:pointer" style-hover="background:var(--card2);color:var(--hi)"><svg width="17" height="17" viewBox="0 0 18 18" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M2 12 L6.5 7 L10 10 L16 3.5"/><path d="M11.5 3.5 H16 V8"/></svg>Forecast</a>
    <a style="display:flex;align-items:center;gap:11px;padding:9px 11px;border-radius:10px;font-size:13.5px;font-weight:500;color:var(--mid);margin-bottom:3px;cursor:pointer" style-hover="background:var(--card2);color:var(--hi)"><svg width="17" height="17" viewBox="0 0 18 18" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round"><rect x="2.5" y="9" width="3" height="6.5" rx="1"/><rect x="7.5" y="5" width="3" height="10.5" rx="1"/><rect x="12.5" y="2.5" width="3" height="13" rx="1"/></svg>Budget</a>
    <a style="display:flex;align-items:center;gap:11px;padding:9px 11px;border-radius:10px;font-size:13.5px;font-weight:500;color:var(--mid);margin-bottom:3px;cursor:pointer" style-hover="background:var(--card2);color:var(--hi)"><svg width="17" height="17" viewBox="0 0 18 18" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M9 2.5 L15.5 14 H2.5 Z"/><line x1="9" y1="7" x2="9" y2="10.5"/><circle cx="9" cy="12.3" r=".4"/></svg>Alerts<span style="margin-left:auto;background:var(--cor);color:#0d1220;font-size:10px;font-weight:700;padding:1px 6px;border-radius:20px;font-family:'IBM Plex Mono'">2</span></a>
    <a style="display:flex;align-items:center;gap:11px;padding:9px 11px;border-radius:10px;font-size:13.5px;font-weight:500;color:var(--mid);margin-bottom:3px;cursor:pointer" style-hover="background:var(--card2);color:var(--hi)"><svg width="17" height="17" viewBox="0 0 18 18" fill="none" stroke="currentColor" stroke-width="1.6"><circle cx="9" cy="9" r="6.5"/><circle cx="9" cy="9" r="3"/><circle cx="9" cy="9" r=".3"/></svg>Goals</a>
    <a style="display:flex;align-items:center;gap:11px;padding:9px 11px;border-radius:10px;font-size:13.5px;font-weight:500;color:var(--mid);margin-bottom:3px;cursor:pointer" style-hover="background:var(--card2);color:var(--hi)"><svg width="17" height="17" viewBox="0 0 18 18" fill="none" stroke="currentColor" stroke-width="1.6"><rect x="2.5" y="4" width="13" height="10" rx="2"/><line x1="2.5" y1="7.5" x2="15.5" y2="7.5"/></svg>Accounts</a>
    <div style="margin-top:auto;display:flex;flex-direction:column;gap:12px">
      <div style="background:linear-gradient(150deg,rgba(110,168,255,.16),rgba(73,224,172,.1));border:1px solid rgba(110,168,255,.28);border-radius:13px;padding:14px">
        <div style="font-family:'Space Grotesk';font-weight:600;font-size:13.5px">BASAL Premium</div>
        <div style="font-size:11.5px;color:var(--mid);line-height:1.5;margin:5px 0 11px">Multi-account consolidation, scenario planning & shared budgets.</div>
        <button style="width:100%;background:var(--hi);color:#0d1220;border:none;border-radius:9px;padding:8px;font-weight:600;font-size:12.5px;cursor:pointer;font-family:inherit" style-hover="background:#fff">Upgrade — $9/mo</button>
      </div>
      <div style="display:flex;align-items:center;gap:10px;padding:6px 4px">
        <div style="width:32px;height:32px;border-radius:50%;background:linear-gradient(135deg,#3a4a66,#26324a);display:flex;align-items:center;justify-content:center;font-weight:600;font-size:13px">C</div>
        <div style="line-height:1.3;min-width:0"><div style="font-size:12.5px;font-weight:600;white-space:nowrap;overflow:hidden;text-overflow:ellipsis">Chioma Orji</div><div style="font-size:10.5px;color:var(--lo)">Free plan</div></div>
        <svg style="margin-left:auto" width="15" height="15" viewBox="0 0 16 16" fill="none" stroke="var(--lo)" stroke-width="1.5" stroke-linecap="round"><circle cx="8" cy="8" r="6"/><path d="M8 5.5v5M5.5 8h5"/></svg>
      </div>
    </div>
  </aside>

  <main style="flex:1;display:flex;flex-direction:column;min-width:0">
    <header style="display:flex;align-items:center;gap:18px;padding:16px 26px;border-bottom:1px solid var(--bd);flex:none">
      <div>
        <div style="font-family:'Space Grotesk';font-weight:600;font-size:18px;letter-spacing:-.3px">Good morning, Chioma</div>
        <div style="font-size:12px;color:var(--lo);margin-top:2px">{{ todayLong }} · 4 accounts synced 2m ago</div>
      </div>
      <div style="margin-left:auto;display:flex;align-items:center;gap:10px">
        <div style="display:flex;align-items:center;gap:8px;background:var(--card);border:1px solid var(--bd);border-radius:10px;padding:8px 12px;width:220px"><svg width="15" height="15" viewBox="0 0 16 16" fill="none" stroke="var(--lo)" stroke-width="1.6"><circle cx="7" cy="7" r="4.5"/><line x1="10.5" y1="10.5" x2="14" y2="14" stroke-linecap="round"/></svg><span style="font-size:12.5px;color:var(--lo)">Ask or search…</span><span style="margin-left:auto;font-family:'IBM Plex Mono';font-size:10px;color:var(--lo);border:1px solid var(--bd);border-radius:4px;padding:1px 5px">⌘K</span></div>
        <button style="display:flex;align-items:center;gap:8px;background:var(--acc);color:#0d2a20;border:none;border-radius:10px;padding:9px 14px;font-weight:600;font-size:12.5px;cursor:pointer;font-family:inherit" style-hover="filter:brightness(1.08)"><svg width="14" height="14" viewBox="0 0 14 14" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><path d="M7 2.5v9M2.5 7h9"/></svg>Connect account</button>
        <button style="width:38px;height:38px;flex:none;border-radius:10px;background:var(--card);border:1px solid var(--bd);cursor:pointer;display:flex;align-items:center;justify-content:center;position:relative" style-hover="background:var(--card2)"><svg width="17" height="17" viewBox="0 0 18 18" fill="none" stroke="var(--mid)" stroke-width="1.6" stroke-linecap="round"><path d="M4 7a5 5 0 0 1 10 0c0 4 1.5 5 1.5 5H2.5S4 11 4 7Z"/><path d="M7.3 15a1.8 1.8 0 0 0 3.4 0"/></svg><span style="position:absolute;top:9px;right:10px;width:7px;height:7px;background:var(--cor);border-radius:50%;border:2px solid var(--card)"></span></button>
      </div>
    </header>

    <div style="flex:1;overflow-y:auto;padding:22px 26px 40px">
      <div style="display:grid;grid-template-columns:minmax(0,1fr) 348px;gap:18px;max-width:1240px">
        <div style="display:flex;flex-direction:column;gap:18px;min-width:0">

          <div style="display:grid;grid-template-columns:repeat(3,1fr);gap:14px">
            <div style="background:var(--card);border:1px solid var(--bd);border-radius:15px;padding:16px 17px">
              <div style="display:flex;align-items:center;gap:7px;color:var(--lo);font-size:11.5px;font-weight:500"><span style="width:6px;height:6px;border-radius:50%;background:var(--mid)"></span>Total balance</div>
              <div style="font-family:'Space Grotesk';font-weight:600;font-size:29px;letter-spacing:-.5px;margin:9px 0 6px">{{ statTotal }}</div>
              <div style="display:flex;align-items:center;gap:6px;font-size:11.5px"><span style="color:var(--acc);font-family:'IBM Plex Mono'">▲ 2.4%</span><span style="color:var(--lo)">vs last month</span></div>
            </div>
            <div style="background:var(--card);border:1px solid var(--bd);border-radius:15px;padding:16px 17px">
              <div style="display:flex;align-items:center;gap:7px;color:var(--lo);font-size:11.5px;font-weight:500"><span style="width:6px;height:6px;border-radius:50%;background:var(--amb)"></span>Forecast low point</div>
              <div style="font-family:'Space Grotesk';font-weight:600;font-size:29px;letter-spacing:-.5px;margin:9px 0 6px;color:var(--amb)">{{ statLow }}</div>
              <div style="font-size:11.5px;color:var(--mid)">expected {{ lowDate }}</div>
            </div>
            <div style="background:var(--card);border:1px solid var(--bd);border-radius:15px;padding:16px 17px">
              <div style="display:flex;align-items:center;gap:7px;color:var(--lo);font-size:11.5px;font-weight:500"><span style="width:6px;height:6px;border-radius:50%;background:var(--acc)"></span>Safe to spend</div>
              <div style="font-family:'Space Grotesk';font-weight:600;font-size:29px;letter-spacing:-.5px;margin:9px 0 6px">{{ statSafe }}</div>
              <div style="font-size:11.5px;color:var(--lo)">after bills & {{ bufferStr }} buffer</div>
            </div>
          </div>

          <div style="background:var(--card);border:1px solid var(--bd);border-radius:16px;padding:18px 18px 14px">
            <div style="display:flex;align-items:flex-start;gap:14px;margin-bottom:6px">
              <div><div style="font-family:'Space Grotesk';font-weight:600;font-size:15.5px">Cash-flow forecast</div><div style="font-size:11.5px;color:var(--lo);margin-top:3px">Projected balance from your income & bill patterns</div></div>
              <div style="margin-left:auto;display:flex;gap:3px;background:var(--bg);border:1px solid var(--bd);border-radius:9px;padding:3px">
                <button onClick="{{ setRange14 }}" style="{{ tab14 }}" style-hover="color:var(--hi)">14D</button>
                <button onClick="{{ setRange30 }}" style="{{ tab30 }}" style-hover="color:var(--hi)">30D</button>
                <button onClick="{{ setRange90 }}" style="{{ tab90 }}" style-hover="color:var(--hi)">90D</button>
              </div>
            </div>
            <div style="display:flex;gap:16px;flex-wrap:wrap;font-size:11px;color:var(--mid);margin:4px 0 8px">
              <span style="display:flex;align-items:center;gap:6px"><span style="width:14px;height:2.5px;background:var(--hi);border-radius:2px"></span>Actual</span>
              <span style="display:flex;align-items:center;gap:6px"><span style="width:14px;height:2.5px;background:var(--acc);border-radius:2px"></span>Forecast</span>
              <span style="display:flex;align-items:center;gap:6px"><span style="width:12px;height:8px;background:rgba(73,224,172,.14);border-radius:2px"></span>Confidence range</span>
              <span style="display:flex;align-items:center;gap:6px"><span style="width:14px;border-top:2px dashed var(--amb)"></span>{{ bufferStr }} buffer</span>
            </div>
            <div style="position:relative">
              <svg viewBox="0 0 820 264" width="100%" style="display:block;height:auto">
                <defs><linearGradient id="basalArea" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stopColor="#eef2f8" stopOpacity="0.13"></stop><stop offset="100%" stopColor="#eef2f8" stopOpacity="0"></stop></linearGradient></defs>
                <sc-for list="{{ gridlines }}" as="g" hint-placeholder-count="4">
                  <line x1="52" y1="{{ g.y }}" x2="800" y2="{{ g.y }}" stroke="var(--bds)" strokeWidth="1"></line>
                  <text x="6" y="{{ g.ty }}" fill="var(--lo)" style="font-family:'IBM Plex Mono';font-size:9.5px">{{ g.label }}</text>
                </sc-for>
                <sc-if value="{{ showBand }}" hint-placeholder-val="{{ true }}"><path d="{{ bandPath }}" fill="var(--acc)" opacity="0.1"></path></sc-if>
                <path d="{{ actualArea }}" fill="url(#basalArea)"></path>
                <line x1="52" y1="{{ thY }}" x2="800" y2="{{ thY }}" stroke="var(--amb)" strokeWidth="1.3" strokeDasharray="2 5" opacity="0.85"></line>
                <line x1="{{ todayX }}" y1="24" x2="{{ todayX }}" y2="236" stroke="var(--bd)" strokeWidth="1" strokeDasharray="3 4"></line>
                <text x="{{ todayX }}" y="250" fill="var(--mid)" textAnchor="middle" style="font-family:'IBM Plex Mono';font-size:9.5px">TODAY</text>
                <path d="{{ actualPath }}" fill="none" stroke="var(--hi)" strokeWidth="2.4" strokeLinejoin="round" strokeLinecap="round"></path>
                <path d="{{ projPath }}" fill="none" stroke="var(--acc)" strokeWidth="2.4" strokeLinejoin="round" strokeLinecap="round" strokeDasharray="6 5" style="animation:basalFlow 1.7s linear infinite"></path>
                <sc-for list="{{ markers }}" as="m" hint-placeholder-count="3">
                  <circle cx="{{ m.x }}" cy="{{ m.y }}" r="4" fill="{{ m.color }}" stroke="var(--card)" strokeWidth="2"></circle>
                  <text x="{{ m.tx }}" y="{{ m.ty }}" fill="{{ m.color }}" textAnchor="{{ m.anchor }}" style="font-family:'IBM Plex Mono';font-size:9px">{{ m.label }}</text>
                </sc-for>
                <circle cx="{{ lowX }}" cy="{{ lowY }}" r="5.5" fill="var(--amb)" stroke="var(--card)" strokeWidth="2.5"></circle>
              </svg>
              <sc-if value="{{ lowBelow }}" hint-placeholder-val="{{ true }}"><div style="position:absolute;left:50%;top:8px;transform:translateX(-50%);background:rgba(242,193,78,.14);border:1px solid rgba(242,193,78,.4);color:var(--amb);font-size:11px;font-weight:600;padding:5px 11px;border-radius:20px;white-space:nowrap;backdrop-filter:blur(4px)">⚠ Dips to {{ statLow }} on {{ lowDate }} — below buffer</div></sc-if>
            </div>
          </div>

          <div style="background:var(--card);border:1px solid var(--bd);border-radius:16px;padding:18px">
            <div style="display:flex;align-items:center;gap:10px;margin-bottom:4px">
              <div style="font-family:'Space Grotesk';font-weight:600;font-size:15.5px">Adaptive budget</div>
              <span style="{{ budgetModeBadge }}">{{ budgetModeLabel }}</span>
              <div style="margin-left:auto;font-size:11.5px;color:var(--lo)">June · 12 days left</div>
            </div>
            <div style="font-size:11.5px;color:var(--mid);margin-bottom:14px">{{ budgetSub }}</div>
            <div style="display:flex;flex-direction:column;gap:14px">
              <sc-for list="{{ budget }}" as="b" hint-placeholder-count="4">
                <div>
                  <div style="display:flex;align-items:center;gap:8px;margin-bottom:7px"><span style="font-size:13px;font-weight:500">{{ b.name }}</span><span style="margin-left:auto;font-family:'IBM Plex Mono';font-size:12px;color:var(--mid)">{{ b.spentStr }} <span style="color:var(--lo)">/ {{ b.capStr }}</span></span></div>
                  <div style="height:7px;background:var(--bg);border-radius:20px;overflow:hidden"><div style="height:100%;width:{{ b.pct }};background:{{ b.barColor }};border-radius:20px"></div></div>
                  <sc-if value="{{ b.showChip }}" hint-placeholder-val="{{ false }}">
                    <div style="display:flex;align-items:center;gap:9px;margin-top:9px;background:var(--bg);border:1px solid var(--bd);border-radius:10px;padding:8px 11px">
                      <svg width="15" height="15" viewBox="0 0 16 16" fill="none" stroke="var(--acc2)" stroke-width="1.6" style="flex:none"><circle cx="8" cy="8" r="6.2"/><path d="M8 4.6v3.6l2.3 1.4" stroke-linecap="round"/></svg>
                      <span style="font-size:11.5px;color:var(--mid);line-height:1.4"><b style="color:var(--hi);font-weight:600">Suggests {{ b.suggestStr }}</b> — {{ b.note }}</span>
                      <div style="margin-left:auto;display:flex;gap:6px;flex:none">
                        <button onClick="{{ b.onAccept }}" style="background:var(--acc);color:#0d2a20;border:none;border-radius:7px;padding:5px 11px;font-size:11.5px;font-weight:600;cursor:pointer;font-family:inherit" style-hover="filter:brightness(1.08)">Apply</button>
                        <button onClick="{{ b.onDecline }}" style="background:transparent;color:var(--lo);border:1px solid var(--bd);border-radius:7px;padding:5px 10px;font-size:11.5px;cursor:pointer;font-family:inherit" style-hover="color:var(--hi)">Keep</button>
                      </div>
                    </div>
                  </sc-if>
                  <sc-if value="{{ b.showStatus }}" hint-placeholder-val="{{ false }}"><div style="margin-top:8px;font-size:11px;color:{{ b.statusColor }}">{{ b.statusText }}</div></sc-if>
                </div>
              </sc-for>
            </div>
          </div>

          <div style="background:var(--card);border:1px solid var(--bd);border-radius:16px;padding:18px">
            <div style="display:flex;align-items:center;gap:9px;margin-bottom:14px"><div style="font-family:'Space Grotesk';font-weight:600;font-size:15.5px">Early warnings</div><span style="font-size:11px;color:var(--lo)">· flagged days ahead, not after</span></div>
            <div style="display:flex;flex-direction:column;gap:10px">
              <sc-for list="{{ alerts }}" as="a" hint-placeholder-count="3">
                <div style="display:flex;gap:12px;align-items:flex-start;background:var(--bg);border:1px solid {{ a.line }};border-radius:12px;padding:13px 14px">
                  <div style="width:30px;height:30px;flex:none;border-radius:8px;background:{{ a.tint }};display:flex;align-items:center;justify-content:center;color:{{ a.chipColor }};font-weight:700;font-size:14px">{{ a.glyph }}</div>
                  <div style="min-width:0;flex:1">
                    <div style="display:flex;align-items:center;gap:8px;flex-wrap:wrap"><span style="font-size:13px;font-weight:600">{{ a.title }}</span><span style="font-family:'IBM Plex Mono';font-size:10px;color:{{ a.chipColor }};background:{{ a.tint }};padding:1px 7px;border-radius:20px">{{ a.when }}</span></div>
                    <div style="font-size:12px;color:var(--mid);line-height:1.5;margin-top:4px">{{ a.body }}</div>
                    <sc-if value="{{ a.cta }}" hint-placeholder-val="{{ false }}"><button style="margin-top:9px;background:transparent;color:{{ a.chipColor }};border:1px solid {{ a.line }};border-radius:8px;padding:5px 11px;font-size:11.5px;font-weight:600;cursor:pointer;font-family:inherit" style-hover="background:var(--card2)">{{ a.cta }}</button></sc-if>
                  </div>
                  <button onClick="{{ a.onDismiss }}" style="flex:none;background:transparent;border:none;color:var(--lo);cursor:pointer;padding:2px;font-size:14px;line-height:1" style-hover="color:var(--hi)">✕</button>
                </div>
              </sc-for>
            </div>
          </div>
        </div>

        <div style="display:flex;flex-direction:column;gap:18px;min-width:0">
          <div style="background:linear-gradient(180deg,#182338,var(--card));border:1px solid rgba(110,168,255,.22);border-radius:16px;overflow:hidden;display:flex;flex-direction:column">
            <div style="display:flex;align-items:center;gap:11px;padding:16px 16px 14px;border-bottom:1px solid var(--bd)">
              <div style="position:relative;width:34px;height:34px;flex:none">
                <div style="width:34px;height:34px;border-radius:10px;background:linear-gradient(135deg,var(--acc2),var(--acc));display:flex;align-items:center;justify-content:center"><div style="width:11px;height:11px;background:#0d1220;transform:rotate(45deg);border-radius:2px"></div></div>
                <span style="position:absolute;bottom:-1px;right:-1px;width:9px;height:9px;background:var(--acc);border-radius:50%;border:2px solid var(--card)"></span>
                <span style="position:absolute;bottom:1px;right:1px;width:5px;height:5px;background:var(--acc);border-radius:50%;animation:basalPulse 2.2s ease-out infinite"></span>
              </div>
              <div style="line-height:1.3"><div style="font-family:'Space Grotesk';font-weight:600;font-size:14px">BASAL Co-pilot</div><div style="font-size:10.5px;color:var(--acc)">● Analyzing · updated 2m ago</div></div>
            </div>
            <div style="padding:14px 16px 4px">
              <div style="font-size:12.5px;color:var(--mid);line-height:1.55;margin-bottom:13px">You're on track this month. I found <b style="color:var(--hi)">a few things</b> worth a look — each is one tap and reversible.</div>
              <div style="display:flex;flex-direction:column;gap:11px">
                <sc-for list="{{ recs }}" as="r" hint-placeholder-count="3">
                  <div style="background:var(--bg);border:1px solid var(--bd);border-radius:13px;padding:13px;animation:basalRise .35s ease both">
                    <div style="display:flex;align-items:center;gap:7px;margin-bottom:7px"><span style="width:6px;height:6px;border-radius:50%;background:{{ r.dot }}"></span><span style="font-family:'IBM Plex Mono';font-size:9.5px;letter-spacing:.5px;color:{{ r.dot }};text-transform:uppercase">{{ r.tag }}</span></div>
                    <div style="font-size:13px;font-weight:600;line-height:1.35;margin-bottom:5px">{{ r.title }}</div>
                    <div style="font-size:11.5px;color:var(--mid);line-height:1.5;margin-bottom:11px">{{ r.body }}</div>
                    <div style="display:flex;gap:7px">
                      <button onClick="{{ r.onApprove }}" style="flex:1;background:var(--acc);color:#0d2a20;border:none;border-radius:8px;padding:7px;font-size:12px;font-weight:600;cursor:pointer;font-family:inherit" style-hover="filter:brightness(1.08)">{{ r.cta }}</button>
                      <button onClick="{{ r.onDismiss }}" style="background:transparent;color:var(--lo);border:1px solid var(--bd);border-radius:8px;padding:7px 12px;font-size:12px;cursor:pointer;font-family:inherit" style-hover="color:var(--hi)">Not now</button>
                    </div>
                  </div>
                </sc-for>
                <sc-if value="{{ recsEmpty }}" hint-placeholder-val="{{ false }}"><div style="text-align:center;padding:16px 8px;font-size:12px;color:var(--lo)">✓ All caught up. I'll keep watching your accounts.</div></sc-if>
              </div>
            </div>
            <sc-if value="{{ hasChat }}" hint-placeholder-val="{{ false }}">
              <div style="padding:8px 16px 4px;display:flex;flex-direction:column;gap:8px">
                <sc-for list="{{ chat }}" as="c" hint-placeholder-count="0"><div style="{{ c.wrap }}"><div style="{{ c.bubble }}">{{ c.text }}</div></div></sc-for>
              </div>
            </sc-if>
            <div style="padding:12px 14px 14px;margin-top:auto">
              <div style="display:flex;gap:8px;align-items:center;background:var(--bg);border:1px solid var(--bd);border-radius:11px;padding:6px 6px 6px 13px">
                <input ref="{{ chatRef }}" onKeyDown="{{ onKey }}" placeholder="Ask about your money…" style="flex:1;background:transparent;border:none;outline:none;color:var(--hi);font-size:12.5px;font-family:inherit"/>
                <button onClick="{{ send }}" style="width:30px;height:30px;flex:none;border-radius:8px;background:var(--acc2);border:none;cursor:pointer;display:flex;align-items:center;justify-content:center" style-hover="filter:brightness(1.1)"><svg width="15" height="15" viewBox="0 0 16 16" fill="none" stroke="#0d1220" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M2.5 8h10M8 3.5 12.5 8 8 12.5"/></svg></button>
              </div>
            </div>
          </div>

          <div style="background:var(--card);border:1px solid var(--bd);border-radius:16px;padding:16px 18px">
            <div style="display:flex;align-items:center;gap:8px;margin-bottom:13px"><div style="font-family:'Space Grotesk';font-weight:600;font-size:14px">Connected accounts</div><span style="margin-left:auto;display:flex;align-items:center;gap:5px;font-size:10px;color:var(--acc)"><svg width="12" height="12" viewBox="0 0 14 14" fill="none" stroke="currentColor" stroke-width="1.5"><rect x="2.5" y="6" width="9" height="6" rx="1.4"/><path d="M4.5 6V4.3a2.5 2.5 0 0 1 5 0V6"/></svg>Encrypted</span></div>
            <div style="display:flex;flex-direction:column;gap:3px">
              <sc-for list="{{ accounts }}" as="ac" hint-placeholder-count="4">
                <div style="display:flex;align-items:center;gap:11px;padding:9px 4px;border-bottom:1px solid var(--bds)">
                  <div style="width:30px;height:30px;flex:none;border-radius:8px;background:var(--card2);display:flex;align-items:center;justify-content:center;font-family:'IBM Plex Mono';font-size:11px;color:{{ ac.color }};font-weight:500">{{ ac.badge }}</div>
                  <div style="min-width:0"><div style="font-size:12.5px;font-weight:500;white-space:nowrap;overflow:hidden;text-overflow:ellipsis">{{ ac.name }}</div><div style="font-family:'IBM Plex Mono';font-size:10px;color:var(--lo)">{{ ac.mask }}</div></div>
                  <div style="margin-left:auto;font-family:'IBM Plex Mono';font-size:13px;font-weight:500;color:{{ ac.balColor }}">{{ ac.balStr }}</div>
                </div>
              </sc-for>
            </div>
            <div style="font-size:10px;color:var(--lo);margin-top:11px;line-height:1.5">256-bit encryption · read-only access · we never store your bank credentials</div>
          </div>

          <div style="background:var(--card);border:1px solid var(--bd);border-radius:16px;padding:16px 18px">
            <div style="font-family:'Space Grotesk';font-weight:600;font-size:14px;margin-bottom:13px">Goals</div>
            <div style="display:flex;flex-direction:column;gap:15px">
              <sc-for list="{{ goals }}" as="g" hint-placeholder-count="2">
                <div>
                  <div style="display:flex;align-items:center;gap:8px;margin-bottom:7px"><span style="font-size:12.5px;font-weight:500">{{ g.name }}</span><span style="margin-left:auto;font-family:'IBM Plex Mono';font-size:11px;color:var(--mid)">{{ g.curStr }} <span style="color:var(--lo)">/ {{ g.tgtStr }}</span></span></div>
                  <div style="height:7px;background:var(--bg);border-radius:20px;overflow:hidden"><div style="height:100%;width:{{ g.pct }};background:linear-gradient(90deg,var(--acc2),var(--acc));border-radius:20px"></div></div>
                </div>
              </sc-for>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>

  <sc-if value="{{ toast }}" hint-placeholder-val="{{ false }}">
    <div style="position:fixed;bottom:22px;left:50%;transform:translateX(-50%);display:flex;align-items:center;gap:14px;background:#1b2537;border:1px solid var(--bd);border-radius:12px;padding:11px 14px 11px 16px;box-shadow:0 12px 40px rgba(0,0,0,.5);z-index:50;animation:basalRise .3s ease both">
      <span style="font-size:12.5px;color:var(--hi)">{{ toastMsg }}</span>
      <button onClick="{{ onUndo }}" style="background:transparent;border:none;color:var(--acc);font-weight:600;font-size:12.5px;cursor:pointer;font-family:inherit">Undo</button>
    </div>
  </sc-if>
</div>
</x-dc>
<script type="text/x-dc" data-dc-script data-props="{&quot;$preview&quot;:{&quot;width&quot;:1440,&quot;height&quot;:940},&quot;budgetMode&quot;:{&quot;editor&quot;:&quot;enum&quot;,&quot;options&quot;:[&quot;Suggest &amp; confirm&quot;,&quot;Fully automatic&quot;],&quot;default&quot;:&quot;Suggest &amp; confirm&quot;,&quot;tsType&quot;:&quot;string&quot;,&quot;section&quot;:&quot;Behavior&quot;},&quot;showConfidenceBand&quot;:{&quot;editor&quot;:&quot;boolean&quot;,&quot;default&quot;:true,&quot;tsType&quot;:&quot;boolean&quot;,&quot;section&quot;:&quot;Forecast&quot;},&quot;riskThreshold&quot;:{&quot;editor&quot;:&quot;range&quot;,&quot;default&quot;:1500,&quot;min&quot;:0,&quot;max&quot;:3000,&quot;step&quot;:100,&quot;unit&quot;:&quot;$&quot;,&quot;tsType&quot;:&quot;number&quot;,&quot;section&quot;:&quot;Forecast&quot;}}">
class Component extends DCLogic {
  state = {
    range: '30D',
    recs: [
      { id:'r1', tag:'Cash flow', dot:'var(--acc)', title:'Move $200 into savings today', body:'Your forecast shows a surplus through Jul 4. Transferring now keeps your buffer healthy and earns interest.', cta:'Transfer $200', done:'Transfer scheduled ✓' },
      { id:'r2', tag:'Bills', dot:'var(--acc2)', title:'Schedule your $540 card payment', body:'Due Jun 27. Pay from checking on the 26th to avoid a late fee and stay above your buffer.', cta:'Schedule', done:'Payment scheduled ✓' },
      { id:'r3', tag:'Savings', dot:'var(--amb)', title:'Duplicate subscription found', body:'You pay for two music services ($20/mo). Cancelling one saves about $240 a year.', cta:'Review', done:'Opened review ✓' },
    ],
    budget: [
      { id:'b1', name:'Dining & takeout', spent:286, cap:400, suggest:320, note:'trending 20% lower for 3 weeks', status:'suggest' },
      { id:'b2', name:'Groceries', spent:472, cap:520, suggest:580, note:'seasonal price rise detected', status:'suggest' },
      { id:'b3', name:'Transport', spent:96, cap:160, suggest:160, note:'', status:'ok' },
      { id:'b4', name:'Shopping', spent:210, cap:300, suggest:240, note:'freeing cash toward your Japan goal', status:'suggest' },
    ],
    alerts: [
      { id:'a1', sev:'warn', glyph:'!', title:'Forecast dips below your buffer', when:'in 12 days', bodyT:'Balance is projected to reach {low} on {date} — under your {buf} safety buffer.', cta:'See the plan' },
      { id:'a2', sev:'warn', glyph:'~', title:'Dining is above your usual pace', when:'this week', bodyT:'You have spent 42% more than a typical week. At this rate you will exceed the category by about $80.', cta:'Adjust budget' },
      { id:'a3', sev:'ok', glyph:'✓', title:'Income on track', when:'Jun 24', bodyT:'Your $2,800 salary is expected on time. A $900 freelance deposit is also detected for Jul 2.', cta:null },
    ],
    chat: [],
    toast: null,
  };

  buildMaster(){
    if(this._m2) return this._m2;
    const N=110, today=44; const bal=new Array(N); const ev={};
    const add=(i,label,amt,kind)=>{ (ev[i]=ev[i]||[]).push({label,amt,kind}); };
    let b=5200;
    for(let i=0;i<N;i++){
      b -= (80 + 22*Math.sin(i*1.1) + 9*Math.cos(i*0.4));
      if(i%14===8){ b+=2800; add(i,'Salary',2800,'in'); }
      if(i%30===19){ b-=1650; add(i,'Rent',-1650,'out'); }
      if(i%15===12){ b-=540; add(i,'Card',-540,'out'); }
      if(i===46){ b-=1200; add(i,'Insurance',-1200,'out'); }
      if(i===48){ b-=540; add(i,'Card',-540,'out'); }
      if(i===52){ b+=900; add(i,'Freelance',900,'in'); }
      bal[i]=Math.round(b);
    }
    const off = 4740 - bal[today];
    for(let i=0;i<N;i++) bal[i]+=off;
    this._m2 = { N, today, bal, ev };
    return this._m2;
  }

  fmt(n){ const s=n<0?'-':''; return s+'$'+Math.abs(Math.round(n)).toLocaleString('en-US'); }
  dateFor(i){ const m=this.buildMaster(); const d=new Date(2026,5,18); d.setDate(d.getDate()+(i-m.today)); return d.toLocaleDateString('en-US',{month:'short',day:'numeric'}); }

  buffer(){ return this.props.riskThreshold ?? 1500; }

  chart(){
    const m=this.buildMaster();
    const cfg={ '14D':{back:5,fwd:9}, '30D':{back:11,fwd:19}, '90D':{back:30,fwd:59} }[this.state.range];
    const start=m.today-cfg.back, end=m.today+cfg.fwd;
    const X0=52,X1=800,Y0=26,Y1=232;
    const vals=[]; for(let i=start;i<=end;i++) vals.push(m.bal[i]);
    let maxV=Math.max(...vals), minV=Math.min(...vals);
    const buf=this.buffer(); maxV=Math.max(maxV,buf); minV=Math.min(minV,buf);
    const top=Math.ceil((maxV*1.12)/500)*500;
    const bot=Math.max(0,Math.floor((minV*0.82)/500)*500);
    const sx=i=> X0 + ((i-start)/(end-start))*(X1-X0);
    const sy=v=> Y1 - ((v-bot)/(top-bot))*(Y1-Y0);
    const P=a=>a.map((p,i)=>(i?'L':'M')+p[0].toFixed(1)+' '+p[1].toFixed(1)).join(' ');

    const actual=[], proj=[];
    for(let i=start;i<=end;i++){ const pt=[sx(i),sy(m.bal[i])]; if(i<=m.today) actual.push(pt); if(i>=m.today) proj.push(pt); }
    const actualPath=P(actual), projPath=P(proj);
    const actualArea='M '+sx(start).toFixed(1)+' '+Y1+' '+P(actual).slice(2).replace(/M/g,'L')+' L '+sx(m.today).toFixed(1)+' '+Y1+' Z';

    // confidence band on projected
    const up=[], lo=[];
    for(let i=m.today;i<=end;i++){ const sp=(i-m.today)*Math.max(30,(top-bot)*0.012); up.push([sx(i),sy(m.bal[i]+sp)]); lo.push([sx(i),sy(m.bal[i]-sp)]); }
    const bandPath = P(up)+' '+lo.reverse().map(p=>'L'+p[0].toFixed(1)+' '+p[1].toFixed(1)).join(' ')+' Z';

    // gridlines
    const gridlines=[]; for(let k=0;k<=3;k++){ const v=bot+(top-bot)*(k/3); const y=sy(v); gridlines.push({ y:y.toFixed(1), ty:(y-4).toFixed(1), label:'$'+Math.round(v/1000*10)/10+'k' }); }

    // markers (significant events in window)
    const markers=[];
    for(let i=start;i<=end;i++){ const es=m.ev[i]; if(!es) continue; for(const e of es){ if(Math.abs(e.amt)<500) continue;
      const x=sx(i), y=sy(m.bal[i]); const isIn=e.kind==='in';
      markers.push({ x:x.toFixed(1), y:y.toFixed(1), tx:x.toFixed(1), ty:(isIn?y-10:y+16).toFixed(1), anchor:'middle', color:isIn?'var(--acc)':'var(--cor)', label:e.label });
    }}
    while(markers.length>5) markers.splice(2,1);

    // low point over projected
    let lowIdx=m.today, lowVal=Infinity;
    for(let i=m.today;i<=end;i++){ if(m.bal[i]<lowVal){ lowVal=m.bal[i]; lowIdx=i; } }
    const thY=Math.max(Y0,Math.min(Y1,sy(buf)));

    // safe to spend
    let near=0; for(let i=m.today+1;i<=m.today+7;i++){ const es=m.ev[i]; if(es) for(const e of es) if(e.amt<0) near+=Math.abs(e.amt); }
    const safe=Math.max(0, m.bal[m.today]-buf-near);

    return {
      actualPath, projPath, actualArea, bandPath, gridlines, markers,
      thY:thY.toFixed(1), todayX:sx(m.today).toFixed(1),
      lowX:sx(lowIdx).toFixed(1), lowY:sy(lowVal).toFixed(1),
      lowVal, lowIdx, safe, current:m.bal[m.today],
    };
  }

  setRange(r){ this.setState({range:r}); }

  approve(id){ const r=this.state.recs.find(x=>x.id===id); this._removeRec(id, r?r.done:'Done ✓'); }
  dismiss(id){ this._removeRec(id, 'Suggestion dismissed'); }
  _removeRec(id,msg){ const r=this.state.recs.find(x=>x.id===id); this.setState(s=>({ recs:s.recs.filter(x=>x.id!==id), toast:{ msg, rec:r } })); clearTimeout(this._tt); this._tt=setTimeout(()=>this.setState({toast:null}),6000); }
  undo(){ const t=this.state.toast; if(t&&t.rec){ this.setState(s=>({ recs:[t.rec,...s.recs], toast:null })); } else this.setState({toast:null}); }

  acceptBudget(id){ this.setState(s=>({ budget:s.budget.map(b=>b.id===id?{...b,cap:b.suggest,status:'applied'}:b) })); }
  declineBudget(id){ this.setState(s=>({ budget:s.budget.map(b=>b.id===id?{...b,status:'kept'}:b) })); }
  dismissAlert(id){ this.setState(s=>({ alerts:s.alerts.filter(a=>a.id!==id) })); }

  send(){ const el=this._chat; if(!el) return; const v=(el.value||'').trim(); if(!v) return; el.value=''; const a=this.reply(v); this.setState(s=>({ chat:[...s.chat,{who:'me',text:v},{who:'ai',text:a}] })); }
  onKey(e){ if(e.key==='Enter'){ e.preventDefault(); this.send(); } }
  reply(q){ const c=this.chart(); const t=q.toLowerCase();
    if(/afford|spend|spare/.test(t)) return 'You can safely spend about '+this.fmt(c.safe)+' right now — that keeps your '+this.fmt(this.buffer())+' buffer intact through your next bill.';
    if(/save|saving/.test(t)) return 'Based on your forecast you have room to move ~$200 to savings today without risking your buffer.';
    if(/rent|bill|due/.test(t)) return 'Your next big outflow is a $540 card payment on Jun 27, then insurance around Jun 30. I can schedule either for you.';
    if(/low|short|overdraft|risk/.test(t)) return 'Your projected low is '+this.fmt(c.lowVal)+' on '+this.dateFor(c.lowIdx)+'. I flagged it 12 days ahead so you have time to act.';
    return 'Right now your safe-to-spend is '+this.fmt(c.safe)+' and your forecast low is '+this.fmt(c.lowVal)+' on '+this.dateFor(c.lowIdx)+'. Ask me about saving, bills, or what you can afford.';
  }

  tabStyle(on){ return 'border:none;border-radius:7px;padding:5px 11px;font-size:11.5px;font-weight:600;cursor:pointer;font-family:inherit;background:'+(on?'var(--card2)':'transparent')+';color:'+(on?'var(--hi)':'var(--lo)'); }

  renderVals(){
    const c=this.chart(); const buf=this.buffer(); const auto=(this.props.budgetMode??'Suggest & confirm')==='Fully automatic';
    const badge='font-family:\'IBM Plex Mono\';font-size:9.5px;letter-spacing:.5px;padding:2px 8px;border-radius:20px;'+(auto?'color:var(--acc2);background:rgba(110,168,255,.14)':'color:var(--acc);background:rgba(73,224,172,.12)');

    const budget=this.state.budget.map(b=>{
      const cap=auto?b.suggest:b.cap; const pct=Math.min(100,Math.round(b.spent/cap*100));
      const over=b.spent>cap; const showChip=!auto && b.status==='suggest';
      let statusText='', statusColor='var(--lo)', showStatus=false;
      if(auto && b.suggest!==b.cap){ showStatus=true; statusText='◆ Auto-adjusted to '+this.fmt(b.suggest)+' — '+b.note; statusColor='var(--acc2)'; }
      else if(b.status==='applied'){ showStatus=true; statusText='✓ Applied — new limit '+this.fmt(b.cap); statusColor='var(--acc)'; }
      else if(b.status==='kept'){ showStatus=true; statusText='Kept your limit of '+this.fmt(b.cap); statusColor='var(--lo)'; }
      return { ...b, pct:pct+'%', capStr:this.fmt(cap), spentStr:this.fmt(b.spent), suggestStr:this.fmt(b.suggest),
        barColor: over?'var(--cor)':(pct>85?'var(--amb)':'var(--acc)'),
        showChip, showStatus, statusText, statusColor,
        onAccept:()=>this.acceptBudget(b.id), onDecline:()=>this.declineBudget(b.id) };
    });

    const tint={ warn:'rgba(242,193,78,.14)', ok:'rgba(73,224,172,.12)' };
    const line={ warn:'rgba(242,193,78,.32)', ok:'rgba(73,224,172,.28)' };
    const chip={ warn:'var(--amb)', ok:'var(--acc)' };
    const daysToLow=c.lowIdx-this.buildMaster().today;
    const alerts=this.state.alerts.map(a=>({ ...a,
      body:a.bodyT.replace('{low}',this.fmt(c.lowVal)).replace('{buf}',this.fmt(buf)).replace('{date}',this.dateFor(c.lowIdx)),
      when: a.id==='a1' ? ('in '+daysToLow+' days') : a.when,
      tint:tint[a.sev], line:line[a.sev], chipColor:chip[a.sev], onDismiss:()=>this.dismissAlert(a.id) }));

    const recs=this.state.recs.map(r=>({ ...r, onApprove:()=>this.approve(r.id), onDismiss:()=>this.dismiss(r.id) }));

    const accents={ Bank:'var(--acc)', Card:'var(--acc2)', Wallet:'var(--amb)' };
    const accs=[
      { name:'Chase Checking', mask:'•••• 4021', bal:4740, type:'Bank', badge:'CH' },
      { name:'Ally Savings', mask:'•••• 7788', bal:12300, type:'Bank', badge:'AS' },
      { name:'Amex Platinum', mask:'•••• 1009', bal:-540, type:'Card', badge:'AX' },
      { name:'Cash App', mask:'wallet', bal:220, type:'Wallet', badge:'$' },
    ].map(a=>({ ...a, color:accents[a.type], balStr:this.fmt(a.bal), balColor:a.bal<0?'var(--cor)':'var(--hi)' }));

    const goals=[
      { name:'Emergency fund', cur:12300, tgt:15000 },
      { name:'Japan trip', cur:2100, tgt:5000 },
    ].map(g=>({ ...g, pct:Math.round(g.cur/g.tgt*100)+'%', curStr:this.fmt(g.cur), tgtStr:this.fmt(g.tgt) }));

    const chat=this.state.chat.map(m=>({ text:m.text,
      wrap:'display:flex;justify-content:'+(m.who==='me'?'flex-end':'flex-start'),
      bubble:'max-width:82%;font-size:11.5px;line-height:1.45;padding:7px 11px;border-radius:12px;'+(m.who==='me'?'background:var(--acc2);color:#0d1220;border-bottom-right-radius:3px':'background:var(--bg);color:var(--mid);border:1px solid var(--bd);border-bottom-left-radius:3px') }));

    return {
      todayLong:'Thursday, June 18',
      statTotal:this.fmt(4740+12300+220), statLow:this.fmt(c.lowVal), lowDate:this.dateFor(c.lowIdx),
      statSafe:this.fmt(c.safe), bufferStr:this.fmt(buf),
      tab14:this.tabStyle(this.state.range==='14D'), tab30:this.tabStyle(this.state.range==='30D'), tab90:this.tabStyle(this.state.range==='90D'),
      setRange14:()=>this.setRange('14D'), setRange30:()=>this.setRange('30D'), setRange90:()=>this.setRange('90D'),
      gridlines:c.gridlines, markers:c.markers, actualPath:c.actualPath, projPath:c.projPath, actualArea:c.actualArea, bandPath:c.bandPath,
      showBand:(this.props.showConfidenceBand??true), thY:c.thY, todayX:c.todayX, lowX:c.lowX, lowY:c.lowY, lowBelow:c.lowVal<buf,
      budgetModeLabel:auto?'Fully automatic':'Suggest & confirm', budgetModeBadge:badge,
      budgetSub:auto?'BASAL reallocates categories automatically based on your behavior. Every change is logged and reversible.':'BASAL proposes changes based on your behavior — you stay in control and confirm each one.',
      budget, alerts, recs, recsEmpty:this.state.recs.length===0,
      accounts:accs, goals,
      chat, hasChat:this.state.chat.length>0, chatRef:(el)=>{this._chat=el;}, send:()=>this.send(), onKey:(e)=>this.onKey(e),
      toast:this.state.toast, toastMsg:this.state.toast?this.state.toast.msg:'', onUndo:()=>this.undo(),
    };
  }
}
</script>
</body>
</html>
