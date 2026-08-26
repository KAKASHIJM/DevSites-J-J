# DevSites-J-J
💻 Desenvolvimento de Sites 🌐 Sites modernos e responsivos 🚀 Transformamos ideias em presença digital 📲 Orçamentos pelo Direct
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>J&J DEV SITES — Sua ideia. Nosso código. Seu site.</title>

  <!-- FontAwesome Ícones -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

  <style>
    :root {
      --background: #030305;
      --card: rgba(17, 17, 17, 0.7);
      --white: #ffffff;
      --text: #a0a0a0;
      --primary: #007bff;
      --neon-blue: #00e5ff;
      --border: #222222;
      --blue-glow: rgba(0, 123, 255, 0.3);
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background: linear-gradient(45deg, #020202, #000c1a, #020202);
      background-size: 400% 400%;
      animation: gradientBG 15s ease infinite;
      color: var(--white);
      line-height: 1.6;
      overflow-x: hidden;
    }

    @keyframes gradientBG {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(1120px, calc(100% - 32px));
      margin: auto;
    }

    /* REVEAL ANIMAÇÕES */
    .reveal {
      opacity: 0;
      transform: translateY(50px);
      transition: all 0.8s ease-out;
    }

    .reveal.active {
      opacity: 1;
      transform: translateY(0);
    }

    /* TOP BAR */
    .top-bar {
      background-color: #000000;
      color: var(--text);
      font-size: 12px;
      padding: 8px 5%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid var(--border);
    }
    .top-bar span i { color: var(--neon-blue); margin-right: 5px; }

    /* HEADER */
    header {
      position: sticky;
      top: 0;
      z-index: 100;
      background: rgba(5, 5, 5, 0.85);
      border-bottom: 1px solid rgba(34, 34, 34, 0.5);
      backdrop-filter: blur(12px);
    }

    .navbar {
      min-height: 75px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
    }

    .logo {
      display: flex;
      flex-direction: column;
      align-items: center;
      line-height: 1;
    }
    .logo-top { font-size: 26px; font-weight: 900; letter-spacing: 2px;}
    .logo-top span { color: var(--primary); }
    .logo-bottom { font-size: 22px; font-weight: 900; font-style: italic; letter-spacing: 1px;}
    .logo-bottom span { color: var(--primary); }

    nav {
      display: flex;
      align-items: center;
      gap: 22px;
    }

    nav a {
      font-size: 14px;
      font-weight: 500;
      text-transform: uppercase;
      letter-spacing: 1px;
      color: var(--text);
      transition: 0.3s;
    }

    nav a:hover {
      color: var(--neon-blue);
      text-shadow: 0 0 10px rgba(0, 229, 255, 0.6);
    }

    .button {
      display: inline-block;
      padding: 13px 20px;
      border: 0;
      border-radius: 6px;
      background: linear-gradient(90deg, var(--primary) 0%, #0056b3 100%);
      box-shadow: 0 4px 15px var(--blue-glow);
      color: white;
      font-weight: bold;
      text-transform: uppercase;
      letter-spacing: 1px;
      font-size: 13px;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    .button:hover {
      transform: translateY(-3px) scale(1.02);
      box-shadow: 0 8px 25px rgba(0, 123, 255, 0.6);
    }

    .button-outline {
      background: transparent;
      border: 1px solid var(--primary);
      box-shadow: none;
    }

    .button-outline:hover {
      background: rgba(0, 123, 255, 0.1);
      border-color: var(--neon-blue);
      color: var(--neon-blue);
    }

    .menu-button {
      display: none;
      border: 0;
      background: transparent;
      color: white;
      font-size: 1.8rem;
      cursor: pointer;
    }

    section { padding: 90px 0; }

    /* HERO */
    .hero-content {
      min-height: 85vh;
      display: grid;
      grid-template-columns: 1fr 1fr;
      align-items: center;
      gap: 50px;
    }

    .tag {
      display: inline-block;
      margin-bottom: 20px;
      padding: 6px 14px;
      border: 1px solid var(--primary);
      border-radius: 30px;
      color: var(--neon-blue);
      font-size: .85rem;
      font-weight: bold;
      letter-spacing: 1px;
      background: rgba(0, 123, 255, 0.1);
    }

    h1 {
      max-width: 650px;
      margin-bottom: 24px;
      font-size: clamp(2.5rem, 5vw, 4.2rem);
      line-height: 1.1;
      font-weight: 900;
      text-transform: uppercase;
    }

    .typing-cursor::after {
      content: '|';
      color: var(--neon-blue);
      animation: blink 1s step-end infinite;
    }
    @keyframes blink { 50% { opacity: 0; } }

    .hero-description {
      max-width: 600px;
      margin-bottom: 30px;
      color: var(--text);
      font-size: 1.1rem;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 15px;
    }

    @keyframes float {
      0% { transform: translateY(0px); }
      50% { transform: translateY(-15px); }
      100% { transform: translateY(0px); }
    }

    .code-window {
      padding: 20px;
      border: 1px solid var(--border);
      border-radius: 12px;
      background: rgba(5,5,5,0.9);
      box-shadow: 0 20px 50px rgba(0, 123, 255, 0.15);
      animation: float 6s ease-in-out infinite;
      backdrop-filter: blur(5px);
    }
    .code-window:hover {
      border-color: var(--primary);
      box-shadow: 0 20px 60px rgba(0, 229, 255, 0.2);
    }

    .window-top { display: flex; gap: 7px; margin-bottom: 15px; }
    .dot { width: 12px; height: 12px; border-radius: 50%; background: #ef4444; }
    .dot:nth-child(2) { background: #f59e0b; }
    .dot:nth-child(3) { background: #22c55e; }

    .code {
      color: #dbeafe;
      font-family: monospace;
      line-height: 1.8;
      font-size: 15px;
    }
    .blue { color: var(--neon-blue); }
    .purple { color: #c084fc; }
    .green { color: #86efac; }

    /* CARDS */
    .section-heading { max-width: 680px; margin-bottom: 50px; }
    .section-heading h2 { margin-bottom: 12px; font-size: clamp(1.8rem, 3.5vw, 2.5rem); font-weight: 800; text-transform: uppercase; }
    .section-heading h2 span { color: var(--primary); }
    .section-heading p { color: var(--text); }
    .center { margin: 0 auto; text-align: center; }

    .cards { display: grid; grid-template-columns: repeat(3, 1fr); gap: 25px; }

    .card {
      padding: 35px 25px;
      border: 1px solid var(--border);
      border-radius: 12px;
      background: var(--card);
      transition: all 0.4s ease;
      position: relative;
      overflow: hidden;
      backdrop-filter: blur(10px);
    }

    .card::before {
      content: '';
      position: absolute;
      top: 0; left: -100%; width: 100%; height: 2px;
      background: linear-gradient(90deg, transparent, var(--neon-blue), transparent);
      transition: 0.5s;
    }

    .card:hover {
      transform: translateY(-10px);
      border-color: rgba(0, 123, 255, 0.5);
      box-shadow: 0 15px 30px rgba(0, 123, 255, 0.1);
    }

    .card:hover::before { left: 100%; }

    .icon {
      display: grid; place-items: center;
      width: 60px; height: 60px;
      margin-bottom: 20px;
      border-radius: 12px;
      background: rgba(0, 123, 255, 0.1);
      border: 1px solid rgba(0, 123, 255, 0.3);
      color: var(--neon-blue);
      font-size: 1.6rem;
      transition: 0.4s;
    }

    .card:hover .icon {
      background: var(--primary);
      color: white;
      transform: rotateY(180deg);
    }

    .card h3 { margin-bottom: 10px; font-size: 1.3rem; }
    .card p { color: var(--text); font-size: 0.95rem; }
    .card strong { display: block; margin: 15px 0; color: var(--neon-blue); font-size: 1.6rem; font-weight: 800; }

    .check-list { display: grid; gap: 10px; margin: 15px 0 25px; color: var(--text); list-style: none; font-size: 0.9rem; }
    .check-list li::before { content: "✓"; margin-right: 8px; color: var(--neon-blue); font-weight: bold; }
    .product-card .button { width: 100%; text-align: center; }

    /* BRAND STRIP */
    .brand-strip {
      padding: 50px 0;
      background: rgba(0,0,0,0.6);
      border-top: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
      backdrop-filter: blur(5px);
    }
    .brand-strip-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 20px; text-align: center; }
    .brand-feature i { font-size: 35px; color: var(--neon-blue); margin-bottom: 10px; transition: 0.3s; }
    .brand-feature:hover i { transform: scale(1.2); color: var(--primary); }
    .brand-feature span { font-size: 13px; font-weight: 700; text-transform: uppercase; letter-spacing: 1px; }

    /* PROCESSO */
    .process { position: relative; }
    .process-list { display: grid; grid-template-columns: repeat(4, 1fr); gap: 20px; }
    .process-item { padding: 25px; background: var(--card); border: 1px solid var(--border); border-radius: 12px; transition: 0.3s; }
    .process-item:hover { border-color: var(--primary); background: rgba(0, 123, 255, 0.05); }
    .process-number {
      display: grid; place-items: center; width: 45px; height: 45px;
      margin-bottom: 15px; border-radius: 8px;
      background: linear-gradient(135deg, var(--primary), #00e5ff);
      color: #fff; font-weight: bold; font-size: 1.2rem;
    }

    /* CARRINHO */
    .cart-box { margin-top: 50px; padding: 35px; border: 1px solid var(--primary); border-radius: 12px; background: rgba(0,0,0,0.8); box-shadow: 0 10px 30px rgba(0, 123, 255, 0.1); }
    .cart-box h3 { margin-bottom: 20px; text-transform: uppercase; color: var(--neon-blue); }
    .cart-item { display: flex; justify-content: space-between; align-items: center; padding: 15px 0; border-bottom: 1px solid var(--border); }
    .cart-item small { display: block; color: var(--text); }
    .remove-item { border: 0; background: rgba(239, 68, 68, 0.1); padding: 5px 10px; border-radius: 4px; color: #ef4444; cursor: pointer; transition: 0.3s;}
    .remove-item:hover { background: #ef4444; color: white; }
    .cart-total { margin: 25px 0; text-align: right; font-size: 1.4rem; font-weight: bold; color: var(--white); }

    /* CONTATO */
    .contact-box {
      display: flex; align-items: center; justify-content: space-between; gap: 25px;
      padding: 50px; border-radius: 12px;
      background: linear-gradient(135deg, #001a3a, #020202);
      border: 1px solid var(--primary);
      box-shadow: inset 0 0 40px rgba(0, 123, 255, 0.1);
    }

    footer { padding: 30px 0; border-top: 1px solid var(--border); color: var(--text); text-align: center; font-size: 14px; background: #000; }

    /* ADMIN */
    .admin-nav-btn { border: 1px solid var(--primary); background: rgba(0,123,255,0.1); color: var(--neon-blue); border-radius: 4px; padding: 6px 12px; cursor: pointer; font-size: 12px; font-weight: 700; text-transform: uppercase; transition: 0.3s; }
    .admin-nav-btn:hover { background: var(--primary); color: white; }
    .admin-overlay { position: fixed; inset: 0; z-index: 9999; display: none; align-items: center; justify-content: center; padding: 18px; background: rgba(0,0,0,.9); backdrop-filter: blur(10px); }
    .admin-overlay.active { display: flex; }
    .admin-panel { width: min(1000px, 100%); max-height: 92vh; overflow: auto; border: 1px solid var(--primary); border-radius: 12px; background: #0a0a0a; box-shadow: 0 0 50px rgba(0, 123, 255, 0.3); padding: 28px; }
    .admin-head { display: flex; align-items: center; justify-content: space-between; gap: 16px; margin-bottom: 24px; }
    .admin-close { border: 0; background: rgba(255,255,255,.1); color: #fff; width: 40px; height: 40px; border-radius: 50%; cursor: pointer; font-size: 20px; transition: 0.3s;}
    .admin-close:hover { background: #ef4444; }
    .admin-login, .admin-content { display: none; }
    .admin-login.active, .admin-content.active { display: block; }
    .admin-login { max-width: 420px; margin: 20px auto; text-align: center; }
    .admin-login input, .admin-field input { width: 100%; box-sizing: border-box; padding: 12px 14px; margin: 8px 0 14px; border-radius: 6px; border: 1px solid var(--border); background: #111; color: #fff; outline: none; transition: 0.3s;}
    .admin-login input:focus, .admin-field input:focus { border-color: var(--primary); }
    .admin-grid { display: grid; grid-template-columns: repeat(2, minmax(0, 1fr)); gap: 18px; }
    .admin-card { padding: 20px; border: 1px solid var(--border); border-radius: 8px; background: rgba(20,20,20,0.8); }
    .admin-actions { display: flex; flex-wrap: wrap; gap: 10px; margin-top: 18px; }
    .admin-message { min-height: 20px; margin: 8px 0 0; color: var(--neon-blue); font-size: .92rem; }
    .order-row { padding: 12px 0; border-bottom: 1px solid var(--border); }
    .order-row small { color: var(--text); display: block; }
    .danger-btn { border: 1px solid rgba(248,113,113,.4); background: rgba(127,29,29,.22); color: #fecaca; cursor: pointer; }
    .admin-stats { display: grid; grid-template-columns: repeat(3, 1fr); gap: 15px; margin-top: 10px; }
    .admin-stat { padding: 20px 10px; border: 1px solid rgba(0, 123, 255, 0.3); border-radius: 8px; background: rgba(0, 123, 255, 0.05); text-align: center; }
    .admin-stat strong { display: block; font-size: 1.5rem; color: var(--neon-blue); }
    .product-admin-row { display: flex; justify-content: space-between; align-items: center; gap: 10px; padding: 10px 0; border-bottom: 1px solid var(--border); }
    .promo-badge { padding: 4px 8px; border-radius: 4px; background: rgba(0, 229, 255, 0.1); border: 1px solid var(--neon-blue); color: var(--neon-blue); font-size: .72rem; font-weight: 800; animation: pulse 2s infinite;}

    @keyframes pulse { 0% { opacity: 1; } 50% { opacity: 0.6; } 100% { opacity: 1; } }

    @media (max-width: 800px) {
      header nav { display: none; position: absolute; top: 75px; left: 0; right: 0; padding: 20px; flex-direction: column; background: rgba(0,0,0,0.95); backdrop-filter: blur(10px); }
      header nav.active { display: flex; }
      header > .container > .button { display: none; }
      .menu-button { display: block; }
      .hero-content { grid-template-columns: 1fr; min-height: auto; padding: 40px 0; text-align: center; }
      .hero-actions { justify-content: center; }
      .brand-strip-grid, .admin-grid { grid-template-columns: repeat(2, 1fr); }
      .cards, .process-list, .admin-stats { grid-template-columns: 1fr; }
      .contact-box { flex-direction: column; text-align: center; }
    }
  </style>
</head>

<body>
  <div class="top-bar">
    <span><i class="fa-solid fa-code"></i> Inovação e Alta Performance</span>
    <span><i class="fa-solid fa-headset"></i> Suporte 24/7</span>
  </div>

  <header>
    <div class="container navbar">
      <a href="#inicio" class="logo">
        <div class="logo-top"><span>J</span>&<span>J</span></div>
        <div class="logo-bottom">DEV<span>SITES</span></div>
      </a>
      <button class="menu-button" id="menuButton" aria-label="Abrir Menu" aria-expanded="false">☰</button>
      <nav id="menu">
        <a href="#servicos">Serviços</a>
        <a href="#produtos">Produtos</a>
        <a href="#processo">Metodologia</a>
        <a href="#contato">Contato</a>
        <button type="button" class="admin-nav-btn" id="openAdmin">⚙️ Admin</button>
      </nav>
      <a href="#contato" class="button">Quero vender mais</a>
    </div>
  </header>

  <main>
    <section id="inicio">
      <div class="container hero-content">
        <div class="reveal">
          <span class="tag"><i class="fa-solid fa-rocket"></i> DESENVOLVIMENTO WEB PROFISSIONAL</span>
          <h1>
            Sua ideia.<br>
            <span id="typing-text" class="typing-cursor"></span><br>
            Seu site.
          </h1>
          <p class="hero-description">
            Criamos experiências digitais rápidas, imersivas e otimizadas. Transforme visitantes em clientes com um design moderno feito sob medida para você.
          </p>
          <div class="hero-actions">
            <a href="#contato" class="button"><i class="fa-solid fa-paper-plane"></i> Iniciar Projeto</a>
            <a href="#produtos" class="button button-outline">Ver Planos</a>
          </div>
        </div>

        <div class="code-window reveal" style="transition-delay: 0.2s;">
          <div class="window-top">
            <span class="dot"></span><span class="dot"></span><span class="dot"></span>
          </div>
          <div class="code">
            <span class="blue">const</span> <span class="purple">empresa</span> = <span class="blue">new</span> <span class="green">NegocioDigital</span>();<br><br>
            <span class="blue">function</span> <span class="purple">decolar</span>() {<br>
            &nbsp;&nbsp;empresa.<span class="purple">adicionarSite</span>(<span class="green">"J&J Devsites"</span>);<br>
            &nbsp;&nbsp;<span class="blue">return</span> <span class="green">"Vendas multiplicadas 🚀"</span>;<br>
            }<br><br>
            <span class="purple">decolar</span>();
          </div>
        </div>
      </div>
    </section>

    <section class="brand-strip reveal" aria-label="Diferenciais J&J Devsites">
      <div class="container brand-strip-grid">
        <div class="brand-feature">
          <i class="fa-solid fa-desktop"></i>
          <span>100% Responsivos</span>
        </div>
        <div class="brand-feature">
          <i class="fa-solid fa-gauge-high"></i>
          <span>Ultrarrápidos</span>
        </div>
        <div class="brand-feature">
          <i class="fa-solid fa-shield-halved"></i>
          <span>Máxima Segurança</span>
        </div>
        <div class="brand-feature">
          <i class="fa-solid fa-ranking-star"></i>
          <span>SEO Otimizado</span>
        </div>
      </div>
    </section>

    <section id="servicos">
      <div class="container">
        <div class="section-heading center reveal">
          <h2>Engenharia digital com a identidade <span>J&J</span></h2>
          <p>Não construímos apenas sites, criamos máquinas de conversão para o seu negócio.</p>
        </div>

        <div class="cards">
          <article class="card reveal" style="transition-delay: 0.1s;">
            <div class="icon"><i class="fa-solid fa-bolt"></i></div>
            <h3>Performance Máxima</h3>
            <p>Carregamento instantâneo. Código limpo e otimizado para não deixar seu cliente esperando.</p>
          </article>
          <article class="card reveal" style="transition-delay: 0.2s;">
            <div class="icon"><i class="fa-solid fa-bullseye"></i></div>
            <h3>Foco em Conversão</h3>
            <p>UI/UX Design estratégico posicionado para guiar o usuário diretamente para a compra ou contato.</p>
          </article>
          <article class="card reveal" style="transition-delay: 0.3s;">
            <div class="icon"><i class="fa-solid fa-mobile-screen-button"></i></div>
            <h3>Mobile First</h3>
            <p>Mais de 70% dos acessos são pelo celular. Seu site será impecável em qualquer tela.</p>
          </article>
        </div>
      </div>
    </section>

    <section id="produtos">
      <div class="container">
        <div class="section-heading center reveal">
          <h2>Escolha a <span>Sua Solução</span></h2>
          <p>Adicione ao carrinho e monte o pacote ideal para sua empresa.</p>
        </div>

        <div class="cards reveal" id="productGrid">
          <article class="card product-card">
            <div class="icon"><i class="fa-solid fa-globe"></i></div>
            <h3>Site Simples</h3>
            <p>Página objetiva e elegante para marcar presença na web.</p>
            <strong>R$ 150,00</strong>
            <ul class="check-list">
              <li>Layout responsivo</li>
              <li>Botão para WhatsApp</li>
              <li>Hospedagem e setup</li>
            </ul>
            <button type="button" class="button add-cart" data-id="simple" data-name="Site Simples" data-price="150">Adicionar ao carrinho</button>
          </article>

          <article class="card product-card">
            <div class="icon"><i class="fa-solid fa-palette"></i></div>
            <h3>Site Personalizado</h3>
            <p>Design exclusivo moldado com a identidade da sua marca.</p>
            <strong>R$ 300,00</strong>
            <ul class="check-list">
              <li>Design sob medida</li>
              <li>Animações modernas</li>
              <li>Integrações essenciais</li>
            </ul>
            <button type="button" class="button add-cart" data-id="custom" data-name="Site Personalizado" data-price="300">Adicionar ao carrinho</button>
          </article>

          <article class="card product-card">
            <div class="icon"><i class="fa-solid fa-trophy"></i></div>
            <h3>Site Oficial</h3>
            <p>Projeto avançado para líderes de mercado e alta conversão.</p>
            <strong>R$ 450,00</strong>
            <ul class="check-list">
              <li>Múltiplas páginas</li>
              <li>Painel administrador</li>
              <li>Otimização Avançada (SEO)</li>
            </ul>
            <button type="button" class="button add-cart" data-id="official" data-name="Site Oficial" data-price="450">Adicionar ao carrinho</button>
          </article>

          <article class="card product-card">
            <div class="icon"><i class="fa-solid fa-screwdriver-wrench"></i></div>
            <h3>Plano Mensal + Suporte 24h</h3>
            <p>Tranquilidade total. Nós cuidamos do seu site enquanto você foca no negócio.</p>
            <strong>R$ 50,00 / mês</strong>
            <ul class="check-list">
              <li>Suporte técnico 24/7</li>
              <li>Backups diários</li>
              <li>Atualizações de conteúdo</li>
            </ul>
            <button type="button" class="button add-cart" data-id="monthly" data-name="Plano Mensal + Suporte 24h" data-price="50">Adicionar plano</button>
          </article>
        </div>

        <div class="cart-box reveal">
          <h3><i class="fa-solid fa-cart-shopping"></i> Seu Projeto (Carrinho)</h3>
          <div id="cartItems"><p style="color: var(--text);">Seu carrinho está vazio.</p></div>
          <div class="cart-total">Investimento: <span id="cartTotal" style="color:var(--neon-blue);">R$ 0,00</span></div>
          <div style="display: flex; gap: 10px; flex-wrap: wrap;">
            <button type="button" class="button" id="whatsappCart"><i class="fa-brands fa-whatsapp"></i> Finalizar Pedido</button>
            <button type="button" class="button button-outline" id="clearCart">Esvaziar</button>
          </div>
        </div>
      </div>
    </section>

    <section id="processo" class="process">
      <div class="container">
        <div class="section-heading reveal">
          <h2>Nossa <span>Metodologia</span></h2>
          <p>Transparência e agilidade do primeiro contato ao site no ar.</p>
        </div>
        <div class="process-list">
          <div class="process-item reveal" style="transition-delay: 0.1s;">
            <div class="process-number">01</div>
            <h3>Descoberta</h3>
            <p>Reunião de briefing para mapear seus objetivos e público-alvo.</p>
          </div>
          <div class="process-item reveal" style="transition-delay: 0.2s;">
            <div class="process-number">02</div>
            <h3>Design UI/UX</h3>
            <p>Criação do protótipo visual focado na melhor experiência.</p>
          </div>
          <div class="process-item reveal" style="transition-delay: 0.3s;">
            <div class="process-number">03</div>
            <h3>Código Limpo</h3>
            <p>Desenvolvimento ágil utilizando as melhores tecnologias web.</p>
          </div>
          <div class="process-item reveal" style="transition-delay: 0.4s;">
            <div class="process-number">04</div>
            <h3>Lançamento</h3>
            <p>Testes rigorosos e entrega do site rápido, seguro e no ar.</p>
          </div>
        </div>
      </div>
    </section>

    <section id="contato">
      <div class="container reveal">
        <div class="contact-box">
          <div>
            <h2 style="margin-bottom: 10px; font-size: 2rem;">Vamos dominar o digital?</h2>
            <p style="color: var(--text); font-size: 1.1rem;">Nossa equipe está pronta para transformar sua ideia no melhor site do seu nicho.</p>
          </div>
          <a class="button" href="https://wa.me/5500000000000" target="_blank" style="padding: 18px 30px; font-size: 1.1rem;">
            <i class="fa-brands fa-whatsapp" style="font-size: 1.3rem; margin-right: 8px;"></i> Falar com Especialista
          </a>
        </div>
      </div>
    </section>
  </main>

  <footer>
    © 2026 J&J DEV SITES. Todos os direitos reservados.
  </footer>

  <div class="admin-overlay" id="adminOverlay" aria-hidden="true">
    <div class="admin-panel">
      <div class="admin-head">
        <div>
          <h2>⚙️ Painel de Controle</h2>
          <p style="color:var(--text); font-size:0.9rem;">Gerencie preços, produtos, métricas e contatos localmente.</p>
        </div>
        <button class="admin-close" id="closeAdmin" aria-label="Fechar Painel">×</button>
      </div>

      <div class="admin-login active" id="adminLogin">
        <h3>Autenticação Restrita</h3>
        <p style="color:var(--text); margin-bottom: 15px;">Insira sua credencial administrativa.</p>
        <input id="adminPassword" type="password" placeholder="Senha: 1234">
        <button class="button" id="adminLoginBtn" style="width: 100%; margin-top: 10px;">Acessar Sistema</button>
        <p class="admin-message" id="adminLoginMsg"></p>
      </div>

      <div class="admin-content" id="adminContent">
        <div class="admin-grid">
          <div class="admin-card">
            <h3 style="margin-bottom: 15px; color: var(--neon-blue);">💰 Tabela de Preços (Base)</h3>
            <div class="admin-field">
              <label for="priceSimple">Site Simples</label><input id="priceSimple" type="number" step="0.01">
              <label for="priceCustom">Site Personalizado</label><input id="priceCustom" type="number" step="0.01">
              <label for="priceOfficial">Site Oficial</label><input id="priceOfficial" type="number" step="0.01">
              <label for="priceMonthly">Plano Mensal</label><input id="priceMonthly" type="number" step="0.01">
            </div>
            <button class="button button-outline" id="savePrices" style="width: 100%;">Atualizar Preços</button>
          </div>

          <div class="admin-card">
            <h3 style="margin-bottom: 15px; color: var(--neon-blue);">📞 Dados de Contato</h3>
            <div class="admin-field">
              <label for="adminWhatsapp">WhatsApp (DDI + DDD + Núm)</label>
              <input id="adminWhatsapp" type="text" placeholder="5511999999999">
              <label for="adminInstagram">Instagram / Outros</label>
              <input id="adminInstagram" type="text" placeholder="@jjdevsites">
            </div>
            <button class="button button-outline" id="saveBusiness" style="width: 100%;">Salvar Contato</button>
          </div>

          <div class="admin-card">
            <h3 style="margin-bottom: 15px; color: var(--neon-blue);">🛍️ Adicionar Serviço/Produto</h3>
            <div class="admin-field">
              <label for="newProductName">Nome do Serviço</label><input id="newProductName" type="text" placeholder="Ex: Landing Page">
              <label for="newProductPrice">Preço Padrão (R$)</label><input id="newProductPrice" type="number" step="0.01">
              <label for="newProductCategory">Categoria</label><input id="newProductCategory" type="text" placeholder="Sites">
              <label for="newProductPromo">Preço Promo (Opcional)</label><input id="newProductPromo" type="number" step="0.01">
            </div>
            <button class="button" id="addProduct" style="width: 100%;">Cadastrar</button>
            <div id="productAdminList" style="margin-top:20px;"></div>
          </div>

          <div class="admin-card">
            <h3 style="margin-bottom: 15px; color: var(--neon-blue);">📦 Histórico de Leads</h3>
            <div id="adminOrders" style="max-height: 250px; overflow-y: auto; padding-right: 5px;"></div>
            <button class="button danger-btn" id="clearOrders" style="width: 100%; margin-top:15px;">Limpar Histórico</button>
          </div>

          <div class="admin-card" style="grid-column: 1 / -1; border-color: rgba(0, 123, 255, 0.4);">
            <h3 style="margin-bottom: 15px; color: var(--neon-blue);">📊 Inteligência de Vendas</h3>
            <div class="admin-stats">
              <div class="admin-stat"><strong id="statOrders">0</strong><span style="color:var(--text); font-size:0.8rem; text-transform:uppercase;">Leads Gerados</span></div>
              <div class="admin-stat"><strong id="statRevenue">R$ 0,00</strong><span style="color:var(--text); font-size:0.8rem; text-transform:uppercase;">Volume Financeiro</span></div>
              <div class="admin-stat"><strong id="statAverage">R$ 0,00</strong><span style="color:var(--text); font-size:0.8rem; text-transform:uppercase;">Ticket Médio</span></div>
            </div>
            <div class="admin-actions" style="margin-top: 20px; justify-content: flex-end;">
              <button class="button button-outline" id="refreshDashboard">Recarregar Painel</button>
              <button class="button danger-btn" id="logoutAdmin">Encerrar Sessão</button>
            </div>
          </div>
        </div>
        <p class="admin-message" id="adminMsg" style="text-align: center; font-size: 1.1rem;"></p>
      </div>
    </div>
  </div>

  <script>
    // 1. Typing Effect
    const textToType = "Nosso código.";
    const typeElement = document.getElementById('typing-text');
    let typeIndex = 0;

    function typeWriter() {
      if (typeIndex < textToType.length) {
        typeElement.innerHTML += textToType.charAt(typeIndex);
        typeIndex++;
        setTimeout(typeWriter, 120);
      } else {
        setTimeout(() => {
          typeElement.innerHTML = "";
          typeIndex = 0;
          typeWriter();
        }, 4000);
      }
    }
    setTimeout(typeWriter, 500);

    // 2. Scroll Animation
    const revealElements = document.querySelectorAll('.reveal');
    const scrollObserver = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if(entry.isIntersecting) {
          entry.target.classList.add('active');
        }
      });
    }, { threshold: 0.15 });

    revealElements.forEach(el => scrollObserver.observe(el));

    // 3. Mobile Menu
    const menuButton = document.getElementById("menuButton");
    const menu = document.getElementById("menu");
    menuButton.addEventListener("click", () => {
      const isActive = menu.classList.toggle("active");
      menuButton.setAttribute("aria-expanded", isActive);
    });
    document.querySelectorAll('#menu a').forEach(link => {
      link.addEventListener("click", () => {
        menu.classList.remove("active");
        menuButton.setAttribute("aria-expanded", "false");
      });
    });

    // 4. Carrinho de Compras
    const cart = [];
    window.__jjCart = cart;
    const formatMoney = (val) => Number(val||0).toLocaleString("pt-BR", {style: "currency", currency: "BRL"});

    function renderCart() {
      const box = document.getElementById("cartItems");
      const tot = document.getElementById("cartTotal");
      if (!cart.length) {
        box.innerHTML = '<p style="color: var(--text);">Seu carrinho está vazio.</p>';
        tot.textContent = formatMoney(0);
        return;
      }
      box.innerHTML = cart.map((item, i) => `
        <div class="cart-item">
          <div>
            <strong style="color:var(--white);">${item.name}</strong>
            <small>Qtd: ${item.quantity} | Sub: ${formatMoney(item.price * item.quantity)}</small>
          </div>
          <button class="remove-item" onclick="window.__jjRemoveCartItem(${i})"><i class="fa-solid fa-trash"></i></button>
        </div>
      `).join("");
      tot.textContent = formatMoney(cart.reduce((s, i) => s + (i.price * i.quantity), 0));
    }

    window.__jjRemoveCartItem = (index) => {
      cart.splice(index, 1);
      renderCart();
    };

    document.getElementById("clearCart").addEventListener("click", () => {
      cart.length = 0;
      renderCart();
    });

    // Delegação Global para Inclusão no Carrinho
    document.addEventListener("click", (e) => {
      const btn = e.target.closest(".add-cart");
      if (btn) {
        const nm = btn.dataset.name;
        const pr = Number(btn.dataset.price);
        const ex = cart.find(i => i.name === nm);
        if(ex) ex.quantity++; else cart.push({name: nm, price: pr, quantity: 1});
        renderCart();
        alert("✅ Adicionado ao projeto!");
      }
    });

    // 5. Back-Office / Admin
    (() => {
      const PASS="2001", PRODUCT_KEY="jjProducts", ORDER_KEY="jjOrders", SETTINGS_KEY="jjSettings";
      const defaults = { simple:150, custom:300, official:450, monthly:50, whatsapp:"5500000000000", instagram:"" };
      const defaultProducts = [
        {id:"simple", name:"Site Simples", price:150, category:"Sites Básicos"},
        {id:"custom", name:"Site Personalizado", price:300, category:"Sites Intermediários"},
        {id:"official", name:"Site Oficial", price:450, category:"Projetos Avançados"},
        {id:"monthly", name:"Plano Mensal + Suporte 24h", price:50, category:"Assinaturas"}
      ];

      const getSettings = () => ({...defaults, ...JSON.parse(localStorage.getItem(SETTINGS_KEY)||"{}")});
      const saveSettings = (s) => localStorage.setItem(SETTINGS_KEY, JSON.stringify(s));

      function getProducts() {
        try {
          const s = JSON.parse(localStorage.getItem(PRODUCT_KEY));
          return Array.isArray(s) && s.length ? s : defaultProducts;
        } catch {
          return defaultProducts;
        }
      }
      const saveProducts = (p) => localStorage.setItem(PRODUCT_KEY, JSON.stringify(p));

      const overlay = document.getElementById("adminOverlay");
      document.getElementById("openAdmin").onclick = () => {
        overlay.classList.add("active");
        overlay.setAttribute("aria-hidden", "false");
        document.getElementById("adminPassword").focus();
      };

      const closeAdminPanel = () => {
        overlay.classList.remove("active");
        overlay.setAttribute("aria-hidden", "true");
      };

      document.getElementById("closeAdmin").onclick = closeAdminPanel;

      document.getElementById("adminLoginBtn").onclick = () => {
        if(document.getElementById("adminPassword").value === PASS) {
          document.getElementById("adminLogin").classList.remove("active");
          document.getElementById("adminContent").classList.add("active");
          document.getElementById("adminLoginMsg").textContent = "";
          loadAdminData();
        } else {
          document.getElementById("adminLoginMsg").textContent = "❌ Senha incorreta!";
        }
      };

      document.getElementById("adminPassword").onkeydown = (e) => {
        if(e.key==="Enter") document.getElementById("adminLoginBtn").click();
      };

      document.getElementById("logoutAdmin").onclick = () => {
        document.getElementById("adminContent").classList.remove("active");
        document.getElementById("adminLogin").classList.add("active");
        document.getElementById("adminPassword").value = "";
        closeAdminPanel();
      };

      function notifyMsg(text) {
        const m = document.getElementById("adminMsg");
        m.textContent = text;
        setTimeout(()=> m.textContent="", 3000);
      }

      function loadAdminData() {
        const s = getSettings();
        document.getElementById("priceSimple").value = s.simple;
        document.getElementById("priceCustom").value = s.custom;
        document.getElementById("priceOfficial").value = s.official;
        document.getElementById("priceMonthly").value = s.monthly;
        document.getElementById("adminWhatsapp").value = s.whatsapp;
        document.getElementById("adminInstagram").value = s.instagram;
        renderProductAdmin();
        renderDashboard();
      }

      document.getElementById("savePrices").onclick = () => {
        const s = getSettings();
        s.simple = +document.getElementById("priceSimple").value||0;
        s.custom = +document.getElementById("priceCustom").value||0;
        s.official = +document.getElementById("priceOfficial").value||0;
        s.monthly = +document.getElementById("priceMonthly").value||0;
        saveSettings(s);
        syncPricesToProducts(s);
        notifyMsg("✅ Preços atualizados com sucesso!");
      };

      document.getElementById("saveBusiness").onclick = () => {
        const s = getSettings();
        s.whatsapp = document.getElementById("adminWhatsapp").value.trim();
        s.instagram = document.getElementById("adminInstagram").value.trim();
        saveSettings(s);
        updateLinks();
        notifyMsg("✅ Contatos atualizados!");
      };

      function syncPricesToProducts(s) {
        const p = getProducts();
        p.forEach(x => {
          if(x.id==="simple") x.price = s.simple;
          if(x.id==="custom") x.price = s.custom;
          if(x.id==="official") x.price = s.official;
          if(x.id==="monthly") x.price = s.monthly;
        });
        saveProducts(p);
        renderProductAdmin();
        updatePublicStore();
      }

      function updateLinks() {
        const w = getSettings().whatsapp || defaults.whatsapp;
        document.querySelectorAll('a[href*="wa.me/"]').forEach(a => a.href = `https://wa.me/${w}`);
      }

      document.getElementById("addProduct").onclick = () => {
        const n = document.getElementById("newProductName").value.trim();
        const p = Number(document.getElementById("newProductPrice").value);
        const c = document.getElementById("newProductCategory").value.trim() || "Novos";
        const pr = Number(document.getElementById("newProductPromo").value);
        if(!n || !p) return alert("Insira o nome e o preço base.");

        const prods = getProducts();
        const newItem = { id:"p_"+Date.now(), name:n, price:p, category:c };
        if(pr > 0 && pr < p) newItem.promoPrice = pr;
        prods.push(newItem);
        saveProducts(prods);

        document.getElementById("newProductName").value="";
        document.getElementById("newProductPrice").value="";
        document.getElementById("newProductCategory").value="";
        document.getElementById("newProductPromo").value="";

        renderProductAdmin();
        updatePublicStore();
        notifyMsg("✅ Serviço cadastrado na vitrine!");
      };

      window.togglePromo = (idx) => {
        const p = getProducts();
        if(p[idx].promoPrice) {
          delete p[idx].promoPrice;
        } else {
          let val = prompt("Digite o novo valor promocional:");
          if(val) {
            val = Number(val.replace(",","."));
            if(val>0 && val<p[idx].price) p[idx].promoPrice = val; else alert("Valor inválido.");
          }
        }
        saveProducts(p); renderProductAdmin(); updatePublicStore();
      };

      window.delProduct = (idx) => {
        const p = getProducts();
        if(["simple","custom","official","monthly"].includes(p[idx].id)) return alert("Produtos base não podem ser deletados.");
        if(confirm("Remover este serviço?")) { p.splice(idx,1); saveProducts(p); renderProductAdmin(); updatePublicStore(); }
      };

      function renderProductAdmin() {
        const box = document.getElementById("productAdminList");
        if(!box) return;
        box.innerHTML = getProducts().map((p, i) => `
          <div class="product-admin-row">
            <div><strong style="color:#fff">${p.name}</strong><small>${p.category} | Base: ${formatMoney(p.price)} ${p.promoPrice?`| Promo: ${formatMoney(p.promoPrice)}`:""}</small></div>
            <div style="display:flex;gap:5px;">
              <button class="admin-nav-btn" onclick="window.togglePromo(${i})">${p.promoPrice?"Tirar Promo":"Dar Promo"}</button>
              ${["simple","custom","official","monthly"].includes(p.id)?"":`<button class="danger-btn" style="border-radius:4px;padding:5px;" onclick="window.delProduct(${i})"><i class="fa-solid fa-trash"></i></button>`}
            </div>
          </div>
        `).join("");
      }

      function updatePublicStore() {
        const grid = document.getElementById("productGrid");
        if(!grid) return;
        const prods = getProducts();

        prods.filter(p => ["simple","custom","official","monthly"].includes(p.id)).forEach(p => {
          const btn = document.querySelector(`button[data-id="${p.id}"]`);
          if(btn) {
            const finalPrice = p.promoPrice || p.price;
            btn.dataset.price = finalPrice;
            const card = btn.closest('.card');
            const strong = card.querySelector('strong');
            if(p.promoPrice) {
              strong.innerHTML = `<span style="text-decoration:line-through; font-size:1rem; color:var(--text); margin-right:8px;">${formatMoney(p.price)}</span>${formatMoney(p.promoPrice)} <br><span class="promo-badge">🔥 PROMO ATIVA</span>`;
            } else {
              strong.textContent = formatMoney(p.price) + (p.id==='monthly' ? ' / mês' : '');
            }
          }
        });

        const customs = prods.filter(p => !["simple","custom","official","monthly"].includes(p.id));
        customs.forEach(p => {
          const existingCard = document.querySelector(`[data-custom-id="${p.id}"]`);
          const finalPrice = p.promoPrice || p.price;

          if(existingCard) {
            existingCard.querySelector('button').dataset.price = finalPrice;
            const strong = existingCard.querySelector('strong');
            strong.innerHTML = p.promoPrice ?
              `<span style="text-decoration:line-through; font-size:1rem; color:var(--text); margin-right:8px;">${formatMoney(p.price)}</span>${formatMoney(p.promoPrice)} <br><span class="promo-badge">🔥 PROMO ATIVA</span>` :
              formatMoney(p.price);
          } else {
            const card = document.createElement("article");
            card.className = "card product-card reveal active";
            card.dataset.customId = p.id;
            card.innerHTML = `
              <div class="icon"><i class="fa-solid fa-layer-group"></i></div>
              <h3>${p.name}</h3><p>${p.category}</p>
              <strong style="margin: 15px 0; display:block; color:var(--neon-blue); font-size:1.6rem;">
                ${p.promoPrice ? `<span style="text-decoration:line-through; font-size:1rem; color:var(--text); margin-right:8px;">${formatMoney(p.price)}</span>${formatMoney(p.promoPrice)} <br><span class="promo-badge">🔥 PROMO ATIVA</span>` : formatMoney(p.price)}
              </strong>
              <button type="button" class="button add-cart" data-id="${p.id}" data-name="${p.name}" data-price="${finalPrice}">Adicionar</button>
            `;
            grid.appendChild(card);
          }
        });
      }

      function renderDashboard() {
        let orders = [];
        try { orders = JSON.parse(localStorage.getItem(ORDER_KEY)||"[]"); } catch {}

        const rev = orders.reduce((s,o)=>s+o.val, 0);
        document.getElementById("statOrders").textContent = orders.length;
        document.getElementById("statRevenue").textContent = formatMoney(rev);
        document.getElementById("statAverage").textContent = formatMoney(orders.length ? rev/orders.length : 0);

        const list = document.getElementById("adminOrders");
        if(!orders.length) list.innerHTML = '<p style="color:var(--text);">Nenhum lead registrado.</p>';
        else list.innerHTML = orders.map((o,i) => `
          <div class="order-row">
            <strong style="color:var(--white);">Lead #${orders.length - i} — ${formatMoney(o.val)}</strong>
            <small>${o.date}</small>
            <small style="color:var(--primary);">${o.desc}</small>
          </div>
        `).reverse().join("");
      }

      document.getElementById("refreshDashboard").onclick = () => { renderDashboard(); notifyMsg("🔄 Dados atualizados."); };
      document.getElementById("clearOrders").onclick = () => {
        if(confirm("Apagar todo o histórico financeiro do navegador?")) { localStorage.removeItem(ORDER_KEY); renderDashboard(); }
      };

      document.getElementById("whatsappCart").addEventListener("click", () => {
        if(!cart.length) return alert("Selecione um plano primeiro.");

        const total = cart.reduce((s,i)=>s+(i.price*i.quantity),0);
        const desc = cart.map(i=>`▪ ${i.name} (x${i.quantity})`).join("\n");

        let o = []; try { o=JSON.parse(localStorage.getItem(ORDER_KEY)||"[]"); } catch {}
        o.push({ date: new Date().toLocaleString("pt-BR"), val: total, desc: cart.map(i=>i.name).join(", ") });
        localStorage.setItem(ORDER_KEY, JSON.stringify(o));
        renderDashboard();

        const wpp = getSettings().whatsapp || defaults.whatsapp;
        const msg = `🚀 Olá, equipe J&J Devsites!\n\nQuero iniciar um projeto com as seguintes soluções:\n\n${desc}\n\n*Investimento Previsto:* ${formatMoney(total)}\n\nPodemos iniciar o planejamento?`;
        window.open(`https://wa.me/${wpp}?text=${encodeURIComponent(msg)}`, "_blank");
      });

      updateLinks();
      updatePublicStore();
    })();
  </script>
</body>
</html>
