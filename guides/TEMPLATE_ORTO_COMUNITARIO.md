# [TEMPLATE] Modello per Orto Comunitario con MyZubster / Community Garden Setup & Management Template

**Versione / Version:** 1.0.0  
**Data / Date:** 2026-07-31  
**Progetto / Project:** MyZubster Ecosystem  
**Issue di Riferimento / Reference Issue:** #15  
**Pubblico / Audience:** Gruppi di orticoltura comunitaria / Community gardening groups

---

## Indice / Table of Contents

1. [Introduzione / Introduction](#1-introduzione--introduction)
2. [Configurazione Consigliata / Recommended Setup](#2-configurazione-consigliata--recommended-setup)
3. [Componenti a Basso Costo / Low-Cost Components](#3-componenti-a-basso-costo--low-cost-components)
4. [Guida all'Installazione / Installation Guide](#4-guida-allinstallazione--installation-guide)
5. [Gestione Multiutente / Multi-User Management](#5-gestione-multiutente--multi-user-management)
6. [Monitoraggio Collettivo / Collective Monitoring](#6-monitoraggio-collettivo--collective-monitoring)
7. [Dashboard Comunitaria / Community Dashboard](#7-dashboard-comunitaria--community-dashboard)
8. [Esempio di Orto Comunitario / Example Community Garden](#8-esempio-di-orto-comunitario--example-community-garden)
9. [Piano di Manutenzione / Maintenance Plan](#9-piano-di-manutenzione--maintenance-plan)
10. [Appendice: Checklist di Avvio / Appendix: Startup Checklist](#10-appendice-checklist-di-avvio--appendix-startup-checklist)

---

## 1. Introduzione / Introduction

**Italiano:**  
Questo modello aiuta i gruppi a gestire un orto condiviso con MyZubster. In un orto comunitario ogni membro coltiva una parcella, ma i dati di monitoraggio (pH, EC, temperatura, umidità) sono raccolti e condivisi per il bene dell'intera comunità. Il modello definisce configurazione, ruoli, procedure di monitoraggio collettivo e piano di manutenzione condiviso.

**English:**  
This template helps groups manage a shared garden with MyZubster. In a community garden each member cultivates a parcel, but the monitoring data (pH, EC, temperature, moisture) is collected and shared for the whole community. The template defines setup, roles, collective monitoring procedures, and a shared maintenance plan.

### 1.1 Ruoli dei Membri / Member Roles

| Ruolo / Role | Responsabilità / Responsibilities |
|--------------|-----------------------------------|
| **Amministratore / Admin** | Gestisce utenti, parcelle, configurazione del gateway |
| **Coordinatore Tecnico / Tech Coordinator** | Manutenzione hardware, calibrazione sensori |
| **Giardiniere / Gardener** | Coltiva una parcella, annota osservazioni |
| **Osservatore / Observer** | Consulta dati e dashboard (sola lettura / read-only) |

---

## 2. Configurazione Consigliata / Recommended Setup

**Italiano:**  
Per un orto comunitario si consiglia una configurazione **centralizzata**: un gateway centrale con sensori distribuiti nelle parcelle. Riduce costi e semplifica la manutenzione.

**English:**  
For a community garden a **centralized** setup is recommended: one central gateway with sensors distributed across parcels. It reduces costs and simplifies maintenance.

### 2.1 Hardware Consigliato / Recommended Hardware

| Componente / Component | Configurazione / Config | Note |
|------------------------|-------------------------|------|
| **Gateway Centrale / Central Gateway** | Raspberry Pi 4 (2GB) o mini-PC | Esegue MyZubsterGateway + dashboard |
| **Hub Sensori / Sensor Hubs** | ESP32 per zona (2-4 parcelle per hub) | Raccolta dati locale via WiFi |
| **Sensori per Parcella / Per-Parcel Sensors** | pH, EC, temperatura, umidità | 1 set per parcella o ogni 2 |
| **Alimentazione / Power** | Pannello solare 20W + batteria 12V 20Ah | Per installazioni off-grid |
| **Rete / Network** | Router WiFi + connessione internet | Per accesso remoto alla dashboard |

### 2.2 Software Consigliato / Recommended Software

| Componente / Component | Software | Scopo / Purpose |
|------------------------|----------|-----------------|
| **Gateway** | MyZubsterGateway (Node.js/Docker) | API, archiviazione, autenticazione |
| **Dashboard** | MyZubster Dashboard (Web) | Dati, gestione utenti e parcelle |
| **Firmware ESP32** | MyZubster ESP32 Firmware | Lettura sensori e invio dati |
| **App Mobile** | MyZubster Mobile App | Accesso rapido per i membri |

---

## 3. Componenti a Basso Costo / Low-Cost Components

### 3.1 Kit Economico per 6-10 Parcelle / Budget Kit for 6-10 Parcels

**Italiano:**  
Lista indicativa per un orto comunitario di 6-10 parcelle con hub centrale. Gli acquisti in gruppo possono ridurre i prezzi del 20-30%.

**English:**  
Indicative list for a 6-10 parcel community garden with central hub. Group buying can reduce prices by 20-30%.

| # | Componente / Component | Q.tà / Qty | Costo Unit. / Unit Cost | Subtotale / Subtotal |
|---|------------------------|------------|-------------------------|----------------------|
| 1 | **Raspberry Pi 4 (2GB)** | 1 | €55-75 | €55-75 |
| 2 | **ESP32 DevKit V1** | 3 | €8-12 | €24-36 |
| 3 | **Sensore pH (sonda BNC)** | 4 | €12-18 | €48-72 |
| 4 | **Sensore EC (K1.0)** | 4 | €10-15 | €40-60 |
| 5 | **Sensore Temperatura DS18B20** | 6 | €2-4 | €12-24 |
| 6 | **Sensore Umidità capacitivo FC-28** | 6 | €2-5 | €12-30 |
| 7 | **Pannello solare 20W + regolatore** | 1 | €40-60 | €40-60 |
| 8 | **Batteria 12V 20Ah LiFePO₄** | 1 | €45-70 | €45-70 |
| 9 | **Router WiFi (usato / refurbished)** | 1 | €15-30 | €15-30 |
| 10 | **Cavi, connettori, guaine IP65** | Lotto | €25-40 | €25-40 |
| 11 | **Scatole stagne IP65 per hub** | 3 | €8-12 | €24-36 |
| 12 | **Soluzioni di calibrazione** | Lotto | €15-25 | €15-25 |
| | **TOTALE / TOTAL** | | | **≈ €355-558** |

**Italiano:**  
**Risparmio:** acquisto in gruppo (-20-30%), ricondizionati (Raspberry Pi, router), condivisione sensori pH/EC ogni 2 parcelle, sponsor locali.

**English:**  
**Savings:** group buying (-20-30%), refurbished items (Raspberry Pi, routers), sharing pH/EC sensors per 2 parcels, local sponsors.

### 3.2 Costi Ricorrenti / Recurring Costs

**Italiano:** Elettricità €3-8/mese · Internet €10-20/mese · Manutenzione sensori €5-15/mese → **totale ≈ €18-43/mese**, da dividere tra i membri.

**English:** Electricity €3-8/month · Internet €10-20/month · Sensor upkeep €5-15/month → **total ≈ €18-43/month**, shared among members.

---

## 4. Guida all'Installazione / Installation Guide

### 4.1 Installazione Hardware / Hardware Installation

**Italiano:**
1. **Gateway:** installare Raspberry Pi OS Lite, collegare il router, montare pannello solare + batteria (se off-grid)
2. **Hub ESP32:** caricare il firmware, collegare i sensori ai pin ADC (GPIO 34, 35, 36), sigillare in scatola IP65
3. **Sensori:** umidità a 10-15 cm di profondità; pH/EC a 20 cm di distanza; temperatura a contatto con il suolo, in ombra
4. **WiFi:** testare il segnale in ogni parcella, aggiungere un extender se necessario

**English:**
1. **Gateway:** install Raspberry Pi OS Lite, connect the router, mount solar panel + battery (if off-grid)
2. **ESP32 hubs:** flash the firmware, connect sensors to ADC pins (GPIO 34, 35, 36), seal in IP65 box
3. **Sensors:** moisture at 10-15 cm depth; pH/EC 20 cm apart; temperature in soil contact, in shade
4. **WiFi:** test the signal in every parcel, add an extender if needed

### 4.2 Installazione del Gateway / Gateway Software Installation

**Italiano:**
```bash
git clone https://github.com/MyZubster-Ecosystem/MyZubsterGateway.git && cd MyZubsterGateway
cp .env.example .env && nano .env   # Credenziali database / DB credentials
docker-compose up -d && curl http://localhost:3000/api/health
```

**English:** *(stessi comandi / same commands)*

### 4.3 Configurazione Firmware ESP32 / ESP32 Firmware Setup

**Italiano:**
1. Aprire Arduino IDE o PlatformIO e caricare `MyZubsterCommunityHub.ino` (nel repository firmware)
2. Configurare: `WIFI_SSID`, `WIFI_PASSWORD`, `GATEWAY_URL` (es. `http://192.168.1.50:3000`), `HUB_ID` (es. `hub-a`)
3. Verificare che ogni hub compaia nella dashboard entro 5 minuti

**English:**
1. Open Arduino IDE or PlatformIO and flash `MyZubsterCommunityHub.ino` (in the firmware repository)
2. Configure: `WIFI_SSID`, `WIFI_PASSWORD`, `GATEWAY_URL` (e.g. `http://192.168.1.50:3000`), `HUB_ID` (e.g. `hub-a`)
3. Verify each hub appears in the dashboard within 5 minutes

### 4.4 Creazione del Gruppo / Group Creation

**Italiano:**
1. Accedere alla dashboard come amministratore e creare il gruppo da *Community > Groups*
2. Aggiungere i membri con i ruoli (sez. 1.1) e definire/assegnare le parcelle (A, B, C...)
3. Registrare gli hub ESP32 come dispositivi del gruppo

**English:**
1. Sign in to the dashboard as administrator and create the group from *Community > Groups*
2. Add members with roles (sec. 1.1) and define/assign parcels (A, B, C...)
3. Register the ESP32 hubs as group devices

---

## 5. Gestione Multiutente / Multi-User Management

### 5.1 Ruoli e Permessi / Roles & Permissions

| Ruolo / Role | Parcelle / Parcels | Dati / Data | Config / Config | Utenti / Users |
|--------------|--------------------|-------------|-----------------|----------------|
| **Amministratore / Admin** | Tutte / All | L/S (R/W) | Sì / Yes | Sì / Yes |
| **Coordinatore Tecnico / Tech Coordinator** | Tutte / All | L/S (R/W) | Sì (hardware) | No |
| **Giardiniere / Gardener** | Solo proprie / Own only | L/S (R/W) | No | No |
| **Osservatore / Observer** | Tutte (sola lettura) / All (read-only) | Lettura / Read | No | No |

### 5.2 Registrazione dei Membri / Member Onboarding

**Italiano:** Account personale → invito dell'amministratore via email → assegnazione parcella → formazione di 30 minuti → accesso da app mobile.

**English:** Personal account → admin email invitation → parcel assignment → 30-minute training → mobile app access.

### 5.3 Diario di Parcella / Parcel Journal

**Italiano:** Ogni giardiniere annota **eventi** (semina, trapianto, raccolta), **osservazioni** (parassiti, foglie gialle) e **azioni** (irrigazione, potatura).

**English:** Each gardener logs **events** (sowing, transplanting, harvest), **observations** (pests, yellow leaves) and **actions** (watering, pruning).

| Tipo / Type | Esempio / Example |
|-------------|-------------------|
| Evento / Event | `2026-08-01: Trapianto pomodori in parcella A / Tomato transplant in parcel A` |
| Osservazione / Observation | `2026-08-03: Macchie bianche su zucchina / White spots on zucchini` |
| Azione / Action | `2026-08-04: Irrigazione manuale 10L/m² / Manual watering 10L/m²` |

### 5.4 Comunicazione e Notifiche / Communication & Notifications

**Italiano:** Alert automatici sulle soglie · Canale Telegram condiviso · Riepilogo settimanale (lunedì) · Menzioni nei commenti (`@marco`).

**English:** Automatic threshold alerts · Shared Telegram channel · Weekly summary (Monday) · Mentions in comments (`@marco`).

---

## 6. Monitoraggio Collettivo / Collective Monitoring

### 6.1 Mappa dell'Orto / Garden Map

**Italiano:** La dashboard mostra la mappa con le parcelle colorate: **verde** (ottimale), **giallo** (attenzione, un parametro fuori range), **rosso** (critico). Cliccando su una parcella si aprono serie storiche, ultime letture e diario.

**English:** The dashboard shows the map with colored parcels: **green** (optimal), **yellow** (caution, one parameter out of range), **red** (critical). Clicking a parcel opens time series, latest readings, and journal.

### 6.2 Soglie di Allarme Collettive / Collective Alert Thresholds

| Parametro / Parameter | Soglia Bassa / Low | Soglia Alta / High | Unità / Unit |
|----------------------|--------------------|--------------------|--------------|
| **pH** | 5.5 | 7.5 | pH |
| **EC** | 0.5 | 3.0 | mS/cm |
| **Temperatura / Temperature** | 10 | 32 | °C |
| **Umidità / Moisture** | 35 | 80 | % |

**Italiano:** Soglie configurabili per gruppo (consenso della comunità) o per parcella (adattamento alle colture).

**English:** Thresholds configurable per group (community consensus) or per parcel (crop adaptation).

### 6.3 Calendario di Coltivazione Condiviso / Shared Cultivation Calendar

| Mese / Month | Attività / Activity | Parcelle / Parcels |
|--------------|---------------------|--------------------|
| Marzo / March | Semina in semenzaio / Seed sowing | Tutte / All |
| Aprile / April | Trapianto estivo / Summer transplant | A, B |
| Maggio / May | Pacciamatura, irrigazione / Mulching, irrigation | Tutte / All |
| Giugno / June | Monitoraggio parassiti / Pest monitoring | Tutte / All |
| Luglio / July | Raccolta estiva / Summer harvest | A, B, C |
| Settembre / September | Semina autunnale / Fall sowing | D, E |
| Ottobre / October | Pulizia, compostaggio / Cleanup, composting | Tutte / All |
| Novembre / November | Riposo, pianificazione / Rest, planning | Tutte / All |

### 6.4 Report di Comunità / Community Reports

**Italiano:** Il report mensile include: andamento generale (medie orto), parcelle a rischio, interventi registrati, raccomandazioni automatiche (es. "aumentare irrigazione in parcella B").

**English:** The monthly report includes: overall trend (garden averages), at-risk parcels, logged actions, automatic recommendations (e.g. "increase irrigation in parcel B").

---

## 7. Dashboard Comunitaria / Community Dashboard

### 7.1 Widget Disponibili / Available Widgets

| Widget | Descrizione / Description | Personalizzazione / Customization |
|--------|---------------------------|-----------------------------------|
| **Mappa Orto / Garden Map** | Mappa a colori delle parcelle | Ordine, dimensioni, colori |
| **Serie Storiche / Time Series** | Grafici per parametro nel tempo | Range date, parametri, parcelle |
| **Classifica Parcelle / Parcel Ranking** | Parcelle per salute / health score | Metrica, soglie |
| **Calendario / Calendar** | Attività e scadenze condivise | Vista mensile/settimanale |
| **Notizie Gruppo / Group Feed** | Diario e osservazioni recenti | Filtri per membro/parcella |
| **Statistiche Comunità / Community Stats** | KPI del gruppo | Periodo, indicatori |

### 7.2 Personalizzazione / Customization

**Italiano:**
1. **Branding:** nome, logo, colori del gruppo
2. **Lingua:** italiano o inglese
3. **Widget:** trascinare e ridimensionare nel layout
4. **Visibilità:** dati pubblici (es. mappa) vs riservati ai membri
5. **Export:** dati in CSV per report esterni

**English:**
1. **Branding:** group name, logo, colors
2. **Language:** Italian or English
3. **Widgets:** drag and resize in the layout
4. **Visibility:** public data (e.g. map) vs member-only
5. **Export:** data to CSV for external reports

---

## 8. Esempio di Orto Comunitario / Example Community Garden

### 8.1 Caso di Studio / Case Study

**Italiano:**  
**Contesto:** associazione di quartiere, 12 membri, 6 parcelle (A-F), 200 m² urbani.  
**Setup:** 1 Raspberry Pi 4 (gateway), 3 hub ESP32 (hub-a: A/B, hub-b: C/D, hub-c: E/F), 3 set pH/EC, 6 sensori temperatura + 6 umidità.  
**Budget iniziale:** ≈ €410 · **Costi mensili:** €30 condivisi (€2.50/membro).

**English:**  
**Context:** neighborhood association, 12 members, 6 parcels (A-F), 200 m² urban area.  
**Setup:** 1 Raspberry Pi 4 (gateway), 3 ESP32 hubs (hub-a: A/B, hub-b: C/D, hub-c: E/F), 3 pH/EC sets, 6 temperature + 6 moisture sensors.  
**Initial budget:** ≈ €410 · **Monthly costs:** €30 shared (€2.50/member).

### 8.2 Risultati nel Primo Anno / First-Year Results

| Indicatore / Metric | Risultato / Result |
|---------------------|--------------------|
| Membri attivi / Active members | 12/12 |
| Riduzione irrigazione / Water reduction | 25% |
| Riduzione fertilizzanti / Fertilizer reduction | 18% |
| Parcelle con resa stabile / Parcels with stable yield | 5/6 |
| Alert risolti entro 48h / Alerts resolved within 48h | 90% |
| Eventi comunitari / Community events | 6 |

**Italiano:**  
**Lezioni apprese:** la rotazione dei compiti aumenta la partecipazione; le soglie vanno riviste ogni stagione; la dashboard pubblica attira nuovi membri; il diario è lo strumento più usato.

**English:**  
**Lessons learned:** rotating tasks increases participation; review thresholds each season; the public dashboard attracts new members; the journal is the most used tool.

---

## 9. Piano di Manutenzione / Maintenance Plan

### 9.1 Piano Condiviso con Turni / Shared Schedule with Rotation

**Italiano:** I compiti sono distribuiti con calendario rotativo; ogni settimana un "membro di turno" fa la manutenzione di routine.

**English:** Tasks are distributed on a rotating schedule; each week a "member on duty" performs routine maintenance.

| Intervento / Task | Frequenza / Frequency | Ruolo / Role |
|-------------------|------------------------|--------------|
| **Pulizia sensori / Sensor cleaning** | Settimanale / Weekly | Membro di turno / Member on duty |
| **Controllo alimentazione / Power check** | Settimanale / Weekly | Membro di turno / Member on duty |
| **Backup database / Database backup** | Settimanale / Weekly | Amministratore / Admin |
| **Verifica cablaggi / Wiring check** | Mensile / Monthly | Coordinatore tecnico / Tech coordinator |
| **Calibrazione pH / pH calibration** | Mensile / Monthly | Coordinatore tecnico / Tech coordinator |
| **Calibrazione EC / EC calibration** | Bimestrale / Bi-monthly | Coordinatore tecnico / Tech coordinator |
| **Aggiornamento firmware / Firmware update** | Trimestrale / Quarterly | Coordinatore tecnico / Tech coordinator |
| **Revisione soglie / Threshold review** | Stagionale / Seasonal | Tutti / All members |
| **Sostituzione elettrodi / Electrode replacement** | Annuale / Annual | Coordinatore tecnico / Tech coordinator |

**Italiano:** Esempio di turni settimanali: 1 Marco, 2 Anna, 3 Luca, 4 Sara, poi si ripete.

**English:** Example weekly rotation: 1 Marco, 2 Anna, 3 Luca, 4 Sara, then repeats.

### 9.2 Emergenze / Emergency Procedure

**Italiano:**
1. **Segnalazione:** osservazione con tag `#emergenza`
2. **Notifica:** il sistema avvisa coordinatore tecnico e amministratore
3. **Intervento:** entro 24 ore
4. **Registrazione:** intervento nel diario con data e materiali
5. **Verifica:** dopo 48 ore, controllo della risoluzione

**English:**
1. **Report:** observation tagged `#emergency`
2. **Notification:** system alerts tech coordinator and admin
3. **Intervention:** within 24 hours
4. **Logging:** action in journal with date and materials
5. **Verification:** after 48 hours, confirm resolution

### 9.3 Budget di Manutenzione Annuale / Annual Maintenance Budget

| Voce / Item | Costo Annuale / Annual Cost |
|-------------|------------------------------|
| **Elettrodi pH/EC (sostituzione) / pH/EC electrodes (replacement)** | €60-100 |
| **Soluzioni di calibrazione / Calibration solutions** | €20-35 |
| **Sensori di ricambio / Spare sensors** | €25-50 |
| **Imprevisti / Contingency (cables, connectors)** | €30-50 |
| **TOTALE / TOTAL** | **≈ €135-235/anno** |

---

## 10. Appendice: Checklist di Avvio / Appendix: Startup Checklist

### 10.1 Checklist di Installazione / Installation Checklist

- [ ] Gateway Raspberry Pi installato e avviato
- [ ] MyZubsterGateway configurato e raggiungibile
- [ ] Dashboard accessibile via browser
- [ ] Hub ESP32 flashati e collegati
- [ ] Sensori installati in tutte le parcelle
- [ ] Copertura WiFi verificata
- [ ] Gruppo creato, membri invitati, parcelle assegnate
- [ ] Soglie di gruppo configurate
- [ ] Turni di manutenzione pianificati e budget comunicato

### 10.2 Checklist del Primo Mese / First-Month Checklist

- [ ] Calibrazione iniziale di tutti i sensori pH/EC
- [ ] Prima revisione delle soglie sui dati reali
- [ ] Sessione di formazione per i nuovi membri
- [ ] Confronto dati sensore vs misura manuale
- [ ] Primo report mensile e verifica degli alert

### 10.3 Riferimenti Incrociati / Cross-References

| Documento / Document | Riferimento / Reference |
|----------------------|-------------------------|
| `GUIDA_ORTO_INTELLIGENTE.md` | Guida pratica MyZubster (calibrazione, troubleshooting) |
| `legal/TERMS_OF_SERVICE.md` | Termini di servizio / Terms of service |
| `README.md` | Panoramica progetto / Project overview |

---

**📝 Note sulla Versione / Version Notes:**  
Template per orti comunitari (issue #15). Per suggerimenti, aprire una issue su GitHub o contattare il team.

**📝 Version Notes:**  
Community garden template (issue #15). For suggestions, open an issue on GitHub or contact the team.
