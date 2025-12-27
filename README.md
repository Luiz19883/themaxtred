# Trade Alert PRO 🤖 v19.10

**Plataforma de Sinais de Trading com Análise de Inteligência Artificial**

Uma plataforma profissional de análise de sinais de criptomoedas com IA integrada, análise técnica avançada e copy trading para Binance e Bybit.

![Version](https://img.shields.io/badge/version-19.10-blue.svg)
![AI Powered](https://img.shields.io/badge/AI-Powered-green.svg)
![License](https://img.shields.io/badge/license-MIT-yellow.svg)

---

## 🌟 Características Principais

### 🤖 Análise de IA
- **Análise Local (Gratuita)**: Algoritmos heurísticos avançados
- **Análise via API (Opcional)**: Integração com Google Gemini
- **Score de Confiança**: 0-100% para cada sinal
- **Recomendações Automáticas**: STRONG_BUY, BUY, HOLD, SELL, STRONG_SELL
- **Fatores Identificados**: Por que a IA recomenda cada sinal
- **Avaliação de Riscos**: Alertas automáticos

### 📊 Análise Técnica
- **30 Pares de Criptomoedas** monitorados simultaneamente
- **Indicadores Técnicos**:
  - RSI (Relative Strength Index)
  - MACD (Moving Average Convergence Divergence)
  - Volume Analysis
  - Price Momentum
- **Sinais em Tempo Real** com atualizações configuráveis (15/30/40 min)

### 💰 Copy Trading
- **Integração Binance & Bybit**
- **Sugestão Automática de Alavancagem** (3x-10x)
- **Copy trade com 1 clique**
- **Preview completo** antes de executar
- **Histórico** de últimos trades

### 🎨 Interface Moderna
- **Design VIP Premium** com glassmorphism
- **Dark Mode** otimizado
- **Responsivo** para todos os dispositivos
- **Badges de Confiança** da IA coloridos
- **Animações suaves**

### 🔗 Web3 & Blockchain
- **Suporte Multi-Chain**:
  - Ethereum (ETH)
  - Binance Smart Chain (BSC)  
  - Solana (SOL)
- **Conexão de Carteira**
- **Dados on-chain**

---

## 🚀 Instalação

### Pré-requisitos
- Node.js 16+ 
- NPM ou Yarn

### Passos

1. **Clone o repositório**
```bash
git clone https://github.com/seu-usuario/trade-alert-pro.git
cd trade-alert-pro
```

2. **Instale as dependências**
```bash
npm install
```

3. **Configure a IA (Opcional)**

Para usar análise de IA avançada via Google Gemini:

a) Obtenha uma API key gratuita em: https://makersuite.google.com/app/apikey

b) Edite `config.json`:
```json
{
  "ai": {
    "provider": "api",
    "apiKey": "SUA_CHAVE_AQUI"
  }
}
```

4. **Inicie o servidor**
```bash
npm run dev
```

5. **Acesse a plataforma**
```
http://localhost:3000/vip.html
```

---

## 📁 Estrutura do Projeto

```
trade-alert-pro/
├── assets/
│   ├── modern-vip.css          # Estilos principais
│   └── ai-ux.css               # Estilos da IA
├── js/
│   ├── main.js                 # Lógica principal
│   ├── ai-analysis.js          # Módulo de IA ⭐
│   ├── config-loader.js        # Carregador de configuração
│   ├── binance-api.js          # API Binance
│   ├── technical-indicators.js # Indicadores técnicos
│   ├── web3-wallet.js          # Integração Web3
│   └── ...
├── config.json                 # Configurações ⚙️
├── vip.html                    # Interface principal
├── index.html                  # Página de entrada
└── package.json
```

---

## ⚙️ Configuração

### config.json

```json
{
  "app": {
    "name": "Trade Alert PRO",
    "version": "19.10"
  },
  "trading": {
    "pairs": ["BTCUSDT", "ETHUSDT", ...],
    "defaultTimeframe": "15m",
    "strategyName": "IA Grok Copy Trade"
  },
  "ai": {
    "enabled": true,
    "provider": "local",  // ou "api"
    "apiKey": "",
    "thresholds": {
      "minConfidence": 50,
      "highConfidence": 75
    }
  }
}
```

### Intervalos de Atualização

Configure no painel:
- **Manual**: Sob demanda
- **15 min**: Rápido (padrão)
- **30 min**: Balanceado
- **40 min**: Econômico

---

## 🎯 Como Usar

### 1. Dashboard
- Veja estatísticas da sessão
- Monitore sinais recentes
- Acompanhe Auto Trade

### 2. Sinais em Tempo Real
- **Filtre** por tipo: Todos / Long / Short
- **Busque** pares específicos
- **Analise** badges de confiança da IA:
  - 🟢 Verde (75-100%): Alta confiança
  - 🟡 Amarelo (60-74%): Média confiança
  - ⚪ Cinza (<60%): Baixa confiança

### 3. Copy Trading
1. Click em "Copiar Binance" ou "Copiar Bybit"
2. Revise os detalhes no modal
3. Cole na plataforma de trading

### 4. Watchlist
- Adicione seus pares favoritos
- Monitore personalizadamente

### 5. Blockchain
- Conecte carteira Web3
- Alterne entre redes

### 6. Insights
- Carregue análise de mercado
- Sentimento da IA
- Notícias em tempo real

---

## 🤖 Análise de IA

### Modo Local (Gratuito)

A IA analisa automaticamente:
- ✅ **RSI**: Zonas de sobrecompra/sobrevenda
- ✅ **Volume**: Comparação com média
- ✅ **Momentum**: Variação de preço 24h
- ✅ **MACD**: Quando disponível

**Exemplo de Output:**
```
Confidence: 82%
Factor: RSI indicates oversold conditions - good entry point
Recommendation: STRONG_BUY
```

### Modo API (Gemini)

Com uma API key do Google Gemini, você obtém:
- 📈 Análise contextual por linguagem natural
- 🎯 Insights personalizados
- 💡 Recomendações baseadas em ML

---

## 🛠️ Desenvolvimento

### Scripts Disponíveis

```bash
# Desenvolvimento
npm run dev

# Build para produção
npm run build

# Testes
npm test

# Lint
npm run lint
```

###  Adicionar Novos Pares

Edite `config.json`:
```json
{
  "trading": {
    "pairs": [
      "BTCUSDT",
      "NOVO_PAR_USDT"  // ← Adicione aqui
    ]
  }
}
```

---

## 🎨 Personalização

### Temas

Edite `assets/modern-vip.css`:
```css
:root {
  --primary: #d4af37;     /* Cor principal */
  --accent: #ff6b6b;      /* Cor de destaque */
  --success: #10b981;     /* Verde */
  --secondary: #ef4444;   /* Vermelho */
}
```

### Logos & Branding

Substitua em `vip.html`:
```html
<div class="brand">SEU NOME AQUI</div>
```

---

## 📊 API Reference

### Binance API
- Endpoint: `https://api.binance.com/api/v3`
- Rate Limit: 1200 requests/minute
- Docs: https://binance-docs.github.io/apidocs/

### Google Gemini AI
- Endpoint: `https://generativelanguage.googleapis.com/v1beta/`
- Model: `gemini-pro`
- Docs: https://ai.google.dev/docs

---

## 🔒 Segurança

⚠️ **IMPORTANTE**:
- Nunca compartilhe sua API key
- Use variáveis de ambiente em produção
- Não commite credenciais no Git
- Revise permissões de API keys

---

## 🐛 Troubleshooting

### CSS não carrega
```bash
# Verifique se os arquivos existem
ls assets/modern-vip.css
ls assets/ai-ux.css
```

### IA não funciona
1. Verifique `config.json` → `ai.enabled: true`
2. Para modo API, verifique se a API key está correta
3. Abra o console do navegador (F12) para ver erros

### Sinais não atualizam
1. Verifique conexão com internet
2. Teste API Binance: https://api.binance.com/api/v3/ping
3. Limpe cache do navegador

---

## 📝 Changelog

### v19.10 (Atual)
- ✨ **NEW**: Integração completa de IA
- ✨ **NEW**: UI/UX melhorada para badges de IA
- ✨ **NEW**: Suporte a Google Gemini API
- ✨ **NEW**: Sistema de confiança 0-100%
- 🎨 Redesign do CSS com `ai-ux.css`
- 🐛 Correção de bugs no `vip.html`
- 📝 README atualizado

### v19.0
- Lançamento inicial
- 30 pares monitorados
- Copy trading Binance/Bybit
- Análise técnica básica

---

## 🤝 Contribuindo

Contribuições são bem-vindas!

1. Fork o projeto
2. Crie uma branch (`git checkout -b feature/MinhaFeature`)
3. Commit suas mudanças (`git commit -m 'Add: MinhaFeature'`)
4. Push para a branch (`git push origin feature/MinhaFeature`)
5. Abra um Pull Request

---

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

---

## 👨‍💻 Autor

**Trade Alert PRO Team**

- 🌐 Website: [em breve]
- 📧 Email: [seu-email]
- 💼 LinkedIn: [seu-linkedin]

---

## 🙏 Agradecimentos

- **Google Gemini** - Por fornecer IA gratuita
- **Binance** - Pela API robusta
- **Comunidade Crypto** - Por feedback e suporte

---

## ⭐ Star o Projeto!

Se este projeto te ajudou, considere dar uma ⭐!

---

<div align="center">
  <strong>Feito com ❤️ e ☕</strong>
  <br>
  <sub>Trade Alert PRO v19.10 - IA Powered Trading Signals</sub>
</div>
