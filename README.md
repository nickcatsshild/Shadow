<p align="center">
  <a href="https://github.com/nickcatsshild/Shadow">
    <img src="imagens/shadow_banner.png" alt="Shadow Core — Potencializando a inovação de próxima geração" width="820">
  </a>
</p>

<p align="center"><strong>Agente de desktop autônomo para desenvolvimento, produtividade e segurança — 100% portátil, com inferência local e em nuvem.</strong></p>

<p align="center">
  <img alt="Plataforma" src="https://img.shields.io/badge/platform-Windows-blue">
  <img alt="Runtime" src="https://img.shields.io/badge/runtime-Tauri%20v2%20%7C%20Rust-informational">
  <img alt="Stack" src="https://img.shields.io/badge/stack-Rust%20%2B%20Bun%20%2B%20SolidJS%20%2B%20Effect-brightgreen">
  <img alt="Tamanho" src="https://img.shields.io/badge/binary%20size-52.3%20MB%20(-76%25)-success">
  <img alt="Licença" src="https://img.shields.io/badge/license-MIT-lightgrey">
</p>

<p align="center">
  <a href="https://github.com/nickcatsshild/Shadow/releases/latest">
    <img src="https://img.shields.io/badge/Download-Shadow.exe%20(v1.0.0%20Portátil)-2f9fe0?style=for-the-badge&logo=windows&logoColor=white" alt="Download Shadow.exe">
  </a>
  <a href="https://github.com/nickcatsshild/Shadow/releases/latest">
    <img src="https://img.shields.io/badge/Download-Shadow--Portable.zip-10222e?style=for-the-badge&logo=zip&logoColor=white" alt="Download Shadow Portable ZIP">
  </a>
</p>

---

## 💾 Como Baixar e Usar (100% Portátil)

O **Shadow Core** é um aplicativo 100% portátil para Windows — não requer instalação, privilégios administrativos ou alterações no Registro do sistema:

1. Acesse as **[Releases Oficiais no GitHub](https://github.com/nickcatsshild/Shadow/releases/latest)**.
2. Baixe o pacote **`Shadow-Portable-Win-x64.zip`** ou o executável **`Shadow.exe`**.
3. Extraia o conteúdo em qualquer diretório de sua preferência (ex.: `C:\Shadow`, `D:\Shadow` ou em um pendrive portátil).
4. Dê duplo clique em `Shadow.exe` — o aplicativo inicializa em menos de 300ms com todas as capacidades locais ativas!

---

## 🦀 Nova Arquitetura Oficial: Casca Nativa em Rust & Tauri v2

O **Shadow Core** opera sobre uma arquitetura nativa em **Rust com Tauri v2**, substituindo integralmente a antiga casca em Electron. Essa evolução elimina o peso de instâncias completas do Chromium empacotado e garante máxima velocidade, segurança e eficiência no consumo de recursos.

### 📊 Comparativo de Performance

| Métrica / Recurso | Electron (Legado) | Tauri v2 / Rust (Atual Oficial) | Ganho |
|---|---|---|---|
| **Tamanho do Executável** | 220,8 MB | **52,3 MB** | **-76% de redução** |
| **Consumo de Memória (RAM Inativa)** | ~450 MB | **~85 MB** | **-81% de economia** |
| **Tempo de Inicialização (Cold Start)** | ~2,8 segundos | **< 300 ms** | **9x mais veloz** |
| **Inicialização Visual** | Flash de tela cinza/branca | **Exibição determinística (zero flash)** | Experiência fluida |
| **Motor de Renderização** | Chromium empacotado | **Microsoft Edge WebView2 nativo** | Runtime do SO |
| **Painel Lateral Docked** | Janela pesada recriada | **Janela Rust magnetizada (<10ms)** | Instantânea |
| **Navegação Web Externa** | `<webview>` com limitações | **`WebviewWindow` nativa dedicada** | Bypass `X-Frame-Options` |
| **Lógica Administrativa** | Acoplada ao main process | **`@shadow-ai/admin-core` isolado** | 100% desacoplado |

---

## 🚀 O que é o Shadow

O **Shadow** é um agente de desktop **portátil** que combina inteligência local e em nuvem em uma única interface fluida:

- 🖥️ **Inferência local** via `llama-server` (GGUF na GPU) + **nuvem** (Anthropic, OpenAI, Groq, Google, Mistral, Cohere, xAI e mais)
- 🧠 **Aprendizado contínuo** — captura correções, novas técnicas e memorização persistente
- 🛡️ **Guarda de execução** com sandbox 2FA para comandos arriscados
- 🔗 **Coordenação com outros agentes de código** (Claude Code, Cursor, Codex e CLIs compatíveis)
- 🤖 **Automação real de navegador** (Playwright) para captura automática de OAuth, cadastros e scraping
- 📦 **Plugins de produtividade** — E-mails, Calendário, Documentos (PDF/Word/Excel), Mercado Livre
- ⚡ **Zero dependência de Python** — ferramentas nativas compiladas ou executadas via TypeScript/WASM

---

## ✨ Módulos Principais

### 🧠 Inteligência
| Recurso | Detalhes |
|---|---|
| **Motor Llama-server (5 Slots)** | Ciclo de vida de processo nativo, descarrega a VRAM da GPU automaticamente quando inativo, 5 slots dedicados simultâneos (portas 11434 a 11438) |
| **Roteamento de IA** | 3 modos (100% local / híbrido / 100% nuvem) com cascata de fallback para até 5 modelos |
| **RAG SQLite FTS5** | Fragmentação semântica (chunking) + busca híbrida (BM25 + cosseno vetorial com RRF) |
| **Aprendizado contínuo** | Loop pós-interação detecta sinais, corrige skills e salva o aprendizado em `memory/` |
| **Skills geradas** | O sistema cria e edita suas próprias skills; o painel exibe o inventário em tempo real |

### 🛡️ Segurança
| Recurso | Detalhes |
|---|---|
| **Sandbox 2FA** | Comandos arriscados (`git push --force`, `rm -rf`) aguardam aprovação remota via Telegram/celular |
| **Interceptador Pré-voo** | Bloqueia comandos destrutivos do SO na raiz (`format`, `diskpart`, `rmdir /s /q C:\`) |
| **Criptografia Nativa** | Credenciais (tokens OAuth, senhas) protegidas via DPAPI do Windows |
| **Auditoria** | Tabela de execução com pontuações de risco em cores e trilha de auditoria completa |

### 🔗 Integrações
| Recurso | Detalhes |
|---|---|
| **Canais de mensagens** | Telegram · WhatsApp · Discord · Slack · Teams · Signal · Instagram · Messenger · X · LinkedIn |
| **Contas de e-mail** | Gmail · Outlook · Yahoo · iCloud · IMAP · webhook personalizado (múltiplas contas) |
| **Calendário unificado** | Google Agenda · Outlook · Teams · iCal (múltiplas contas) |
| **Mercado Livre** | Plugin de Vendas: pesquisa de preços, upload de fotos, textos gerados por IA, publicação via API |
| **Automação de navegador** | Chromium/Firefox/WebKit via Playwright — Captura automática de OAuth, cadastros, scraping |
| **Extensão Obsidian** | Sincronização contínua com Vault Obsidian (`Diários`, `Aprendizados`, `Notas`, grafo neural) |

### ⚙️ Operações
| Recurso | Detalhes |
|---|---|
| **Verificação de saúde** | Diagnóstico em um clique do workspace, skills, DB e memória |
| **Heartbeat** | Registra sinais de rotina periódicos em `HEARTBEAT.md` |
| **Cron autônomo** | Engine em TypeScript com persistência JSON (`data/cronjobs.json`) sem qualquer dependência de Python |
| **Mobile Companion PWA** | Servidor HTTP na porta `18765` para controle por smartphone através da rede local (LAN) |

---

## 🌟 Recursos em Destaque no Shadow.exe

### 1. 🔮 Modo Assistente Shadow & Orbe Holográfico
- **Interface Flutuante (HUD):** Janela compacta (`440x700`) flutuante e arrastável livremente pela tela, ativada pelo botão luminoso no topo ou pelo atalho **`Ctrl + Shift + A`**.
- **Orbe Holográfico Reativo (`ShadowHologramOrb`):** Anéis concêntricos contra-rotativos em gradiente Ciano Elétrico (`#00f0ff` / `#2f9fe0`) e Magenta/Roxo Neon (`#ff007f` / `#b829ea`).
- **Reatividade Acústica:** Pulsação física proporcional aos decibéis da voz via `Web Audio API` e `AnalyserNode` nos 4 estados animados (`idle`, `listening`, `thinking`, `speaking`).
- **Interação Natural:** Reconhecimento contínuo de voz com transcrição em tempo real e respostas faladas em português nativo.

### 2. 🏛️ Cockpit Executivo Unificado (Shadow Navy Glassmorphism)
- **Model Matrix & Playground:** Esteira visual de failover em 4 slots com simulação de tolerância a falhas, ping em tempo real e comparador de modelos lado a lado com medição de tokens/segundo e latência em milissegundos.
- **Central de Plugins & MCPs:** Marketplace com **294 plugins portáteis** e **65 servidores MCP**, com o *Plugin Inspector Drawer* para auditoria de permissões e manifestos `plugin.json`.
- **Agent Command Hub (145 Subagentes):** Grafo DAG do Ultraplan para execução paralela, telemetria de especialistas e orquestração multi-agente.

### 3. 🦙 Local Multimodal Hub & Áudio Neural 100% Offline
- **Hub Multimodal com 5 Slots Simultâneos:** Execução independente de modelos locais GGUF em 5 slots dedicados (portas automáticas `11434` a `11438`) com endpoints compatíveis com OpenAI.
- **Voice & Audio Studio:** Síntese vocal neural de alta fidelidade em português brasileiro via **Piper Neural TTS (ONNX)** e Windows SAPI em memória, com zero dependência de conexão à internet ou Python.

---

## 🔄 Como Funciona a Atualização Automática

O Shadow Core foi projetado para ser atualizado sem complicações:
1. Ao inicializar ou através do menu **Configurações ➔ Sobre / Atualizações**, o aplicativo consulta a API pública de releases deste repositório (`https://api.github.com/repos/nickcatsshild/Shadow/releases/latest`).
2. Se uma nova versão for detectada, o aplicativo exibe o resumo das novidades e o botão para baixar e atualizar os binários automaticamente.
3. Não há necessidade de reinstalação: as pastas de dados do usuário (`data/`, `workspace/`, `memory/`) são preservadas de forma intacta.

---

## 📜 Licença

Distribuído sob a Licença MIT. Veja [`LICENSE`](LICENSE) para mais detalhes.
