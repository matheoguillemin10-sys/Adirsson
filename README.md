<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Linkterpol - Mission Capillaire</title>
  <style>
    :root{
      --bg:#0f1724;
      --muted:#9aa4b2;
      --accent:#00a6ff;
      --white:#ffffff;
      --radius:18px;
      font-family: Inter, "Segoe UI", Roboto, sans-serif;
    }
    *{box-sizing:border-box;margin:0;padding:0}
    html,body{
      height:100%;
      background:linear-gradient(180deg,#071129 0%,#08101a 100%);
      color:var(--white);
      display:flex;align-items:center;justify-content:center;
      padding:32px;
    }
    .card{
      background:rgba(255,255,255,0.04);
      border-radius:var(--radius);
      padding:28px;
      box-shadow:0 10px 30px rgba(2,6,23,0.6);
      text-align:center;
      border:1px solid rgba(255,255,255,0.04);
      max-width:420px;
    }
    .avatar{
      width:180px;height:180px;
      border-radius:50%;overflow:hidden;
      margin:0 auto 16px;
      background:rgba(255,255,255,0.05);
      border:2px solid rgba(255,255,255,0.08);
    }
    .avatar img{width:100%;height:100%;object-fit:cover;}
    .name{font-weight:600;font-size:18px;margin-top:8px;}
    .links{display:flex;flex-direction:column;gap:12px;margin-top:18px;}
    .btn{
      display:flex;align-items:center;justify-content:center;
      padding:12px 16px;border-radius:12px;
      text-decoration:none;font-weight:600;color:var(--white);
      border:1px solid rgba(255,255,255,0.06);
      background:rgba(255,255,255,0.03);
      transition:transform .12s ease;
      cursor:pointer;
    }
    .btn:hover{transform:translateY(-2px);}
    #message{
      margin-top:20px;font-size:15px;font-weight:600;min-height:24px;
    }
    footer{margin-top:16px;font-size:12px;color:var(--muted);}
  </style>
</head>
<body>
  <section class="card">
    <div class="avatar">
      <!-- Mets ici ta photo -->
      <img src="IMG_0158.jpeg" alt="photo">
    </div>
    <div class="name">Linkedin ou interpol</div>
    <div class="links">
      <button id="interpol" class="btn">Interpol</button>
      <button id="linkedin" class="btn">LinkedIn</button>
    </div>
    <div id="message"></div>
  </section>
  <script>
    const msg = document.getElementById("message");
    document.getElementById("interpol").addEventListener("click",()=>{
      msg.style.color="#00ffcc";
      msg.textContent="🕵️ VRAI : Attaque en bande oraganisé pour une greffe de cheveux en Turquie";
    });
    document.getElementById("linkedin").addEventListener("click",()=>{
      msg.style.color="#ff5c5c";
      msg.textContent="❌ FAUX : Attaque en bande oraganisé pour une greffe de cheveux en Turquie";
    });
  </script>
</body>
</html>
