# Garina-Unban-Server-1
<!-- unban_simulation_demo.html
     Free Fire "Unban Simulation" - Professional-looking, local-only demo UI.
     IMPORTANT: This is a harmless demo. It does NOT connect to any servers and does NOT unblock accounts.
     Use for presentation or training only.
-->

<!doctype html>
<html lang="bn">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Unban Process — Demo (Local Simulation)</title>
<style>
  :root{
    --bg:#0b1220; --card:#0f1724; --accent:#00d1ff; --muted:#9aa7b2;
    --success:#28a745; --danger:#e02424;
    font-family: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
  }
  html,body{height:100%; margin:0; background:linear-gradient(180deg,#031024 0%, #071226 100%); color:#e6eef5;}
  .wrap{max-width:980px; margin:36px auto; padding:28px; background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01)); border-radius:14px; box-shadow: 0 8px 30px rgba(2,6,23,0.7); border:1px solid rgba(255,255,255,0.03);}
  header{display:flex; align-items:center; gap:16px;}
  .logo{width:52px; height:52px; border-radius:10px; background:linear-gradient(135deg,var(--accent), #6ce3ff); display:flex; align-items:center; justify-content:center; color:#001820; font-weight:700;}
  h1{margin:0; font-size:20px;}
  p.lead{margin:6px 0 18px; color:var(--muted); font-size:13px;}
  .grid{display:grid; grid-template-columns: 380px 1fr; gap:18px;}
  .card{background:var(--card); padding:16px; border-radius:12px; border:1px solid rgba(255,255,255,0.02);}
  label{display:block; font-size:12px; color:var(--muted); margin-bottom:6px;}
  input[type=text], textarea, select{width:100%; padding:10px 12px; border-radius:8px; background:#061226; border:1px solid rgba(255,255,255,0.03); color:inherit; outline:none; font-size:14px;}
  .btn{display:inline-flex; gap:10px; align-items:center; padding:10px 14px; border-radius:10px; background:linear-gradient(90deg,var(--accent), #6ce3ff); color:#001820; font-weight:700; border:none; cursor:pointer;}
  .ghost{background:transparent; border:1px solid rgba(255,255,255,0.06); color:var(--muted);}
  .controls{display:flex; gap:10px; margin-top:12px;}
  .status-panel{min-height:360px; display:flex; flex-direction:column; gap:12px;}
  .progress{height:12px; background:rgba(255,255,255,0.03); border-radius:8px; overflow:hidden;}
  .progress > i{display:block; height:100%; width:0%; background:linear-gradient(90deg,var(--accent), #68e2ff); transition:width 700ms ease;}
  .steps{display:flex; flex-direction:column; gap:8px; font-size:13px;}
  .step{display:flex; align-items:center; gap:10px;}
  .dot{width:10px; height:10px; border-radius:50%; background:rgba(255,255,255,0.05); display:inline-block;}
  .dot.ok{background:var(--success); box-shadow:0 0 8px rgba(40,167,69,0.18);}
  .terminal{background:#071827; padding:12px; border-radius:8px; font-family: "Courier New", monospace; font-size:13px; color:#bfe9ff; max-height:180px; overflow:auto; border:1px solid rgba(255,255,255,0.02);}
  .footer{display:flex; justify-content:space-between; align-items:center; gap:12px; margin-top:12px; color:var(--muted); font-size:13px;}
  .big-unlock{display:none; align-items:center; justify-content:center; flex-direction:column; gap:18px; min-height:360px;}
  .unlock-text{font-size:72px; font-weight:900; color:var(--danger); text-shadow: 0 6px 28px rgba(224,36,36,0.28); letter-spacing:6px;}
  .small-note{color:var(--muted); font-size:14px; max-width:720px; text-align:center;}
  .disclaimer{margin-top:12px; padding:10px; background:rgba(255,255,255,0.02); border-radius:8px; color:#ffd6d6; font-size:13px; border:1px dashed rgba(255,255,255,0.03);}
  .muted-small
