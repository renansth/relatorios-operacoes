# relatorios-operacoes
Relatório Diários para colaboradores da qualidade relatar como foi seu dia e registrar evidencias 
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Relatórios Diários - Operações & Gestão de Turnos | Mercado Livre</title>
  
  <!-- Tailwind CSS & Lucide Icons -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://unpkg.com/lucide@latest"></script>

  <style>
    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      background-color: #F5F5F5;
      color: #334155;
    }
    .meli-yellow { background-color: #FFE600; }
    .meli-blue { background-color: #1A4BDB; }
    .meli-blue-hover:hover { background-color: #153bb0; }
    .card-shadow { box-shadow: 0 2px 8px -2px rgba(0, 0, 0, 0.08), 0 1px 4px -1px rgba(0, 0, 0, 0.04); }
  </style>
</head>
<body class="min-h-screen flex flex-col relative pb-24">

  <!-- ==================== TELA DE ENTRADA / SSO GRID ==================== -->
  <div id="telaLogin" class="min-h-screen flex flex-col justify-between">
    <header class="meli-yellow border-b border-amber-300 py-3 px-6 shadow-sm">
      <div class="max-w-6xl mx-auto flex items-center justify-between">
        <div class="flex items-center gap-3">
          <div class="w-10 h-10 meli-blue rounded-lg flex items-center justify-center text-white font-black text-xl shadow">M</div>
          <div>
            <span class="font-extrabold tracking-tight text-[#1A4BDB] text-lg block leading-none">mercado livre</span>
            <span class="text-[11px] font-semibold text-slate-700 tracking-wider uppercase">Operações & Gestão de Turnos • GRID</span>
          </div>
        </div>
        <div class="flex items-center gap-2 bg-yellow-200/80 px-3 py-1 rounded-full text-xs font-semibold text-slate-800">
          <i data-lucide="shield-check" class="w-4 h-4 text-[#1A4BDB]"></i>
          Rede Corporativa Segura
        </div>
      </div>
    </header>

    <main class="flex-1 flex items-center justify-center p-4">
      <div class="w-full max-w-md bg-white rounded-2xl shadow-xl border border-slate-200 overflow-hidden">
        <div class="meli-blue text-white p-6 text-center">
          <div class="w-14 h-14 meli-yellow text-[#1A4BDB] rounded-2xl mx-auto flex items-center justify-center font-black text-2xl shadow-md mb-3">
            <i data-lucide="file-text" class="w-8 h-8 text-[#1A4BDB]"></i>
          </div>
          <h1 class="text-xl font-bold tracking-tight">Portal de Relatórios Diários</h1>
          <p class="text-blue-100 text-xs mt-1">Acompanhamento Operacional, Auditoria 5S & Escalas</p>
        </div>

        <div class="p-6 sm:p-8 space-y-6">
          <div class="bg-amber-50 border border-amber-200 rounded-xl p-3.5 text-xs text-amber-900 flex items-start gap-3">
            <i data-lucide="info" class="w-5 h-5 text-amber-600 shrink-0 mt-0.5"></i>
            <div>
              <strong class="font-semibold block mb-0.5">Acesso Restrito GRID / Google SSO</strong>
              Exclusivo para e-mails autenticados com o domínio corporativo <strong>@mercadolivre.com</strong>.
            </div>
          </div>

          <!-- Botão Único com o seu acesso pronto -->
          <button onclick="fazerLogin('renansth.missias@mercadolivre.com')" class="w-full bg-white hover:bg-slate-50 text-slate-700 font-semibold py-3.5 px-4 border-2 border-slate-300 hover:border-[#1A4BDB] rounded-xl shadow-sm transition flex items-center justify-center gap-3">
            <svg class="w-5 h-5" viewBox="0 0 24 24">
              <path fill="#4285F4" d="M22.56 12.25c0-.78-.07-1.53-.2-2.25H12v4.26h5.92c-.26 1.37-1.04 2.53-2.21 3.31v2.77h3.57c2.08-1.92 3.28-4.74 3.28-8.09z"/>
              <path fill="#34A853" d="M12 23c2.97 0 5.46-.98 7.28-2.66l-3.57-2.77c-.98.66-2.23 1.06-3.71 1.06-2.86 0-5.29-1.93-6.16-4.53H2.18v2.84C3.99 20.53 7.7 23 12 23z"/>
              <path fill="#FBBC05" d="M5.84 14.09c-.22-.66-.35-1.36-.35-2.09s.13-1.43.35-2.09V7.06H2.18C1.43 8.55 1 10.22 1 12s.43 3.45 1.18 4.94l2.85-2.22.81-.63z"/>
              <path fill="#EA4335" d="M12 5.38c1.62 0 3.06.56 4.21 1.64l3.15-3.15C17.45 2.09 14.97 1 12 1 7.7 1 3.99 3.47 2.18 7.06l3.66 2.84c.87-2.6 3.3-4.52 6.16-4.52z"/>
            </svg>
            <span class="text-xs font-bold text-slate-800">Entrar como renansth.missias@mercadolivre.com</span>
          </button>

          <!-- Campo para novos operadores da sua equipe -->
          <div class="pt-4 border-t border-slate-200">
            <form onsubmit="event.preventDefault(); fazerLogin(document.getElementById('inputEmailLivre').value);" class="space-y-2">
              <label class="text-[11px] font-semibold text-slate-500 block">Outro colaborador da equipe (@mercadolivre.com):</label>
              <div class="flex gap-2">
                <input id="inputEmailLivre" type="email" placeholder="operador@mercadolivre.com" class="flex-1 text-xs px-3 py-2 border border-slate-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-[#1A4BDB]">
                <button type="submit" class="bg-slate-800 text-white text-xs px-3 py-2 rounded-lg font-semibold hover:bg-slate-900 transition">Acessar</button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </main>
  </div>

  <!-- ==================== APLICAÇÃO PRINCIPAL ==================== -->
  <div id="telaApp" class="hidden flex-1 flex flex-col">
    <!-- Cabeçalho -->
    <header class="meli-yellow border-b border-amber-300 px-4 py-3 sticky top-0 z-30 shadow-sm">
      <div class="max-w-6xl mx-auto flex flex-col md:flex-row md:items-center md:justify-between gap-3">
        <div class="flex items-center gap-2">
          <div class="bg-[#1A4BDB] text-white text-xs font-black px-2.5 py-1 rounded tracking-wide shadow-sm">GRID</div>
          <div>
            <h1 class="font-extrabold text-slate-900 text-sm md:text-base leading-tight">Relatórios Diários</h1>
            <p class="text-[11px] text-slate-700 font-medium">Operações & Gestão de Turnos</p>
          </div>
        </div>

        <div class="flex items-center gap-3 justify-between md:justify-end">
          <div class="flex items-center gap-2 bg-white/80 border border-amber-300 px-3 py-1.5 rounded-lg text-xs">
            <div id="badgeEscala" class="w-3 h-3 rounded-full bg-red-600"></div>
            <div>
              <span id="labelNomeOperador" class="font-bold text-slate-900 block leading-tight">Renan Missias</span>
              <span id="labelCargoOperador" class="text-[10px] text-slate-600">Administrador</span>
            </div>
          </div>

          <button onclick="sincronizar()" class="flex items-center gap-1 bg-white hover:bg-slate-50 text-slate-700 font-semibold px-2.5 py-1.5 rounded-lg text-xs border border-slate-200 shadow-xs">
            <i data-lucide="refresh-cw" class="w-3.5 h-3.5 text-[#1A4BDB]"></i>
            <span>Sincronizar</span>
          </button>
        </div>
      </div>

      <!-- Abas de Navegação -->
      <nav class="max-w-6xl mx-auto mt-3 flex items-center gap-2 overflow-x-auto text-xs font-bold pt-1">
        <button onclick="mudarAba('painel')" id="tabPainel" class="px-3 py-1.5 rounded-lg bg-slate-900 text-white flex items-center gap-1.5">
          <i data-lucide="layout-dashboard" class="w-3.5 h-3.5"></i> Painel & Metas
        </button>
        <button onclick="mudarAba('relatorios')" id="tabRelatorios" class="px-3 py-1.5 rounded-lg bg-white/70 text-slate-800 hover:bg-white flex items-center gap-1.5">
          <i data-lucide="file-text" class="w-3.5 h-3.5"></i> Relatórios
        </button>
        <button onclick="mudarAba('novo')" id="tabNovo" class="px-3 py-1.5 rounded-lg bg-white/70 text-slate-800 hover:bg-white flex items-center gap-1.5">
          <i data-lucide="plus-circle" class="w-3.5 h-3.5 text-[#1A4BDB]"></i> Novo Relatório
        </button>
        <button onclick="mudarAba('usuarios')" id="tabUsuarios" class="px-3 py-1.5 rounded-lg bg-white/70 text-slate-800 hover:bg-white flex items-center gap-1.5">
          <i data-lucide="users" class="w-3.5 h-3.5"></i> Equipe & Acessos
        </button>
      </nav>
    </header>

    <main class="max-w-6xl mx-auto p-4 flex-1 w-full space-y-4">
      
      <!-- ABA 1: PAINEL -->
      <section id="viewPainel" class="space-y-4">
        <div class="grid grid-cols-2 md:grid-cols-4 gap-
