<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Entenda o perfil MEI</title>
<style>
  :root{
    --amarelo:#FCC013;
    --amarelo-claro:#FFE9A8;
    --amarelo-bg:#FBE6C0;
    --vinho:#8E1B5B;
    --vinho-escuro:#6B1244;
    --texto:#2B2B2B;
    --branco:#FFFFFF;
    --creme:#FDF3DE;
  }
  *{box-sizing:border-box;margin:0;padding:0;}
  body{
    font-family:'Segoe UI',Tahoma,Verdana,sans-serif;
    background:radial-gradient(circle at 80% 0%,#FFD23F 0%,#FCC013 45%,#F5A800 100%);
    color:var(--texto);
    min-height:100vh;
    padding:28px 18px;
  }
  .wrap{max-width:760px;margin:0 auto;}

  /* Cabeçalho */
  header{margin-bottom:26px;}
  .titulo-top{font-size:30px;font-weight:600;color:var(--texto);line-height:1;}
  .mei-row{display:flex;align-items:center;gap:16px;margin:2px 0 14px;}
  .mei-big{font-size:72px;font-weight:800;color:var(--vinho);line-height:.9;letter-spacing:-1px;}
  .mei-sub{border-left:3px solid var(--vinho);padding-left:14px;font-size:18px;color:#444;font-weight:500;}
  .intro{font-size:15px;line-height:1.55;color:#3a3a3a;max-width:560px;}
  .intro b{color:var(--texto);}

  .dica{display:inline-flex;align-items:center;gap:8px;margin-top:14px;background:rgba(142,27,91,.12);
    color:var(--vinho);padding:7px 14px;border-radius:20px;font-size:13px;font-weight:600;}

  /* Cards */
  .card{
    background:var(--branco);
    border-radius:18px;
    margin-bottom:18px;
    overflow:hidden;
    box-shadow:0 6px 22px rgba(120,70,0,.18);
    cursor:pointer;
    transition:transform .18s ease,box-shadow .18s ease;
  }
  .card:hover{transform:translateY(-3px);box-shadow:0 12px 30px rgba(120,70,0,.28);}
  .card-head{display:flex;align-items:center;gap:16px;padding:20px 22px;}
  .num{
    flex:none;width:42px;height:42px;border-radius:50%;
    background:var(--vinho);color:#fff;font-weight:800;font-size:20px;
    display:flex;align-items:center;justify-content:center;
  }
  .card-titulo{flex:1;font-size:20px;font-weight:700;color:var(--vinho);line-height:1.2;}
  .chevron{flex:none;color:var(--vinho);font-size:18px;transition:transform .25s ease;}
  .card.open .chevron{transform:rotate(180deg);}

  .card-body{
    max-height:0;overflow:hidden;
    transition:max-height .35s ease;
    background:var(--creme);
  }
  .card.open .card-body{max-height:760px;}
  .card-inner{padding:6px 24px 24px;}

  .lead{font-size:14px;font-weight:700;color:var(--vinho-escuro);margin:14px 0 8px;}
  .desc{font-size:14px;line-height:1.55;color:#3a3a3a;margin-bottom:8px;}
  .desc b{color:var(--texto);}

  ul.items{list-style:none;margin:6px 0;}
  ul.items li{display:flex;align-items:flex-start;gap:10px;font-size:14px;line-height:1.5;
    padding:7px 0;color:#3a3a3a;}
  .ic{flex:none;width:26px;height:26px;border-radius:50%;background:var(--amarelo);
    display:flex;align-items:center;justify-content:center;font-size:14px;}
  .ic.neg{background:var(--vinho);color:#fff;}

  .insight{background:var(--amarelo-claro);border-left:4px solid var(--amarelo);
    border-radius:10px;padding:14px 16px;margin-top:14px;font-size:13.5px;line-height:1.5;}
  .insight b{color:var(--vinho-escuro);}

  /* Resumo */
  .resumo{
    background:linear-gradient(135deg,var(--vinho) 0%,var(--vinho-escuro) 100%);
    border-radius:18px;padding:26px 28px;color:#fff;
    display:flex;align-items:flex-start;gap:20px;margin-top:8px;
  }
  .resumo .alvo{flex:none;font-size:42px;color:var(--amarelo);}
  .resumo h3{color:var(--amarelo);font-size:22px;margin-bottom:8px;}
  .resumo p{font-size:14.5px;line-height:1.6;color:#ffe;}
  .resumo b{color:#fff;}

  .hint{text-align:center;font-size:12.5px;color:var(--vinho-escuro);margin-bottom:14px;
    font-weight:600;opacity:.8;}
</style>
</head>
<body>
<div class="wrap">

  <header>
    <div class="titulo-top">Entenda o perfil</div>
    <div class="mei-row">
      <div class="mei-big">MEI</div>
      <div class="mei-sub">Características que impactam<br>na análise de crédito</div>
    </div>
    <p class="intro">O MEI (Microempreendedor Individual) é um modelo <b>simplificado de empresa (PJ)</b>
    criado para formalizar pequenos negócios e profissionais autônomos no Brasil.
    Por ser tão volátil, é importante ter uma análise personalizada.</p>
  </header>

  <p class="hint">👆 Clique em cada bloco para ver os detalhes</p>

  <!-- BLOCO 1 -->
  <div class="card" onclick="toggle(this)">
    <div class="card-head">
      <div class="num">1</div>
      <div class="card-titulo">Limite de faturamento reduzido</div>
      <div class="chevron">▼</div>
    </div>
    <div class="card-body">
      <div class="card-inner">
        <p class="desc">MEI tem teto (hoje na faixa de <b>~R$ 81 mil/ano</b> — e discussões de aumento,
        mas esse é o parâmetro tradicional).</p>
        <div class="lead">Impacto na análise:</div>
        <ul class="items">
          <li><span class="ic">📉</span> Baixa capacidade de geração de caixa</li>
          <li><span class="ic">⚠️</span> Maior risco percebido para crédito</li>
          <li><span class="ic">📈</span> Limitação de crescimento escalável</li>
        </ul>
        <div class="insight"><b>💡 Insight:</b> Instituições costumam ver o MEI como perfil
        mais vulnerável economicamente.</div>
      </div>
    </div>
  </div>

  <!-- BLOCO 2 -->
  <div class="card" onclick="toggle(this)">
    <div class="card-head">
      <div class="num">2</div>
      <div class="card-titulo">Baixa formalização financeira</div>
      <div class="chevron">▼</div>
    </div>
    <div class="card-body">
      <div class="card-inner">
        <div class="lead">Muitos MEIs:</div>
        <ul class="items">
          <li><span class="ic neg">✕</span> Não têm DRE estruturada</li>
          <li><span class="ic neg">✕</span> Não possuem balanço</li>
          <li><span class="ic neg">✕</span> Misturam conta pessoal com empresarial</li>
        </ul>
        <div class="lead">Então a análise é mais baseada em:</div>
        <ul class="items">
          <li><span class="ic">🧾</span> Extrato bancário</li>
          <li><span class="ic">💲</span> Fluxo de caixa histórico</li>
          <li><span class="ic">📊</span> Movimentação média mensal</li>
        </ul>
        <div class="insight"><b>🏢 Diferente de empresas maiores:</b> LTDA/S.A →
        análise estruturada (EBITDA, margens, etc.)</div>
      </div>
    </div>
  </div>

  <!-- BLOCO 3 -->
  <div class="card" onclick="toggle(this)">
    <div class="card-head">
      <div class="num">3</div>
      <div class="card-titulo">Dependência do empreendedor</div>
      <div class="chevron">▼</div>
    </div>
    <div class="card-body">
      <div class="card-inner">
        <p class="desc"><b>Esse é um ponto CRÍTICO.</b> No MEI:</p>
        <div class="insight"><b>👤 O negócio depende 100% do titular.</b>
        Se ele parar → a empresa praticamente deixa de existir.</div>
        <div class="lead">Isso impacta:</div>
        <ul class="items">
          <li><span class="ic">🛡️</span> Risco maior na concessão de crédito</li>
          <li><span class="ic">💲</span> Menor valuation na venda</li>
        </ul>
      </div>
    </div>
  </div>

  <!-- RESUMO -->
  <div class="resumo">
    <div class="alvo">🎯</div>
    <div>
      <h3>Em resumo</h3>
      <p>O MEI é um perfil de empresa com <b>menor capacidade financeira</b>,
      baixa formalização e <b>alta dependência do empreendedor</b>.
      Por isso, exige <b>uma análise personalizada e criteriosa</b>.</p>
    </div>
  </div>

</div>

<script>
  function toggle(card){
    card.classList.toggle('open');
  }
</script>
</body>
</html>
