# Clone do Site - Subway Premiado (surfedolucro.vercel.app)

Este repositório contém o clone completo e funcional do site [Subway Premiado](https://surfedolucro.vercel.app/).

---

## 📁 Estrutura de Arquivos

- [index.html](file:///Users/mac/Desktop/RPT/index.html) - Página principal do funil (completa com todo o HTML, CSS, JavaScript, animações, logos e imagens base64 embutidas).
- [assets_surfe/](file:///Users/mac/Desktop/RPT/assets_surfe) - Imagens extraídas em arquivos individuais para fácil edição:
  - `favicon.png` - Ícone da página
  - `subway-bg.jpg` - Fundo temático do Subway Surfers
  - `multicaixa-express.png` - Logotipo do Multicaixa Express
  - `multicaixa-iban.png` - Logotipo da transferência IBAN / Multicaixa
  - `bna-logo.jpg` - Logotipo do Banco Nacional de Angola (BNA)
- [server.py](file:///Users/mac/Desktop/RPT/server.py) - Servidor local Python para testar no navegador.
- [vercel.json](file:///Users/mac/Desktop/RPT/vercel.json) - Configuração para deploy direto na Vercel.
- [_redirects](file:///Users/mac/Desktop/RPT/_redirects) - Configuração para deploy no Netlify / Cloudflare Pages.
- [.htaccess](file:///Users/mac/Desktop/RPT/.htaccess) - Configuração para servidores Apache / cPanel / Hostinger.
- `_backup_antigo/` - Backup dos arquivos anteriores do diretório.

---

## 🕹️ Etapas do Funil

1. **Step 1 (`#step-offer`)**: Oferta Ativa ("Ganhe Dinheiro no Subway Surfers").
2. **Step 2 (`#step-register`)**: Formulário de vinculação de conta (Nome e Telefone de Angola `9XX XXX XXX`).
3. **Step 3 (`#step-linked`)**: Confirmação da conta vinculada e ativação do saldo.
4. **Step 4 (`#step-game`)**: Iframe com o jogo integrado via Worker Cloudflare (`game-proxy.admirablecabinet.workers.dev/game.html`).
5. **Step 5 (`#step-bonus`)**: Tela de parabéns com o saldo acumulado (ex: `115.000 Kz`).
6. **Step 6 (`#step-withdraw`)**: Escolha do método de levantamento (Multicaixa Express ou Transferência IBAN com seleção de banco: BAI, BFA, BIC, etc.).
7. **Step 7 (`#step-error`)**: Simulação de erro / retenção de transferência bancária por segurança.
8. **Step 8 (`#step-security`)**: Protocolo de segurança BNA para desbloqueio.
9. **Step 9 (`#step-almost`)**: VSL (Vídeo de Vendas) com player Vturb e liberação com delay do botão de checkout final (`mentora.ao`).

---

## 🚀 Como Executar Localmente

Execute o script Python:
```bash
python3 server.py
```
Em seguida, abra no navegador:
```
http://localhost:8000
```

---

## ⚙️ Configurações Importantes no `index.html`

- **Link de Checkout**: Linha ~1479 no script final (`var checkoutUrl = 'https://mentora.ao/produto/...';`).
- **Pixels**:
  - Meta / Facebook Pixel: Linhas 30-45 (`fbq('init', '1618326293178975');`).
  - Utmify Pixel: Linhas 48-65.
- **Tempo do Botão da VSL**: Linha ~1197 (`var VSL_CTA_TARGET_SECONDS = 8 * 60 + 34;`).
