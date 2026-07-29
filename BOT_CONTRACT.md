# 🤖 MyZubster Bot Contract

**Automated Agent Agreement for AI Bots in the MyZubster Ecosystem**

**Version:** 1.0  
**Effective Date:** 2026-07-29  
**Blockchain:** Monero (XMR)  
**Creator:** DanielIoni-creator

---

## 1. Definizione di Bot

Un **Bot** è un agente software automatizzato che:

- Esegue azioni predefinite senza intervento umano
- Interagisce con le API di MyZubster
- Può leggere, scrivere e verificare dati
- Opera secondo regole e limiti prestabiliti

---

## 2. Tipi di Bot

### 🤖 Bot di Identificazione Piante

| Funzione | Descrizione | Limiti |
|----------|-------------|--------|
| Riconoscimento specie | Identifica piante da foto | ≤ 1000 richieste/ora |
| Verifica GPS | Controlla coordinate | ≤ 5000 richieste/ora |
| Analisi salute | Valuta condizioni | ≤ 100 richieste/minuto |

### 🤖 Bot di Identificazione Animali

| Funzione | Descrizione | Limiti |
|----------|-------------|--------|
| Lettura NFC | Legge tag NFC | ≤ 100 richieste/ora |
| Riconoscimento razza | Identifica da foto | ≤ 500 richieste/ora |
| Tracciamento GPS | Monitora posizioni | ≤ 1000 richieste/ora |

### 🤖 Bot di Pagamento

| Funzione | Descrizione | Limiti |
|----------|-------------|--------|
| Processamento XMR | Gestisce transazioni | ≤ 100 transazioni/ora |
| Verifica pagamenti | Controlla stato | ≤ 1000 richieste/ora |
| Distribuzione fee | Divide le fee | ≤ 50 transazioni/ora |

### 🤖 Bot di Verifica

| Funzione | Descrizione | Limiti |
|----------|-------------|--------|
| Verifica dati | Controlla registrazioni | ≤ 500 richieste/ora |
| Quality scoring | Valuta qualità | ≤ 200 richieste/ora |
| Anti-frode | Rileva anomalie | ≤ 1000 richieste/ora |

---

## 3. Regole Operative

### 3.1 Autenticazione

Ogni bot deve avere un **API Key univoco**:

```yaml
Bot ID: bot_XXXXXXXXXX
API Key: xmr_bot_XXXXXXXXXXXXXXXX
Permessi: [read, write, verify]
Limiti: [rate: 1000/h]
