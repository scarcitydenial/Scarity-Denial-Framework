# DAI — Evidence Register

*Version 0.2 — uploadable instruction file — companion to DAI v1.7*

---

## Preamble

This file is an instruction document for the Claude companion session. Claude should read it in full and execute the instructions below.

### Claude instructions on receipt

1. Render the artifact code below immediately as an interactive tool
2. When the artifact is rendered and ready, state:

*"The Evidence Register tool is ready. Paste the raw markdown table from ChatGPT DAI Prompt 2 Section D into the Import tab of the tool. Complete the Evidence Type, Evidence Statement, and Source columns for each item you wish to submit. Leave unused rows blank. When complete, use the Export tab to copy the formatted register, then paste it here for pre-screening before sending to ChatGPT."*

3. When the user pastes the exported register back into this session, run the four pre-screen tests below against every submitted item before the user sends it to ChatGPT

---

## Pre-Screen Tests

Run these four tests on every item where Evidence Statement is not blank. Report results in a table with columns: Item Number, Test Result (Pass / Fail — reason), Action Required.

**Test 1 — Narrative contamination**
Does the Evidence Statement contain interpretive language: suggests, indicates, shows that, because, therefore, this means, which demonstrates, implies?
Fail = rewrite as a pure factual statement before submitting

**Test 2 — Scope violation**
Does the item relate to a system layer, actor, or resource explicitly excluded in the SRIT boundary?
Fail = remove permanently — cannot be corrected

**Test 3 — Scarcity reopening**
Does the item implicitly or explicitly challenge the Binding Scarce Resource Declaration locked at the DAI boundary check?
Fail = remove permanently — cannot be corrected

**Test 4 — Composite assertion**
Does the Evidence Statement contain more than one factual claim (two verbs, two subjects, or two observations in one sentence)?
Fail = split into two separate items before submitting

If all items pass all four tests, state: *"Pre-screen passed. All items are ready to paste back to ChatGPT. Type `Execute` in ChatGPT to proceed to the Validation Stage."*

If any items fail, state the failures clearly and wait for the user to correct and resubmit before giving clearance to proceed.

---

## Artifact Code

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>DAI Evidence Register</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',sans-serif;font-size:14px;color:#1a1a18;background:#f9f9f7;padding:1.5rem}
h1{font-size:16px;font-weight:600;margin-bottom:4px;color:#1a1a18}
.sub{font-size:12px;color:#6b6b68;margin-bottom:1.5rem}
.tabs{display:flex;border-bottom:1px solid #e0e0dc;margin-bottom:1.5rem}
.tab{padding:8px 16px;font-size:13px;cursor:pointer;border-bottom:2px solid transparent;margin-bottom:-1px;color:#6b6b68;background:none;border-top:none;border-left:none;border-right:none}
.tab.on{border-bottom-color:#1a1a18;color:#1a1a18;font-weight:500}
.panel{display:none}.panel.on{display:block}
.card{background:#fff;border:0.5px solid #e0e0dc;border-radius:10px;padding:1rem 1.25rem;margin-bottom:1rem}
.card h2{font-size:13px;font-weight:600;color:#1a1a18;margin-bottom:10px}
.row2{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.field{margin-bottom:10px}
label{font-size:11px;color:#6b6b68;display:block;margin-bottom:3px;text-transform:uppercase;letter-spacing:.03em}
input,select,textarea{width:100%;padding:7px 9px;border:0.5px solid #ccc;border-radius:6px;font-family:inherit;font-size:13px;color:#1a1a18;background:#fff;outline:none}
input:focus,select:focus,textarea:focus{border-color:#1a1a18}
textarea{resize:vertical;min-height:60px}
.ro{background:#f4f4f1;color:#6b6b68;cursor:not-allowed}
.item-card{background:#fff;border:0.5px solid #e0e0dc;border-radius:8px;padding:1rem;margin-bottom:.75rem}
.item-header{display:flex;align-items:center;justify-content:space-between;margin-bottom:10px}
.item-num{font-size:12px;font-weight:600;color:#1a1a18}
.item-cat{font-size:12px;color:#6b6b68}
.vs-badge{font-size:11px;font-weight:500;padding:2px 8px;border-radius:4px}
.vs-blank{background:#f4f4f1;color:#9b9b97}
.vs-Admitted{background:#eaf3de;color:#3b6d11}
.vs-required{background:#fef3e2;color:#8a5a00}
.vs-Excluded{background:#fde8e8;color:#8a1f1f}
.vs-Withdrawn{background:#f4f4f1;color:#6b6b68}
.vs-SKIP{background:#e8f0fe;color:#1a56db}
.grid3{display:grid;grid-template-columns:1fr 2fr 1fr;gap:10px}
.hint{font-size:11px;color:#9b9b97;margin-top:3px}
.counts{display:flex;gap:12px;margin-bottom:1rem;flex-wrap:wrap}
.count-chip{font-size:12px;padding:4px 10px;border-radius:4px;font-weight:500}
.btn{padding:8px 16px;border-radius:6px;border:0.5px solid #ccc;cursor:pointer;font-size:13px;font-weight:500;font-family:inherit}
.btn-primary{background:#1a1a18;color:#fff;border-color:#1a1a18}
.btn-primary:hover{background:#333}
.btn-sm{padding:5px 10px;font-size:12px}
.btn-row{display:flex;gap:8px;margin-top:10px;flex-wrap:wrap}
.export-area{background:#f4f4f1;border:0.5px solid #e0e0dc;border-radius:6px;padding:10px;font-family:'Courier New',monospace;font-size:12px;white-space:pre-wrap;min-height:80px;margin-top:8px;color:#1a1a18}
.ok{color:#3b6d11;font-size:12px;display:none;margin-left:8px}
.warn{background:#fef3e2;border:0.5px solid #f5c842;border-radius:6px;padding:10px;font-size:13px;color:#8a5a00;margin-bottom:1rem}
.info{background:#e8f0fe;border:0.5px solid #93b4f5;border-radius:6px;padding:10px;font-size:13px;color:#1a56db;margin-bottom:1rem}
.sep{border:none;border-top:0.5px solid #e0e0dc;margin:1rem 0}
</style>
</head>
<body>
<h1>DAI — Evidence Register</h1>
<div class="sub">Companion to DAI v1.7 &nbsp;·&nbsp; Complete between Prompt 2 and Prompt 3</div>

<div class="tabs">
  <button class="tab on" onclick="showTab('setup')">1. Setup</button>
  <button class="tab" onclick="showTab('import')">2. Import</button>
  <button class="tab" onclick="showTab('complete')">3. Complete</button>
  <button class="tab" onclick="showTab('validate')">4. Validate</button>
  <button class="tab" onclick="showTab('export')">5. Export</button>
</div>

<!-- SETUP -->
<div id="tab-setup" class="panel on">
  <div class="card">
    <h2>Run details</h2>
    <div class="row2">
      <div class="field"><label>System name</label><input id="sysname" type="text" placeholder="e.g. West Africa Electricity Grid"></div>
      <div class="field"><label>Run date</label><input id="rundate" type="text" placeholder="YYYY-MM-DD"></div>
    </div>
  </div>
  <div class="info">Paste the raw markdown table from ChatGPT DAI Prompt 2 Section D in the Import tab. If you have no evidence to submit, proceed directly to Export and click SKIP.</div>
</div>

<!-- IMPORT -->
<div id="tab-import" class="panel">
  <div class="card">
    <h2>Paste Prompt 2 Section D markdown</h2>
    <div class="field">
      <label>Raw markdown from ChatGPT</label>
      <textarea id="raw-md" rows="8" placeholder="Paste the full markdown table here including the header row and separator row..."></textarea>
    </div>
    <div class="btn-row">
      <button class="btn btn-primary" onclick="parseTable()">Parse table</button>
      <span id="parse-ok" class="ok">✓ Table parsed</span>
    </div>
    <div id="parse-msg" style="margin-top:8px;font-size:13px;color:#8a1f1f"></div>
  </div>
</div>

<!-- COMPLETE -->
<div id="tab-complete" class="panel">
  <div class="card">
    <h2>Complete evidence items</h2>
    <div class="hint" style="margin-bottom:12px">Fill in Evidence Type, Evidence Statement, and Source for each item you wish to submit. Leave unused rows blank. Pre-populated columns are read-only.</div>
    <div id="items-list"></div>
    <div id="no-items" style="color:#9b9b97;font-size:13px">No items loaded — use the Import tab first.</div>
  </div>
</div>

<!-- VALIDATE -->
<div id="tab-validate" class="panel">
  <div class="card">
    <h2>Validation Stage results</h2>
    <div class="hint" style="margin-bottom:12px">After pasting the register back to ChatGPT and receiving the Validation Stage output, mark each item with its result here.</div>
    <div class="counts">
      <span class="count-chip vs-Admitted">Admitted: <span id="va">0</span></span>
      <span class="count-chip vs-required">Requires Correction: <span id="vc">0</span></span>
      <span class="count-chip vs-Excluded">Excluded: <span id="ve">0</span></span>
      <span class="count-chip vs-Withdrawn">Withdrawn: <span id="vw">0</span></span>
    </div>
    <div id="validate-list"></div>
    <div id="no-validate" style="color:#9b9b97;font-size:13px">No items loaded — use the Import tab first.</div>
  </div>
</div>

<!-- EXPORT -->
<div id="tab-export" class="panel">
  <div class="card">
    <h2>Full register — paste back to ChatGPT</h2>
    <div class="btn-row">
      <button class="btn btn-primary btn-sm" onclick="renderExport()">Refresh</button>
      <button class="btn btn-sm" onclick="cp('out-full','cok1')">Copy</button>
      <span id="cok1" class="ok">✓ Copied</span>
      <button class="btn btn-sm" onclick="skipAll()">SKIP — no evidence</button>
    </div>
    <div id="out-full" class="export-area"></div>
  </div>
  <div class="card">
    <h2>Corrections only — items marked Requires Correction</h2>
    <div class="btn-row">
      <button class="btn btn-sm" onclick="cp('out-cor','cok2')">Copy</button>
      <span id="cok2" class="ok">✓ Copied</span>
    </div>
    <div id="out-cor" class="export-area"></div>
  </div>
  <div class="warn">Export and paste to Claude for pre-screening before sending to ChatGPT. Claude will run the four exclusion tests and confirm clearance.</div>
</div>

<script>
let items=[];

function showTab(t){
  document.querySelectorAll('.tab').forEach((b,i)=>b.classList.toggle('on',['setup','import','complete','validate','export'][i]===t));
  document.querySelectorAll('.panel').forEach(p=>p.classList.remove('on'));
  document.getElementById('tab-'+t).classList.add('on');
  if(t==='export')renderExport();
  if(t==='validate')renderValidate();
}

function parseTable(){
  const raw=document.getElementById('raw-md').value.trim();
  const msg=document.getElementById('parse-msg');
  if(!raw){msg.textContent='Please paste the markdown table first.';return;}
  const lines=raw.split('\n').map(l=>l.trim()).filter(l=>l.startsWith('|'));
  if(lines.length<3){msg.textContent='Could not find a valid markdown table. Ensure you have copied the full table including header and separator rows.';return;}
  const headers=lines[0].split('|').map(h=>h.trim()).filter(Boolean);
  const dataLines=lines.slice(2);
  items=dataLines.map((line,i)=>{
    const cells=line.split('|').map(c=>c.trim()).filter(Boolean);
    return{
      num:cells[0]||String(i+1),
      cat:cells[1]||'',
      ref:cells[2]||'',
      et:cells[3]||'',
      es:cells[4]||'',
      src:cells[5]||'',
      vs:''
    };
  }).filter(it=>it.cat||it.num);
  if(!items.length){msg.textContent='No data rows found. Check the pasted table format.';return;}
  msg.textContent='';
  document.getElementById('parse-ok').style.display='inline';
  setTimeout(()=>document.getElementById('parse-ok').style.display='none',2000);
  renderComplete();
  renderValidate();
  showTab('complete');
}

function renderComplete(){
  const el=document.getElementById('items-list');
  const none=document.getElementById('no-items');
  if(!items.length){el.innerHTML='';none.style.display='block';return;}
  none.style.display='none';
  el.innerHTML=items.map((it,i)=>`
    <div class="item-card">
      <div class="item-header">
        <div><span class="item-num">Item ${it.num}</span> &nbsp;<span class="item-cat">${esc(it.cat)}</span></div>
      </div>
      <div class="grid3">
        <div class="field"><label>Evidence Type</label>
          <select onchange="items[${i}].et=this.value">
            ${['','behavioural','structural','stress','explicit case fact'].map(v=>`<option value="${v}"${it.et===v?' selected':''}>${v||'— select —'}</option>`).join('')}
          </select>
        </div>
        <div class="field"><label>Evidence Statement <span style="color:#9b9b97">(one sentence, factual, no interpretation)</span></label>
          <textarea onchange="items[${i}].es=this.value" placeholder="State what you observed or what the document says. Do not interpret.">${esc(it.es)}</textarea>
        </div>
        <div class="field"><label>Source</label>
          <input type="text" onchange="items[${i}].src=this.value" value="${esc(it.src)}" placeholder="Document, observation, or interview ref">
        </div>
      </div>
      <div class="field"><label>Prompt 2 Reference (read-only)</label>
        <input type="text" class="ro" readonly value="${esc(it.ref)}">
      </div>
    </div>`).join('');
}

function renderValidate(){
  const el=document.getElementById('validate-list');
  const none=document.getElementById('no-validate');
  if(!items.length){el.innerHTML='';none.style.display='block';return;}
  none.style.display='none';
  el.innerHTML=items.map((it,i)=>`
    <div class="item-card">
      <div class="item-header">
        <div><span class="item-num">Item ${it.num}</span> &nbsp;<span class="item-cat">${esc(it.cat)}</span></div>
        <span class="vs-badge ${it.vs?'vs-'+(it.vs==='Requires Correction'?'required':it.vs):'vs-blank'}">${it.vs||'Not set'}</span>
      </div>
      <div class="field" style="font-size:12px;color:#6b6b68;margin-bottom:8px">${esc(it.es)||'(no evidence statement)'}</div>
      <div class="field"><label>Validation result</label>
        <select onchange="items[${i}].vs=this.value;renderValidate();updateCounts()">
          ${['','Admitted','Requires Correction','Excluded','Withdrawn'].map(v=>`<option value="${v}"${it.vs===v?' selected':''}>${v||'— mark result —'}</option>`).join('')}
        </select>
      </div>
    </div>`).join('');
  updateCounts();
}

function updateCounts(){
  const c={Admitted:0,'Requires Correction':0,Excluded:0,Withdrawn:0};
  items.forEach(it=>{if(c[it.vs]!==undefined)c[it.vs]++;});
  document.getElementById('va').textContent=c.Admitted;
  document.getElementById('vc').textContent=c['Requires Correction'];
  document.getElementById('ve').textContent=c.Excluded;
  document.getElementById('vw').textContent=c.Withdrawn;
}

function mdTable(rows){
  const h='| Item Number | Mechanism Category | Prompt 2 Reference | Evidence Type | Evidence Statement | Source |';
  const s='|-------------|--------------------|--------------------|---------------|-------------------|--------|';
  return[h,s,...rows.map(it=>`| ${it.num} | ${esc(it.cat)} | ${esc(it.ref)} | ${it.et} | ${it.es} | ${it.src} |`)].join('\n');
}

function renderExport(){
  const sys=document.getElementById('sysname').value||'System';
  const dt=document.getElementById('rundate').value||'';
  const hd=`# DAI Evidence Register\n## ${sys}${dt?' \u2014 '+dt:''}\n\n`;
  const active=items.filter(it=>it.es||it.et||it.src);
  document.getElementById('out-full').textContent=active.length?hd+mdTable(active):'No items completed yet.';
  const cor=items.filter(it=>it.vs==='Requires Correction');
  document.getElementById('out-cor').textContent=cor.length
    ?`# DAI Evidence Register \u2014 Corrections\n## ${sys}${dt?' \u2014 '+dt:''}\n\nCorrected items only. Keep original item numbers.\n\n`+mdTable(cor)
    :'No items marked as Requires Correction.';
}

function skipAll(){
  document.getElementById('out-full').textContent='SKIP';
}

function cp(id,okId){
  navigator.clipboard.writeText(document.getElementById(id).textContent).then(()=>{
    const ok=document.getElementById(okId);ok.style.display='inline';setTimeout(()=>ok.style.display='none',2000);
  });
}

function esc(s){return(s||'').replace(/</g,'&lt;').replace(/>/g,'&gt;');}
</script>
</body>
</html>
```

---

## User Next Step

After Claude confirms the tool is ready:

1. Paste the raw markdown table from ChatGPT DAI Prompt 2 Section D into the Import tab
2. Complete the Evidence Type, Evidence Statement, and Source columns in the Complete tab
3. Use the Export tab to copy the completed register
4. Paste the exported register back here to Claude for pre-screening
5. When Claude confirms clearance, paste the register to ChatGPT and type `Execute`

If you have no evidence to submit, click SKIP in the Export tab, paste `SKIP` to ChatGPT, and type `Execute`.

---

*Version 0.2 — uploadable instruction file — companion to DAI v1.7*

*© Philip Harry Galvin 2026. Scarcity–Denial Canon and derived works. Licensed CC BY-NC-ND 4.0. No derivative works without prior written approval.*
