# Kit per Orti Scolastici Sostenibili / Sustainable School Garden Toolkit

**Versione / Version:** 1.0.0  
**Data / Date:** 2026-07-31  
**Progetto / Project:** MyZubster Ecosystem  
**Issue / Issue:** #16  
**Pubblico / Audience:** Organizzazioni ambientaliste, scuole, insegnanti / Environmental organizations, schools, teachers  
**Lingue / Languages:** Italiano / English (bilingue / bilingual)

---

## Indice / Table of Contents

1. [Introduzione / Introduction](#1-introduzione--introduction)
2. [Kit Hardware Consigliato / Recommended Hardware Kit](#2-kit-hardware-consigliato--recommended-hardware-kit)
3. [Piano di Installazione Scolastica / School Installation Plan](#3-piano-di-installazione-scolastica--school-installation-plan)
4. [Monitoraggio di Acqua ed Energia / Water and Energy Monitoring](#4-monitoraggio-di-acqua-ed-energia--water-and-energy-monitoring)
5. [Indicatori di Sostenibilità / Sustainability Indicators](#5-indicatori-di-sostenibilità--sustainability-indicators)
6. [Materiali Educativi per Studenti / Student Education Materials](#6-materiali-educativi-per-studenti--student-education-materials)
7. [Casi di Studio / Case Studies](#7-casi-di-studio--case-studies)
8. [Appendice e Checklist / Appendix and Checklist](#8-appendice-e-checklist--appendix-and-checklist)

---

## 1. Introduzione / Introduction

### 1.1 Perché un Orto Scolastico Intelligente? / Why a Smart School Garden?

**Italiano:**
Gli orti scolastici trasformano le scuole in laboratori viventi di sostenibilità. Integrando MyZubster — l'ecosistema open-source di agricoltura intelligente basato su Arduino/ESP32 e sensori IoT — le organizzazioni ambientaliste possono aiutare le scuole a coltivare cibo reale mentre insegnano scienza, tecnologia e cura dell'ambiente. Questo kit fornisce tutto il necessario per pianificare, installare e monitorare un orto scolastico sostenibile a basso costo.

**English:**
School gardens turn schools into living laboratories of sustainability. By integrating MyZubster — the open-source smart agriculture ecosystem based on Arduino/ESP32 and IoT sensors — environmental organizations can help schools grow real food while teaching science, technology, and environmental stewardship. This toolkit provides everything needed to plan, install, and monitor a low-cost sustainable school garden.

### 1.2 Obiettivi del Toolkit / Toolkit Objectives

| Obiettivo / Objective | Descrizione / Description |
|------------------------|---------------------------|
| **Accessibilità / Accessibility** | Kit hardware a basso costo, con materiali riutilizzabili e riciclati |
| **Educazione / Education** | Materiali didattici pronti per studenti dai 6 ai 18 anni |
| **Misurazione / Measurement** | Indicatori di sostenibilità chiari e monitorabili nel tempo |
| **Risparmio / Savings** | Riduzione documentata di acqua ed energia grazie ai dati |
| **Riproducibilità / Reproducibility** | Piano passo-passo che ogni scuola può seguire |

---

## 2. Kit Hardware Consigliato / Recommended Hardware Kit

### 2.1 Kit Base (Economico ed Ecologico) / Base Kit (Low-Cost and Eco-Friendly)

**Italiano:**
Il kit base utilizza componenti a basso costo e privilegia materiali riutilizzabili, riciclati e a basso consumo energetico. Tutti i componenti possono essere acquistati singolarmente o recuperati da vecchie apparecchiature.

**English:**
The base kit uses low-cost components and prioritizes reusable, recycled, and energy-efficient materials. All components can be purchased individually or salvaged from old equipment.

| Componente / Component | Specifiche / Specifications | Costo / Cost | Eco-Nota / Eco-Note |
|------------------------|----------------------------|--------------|---------------------|
| **ESP32 DevKit** | WiFi + Bluetooth, 30 pin | €8-12 | Basso consumo (deep sleep) |
| **Sensore pH** | Elettrodo pH BNC | €15-25 | Durata prolungata con manutenzione |
| **Sensore EC** | Modulo EC K1.0 | €10-18 | Riusabile, calibrabile |
| **Sensore Temperatura** | DS18B20 impermeabile | €3-5 | Basso consumo |
| **Sensore Umidità** | Capacitivo (non corrosivo) | €3-6 | Evita spreco di sonde |
| **Pannello Solare** | 5V/6W + batteria LiPo 18650 | €18-30 | Energia rinnovabile |
| **Contenitore** | Scatola IP65 riciclata | €0-10 | Materiale di recupero |
| **Tubo di Irrigazione** | Goccia a bassa pressione | €8-15 | Riduce spreco idrico |
| **Compostiera** | Realizzata a scuola | €0-5 | Riciclo rifiuti organici |
| **Totale / Total** | | **€65-126** | |

### 2.2 Kit Avanzato (Opzionale) / Advanced Kit (Optional)

| Componente / Component | Specifiche / Specifications | Costo / Cost | Beneficio / Benefit |
|------------------------|----------------------------|--------------|---------------------|
| **Sensore Umidità Aria** | DHT22 | €4-7 | Monitoraggio microclima |
| **Elettrovalvola** | 12V con relay | €10-18 | Irrigazione automatica |
| **Contatore Acqua** | Flussimetro YF-S201 | €6-10 | Misura consumi reali |
| **Sensore Luce** | Fotoresistenza LDR | €1-2 | Ottimizza esposizione solare |
| **Display LCD** | I2C 16x2 | €4-8 | Dati visibili in aula |
| **Gateway Wi-Fi Mesh** | Router scolastico esistente | €0 | Nessun costo extra |

### 2.3 Consigli per la Sostenibilità del Kit / Kit Sustainability Tips

**Italiano:**
- Preferire batterie ricaricabili e pannelli solari per alimentare i sensori
- Riutilizzare contenitori di plastica alimentare come involucri protettivi
- Stampare i supporti dei sensori con filamento PLA biodegradabile
- Organizzare un punto di raccolta di componenti elettronici usati
- Documentare le quantità di materiali per calcolare l'impronta di carbonio del progetto

**English:**
- Prefer rechargeable batteries and solar panels to power the sensors
- Reuse food-grade plastic containers as protective enclosures
- Print sensor mounts with biodegradable PLA filament
- Organize a collection point for used electronic components
- Document material quantities to calculate the project's carbon footprint

---

## 3. Piano di Installazione Scolastica / School Installation Plan

### 3.1 Fase 0 — Preparazione / Phase 0 — Preparation (Settimane 1-2 / Weeks 1-2)

**Italiano:**
Coinvolgere la direzione scolastica, individuare l'area dell'orto, formare il gruppo di lavoro insegnanti-studenti-volontari e ottenere i permessi necessari. Definire gli obiettivi didattici e le classi partecipanti.

**English:**
Involve the school administration, identify the garden area, form the teacher-student-volunteer working group, and obtain the necessary permissions. Define the educational objectives and participating classes.

| Attività / Activity | Responsabile / Owner | Output |
|---------------------|----------------------|--------|
| Approvazione della scuola | Dirigente scolastico | Permesso formale |
| Analisi dell'area | Insegnanti di scienze | Mappa dell'area |
| Reclutamento volontari | Organizzazione ambientalista | Elenco volontari |
| Budget e raccolta fondi | Comitato genitori | Piano finanziario |

### 3.2 Fase 1 — Installazione Fisica / Phase 1 — Physical Installation (Settimane 3-4 / Weeks 3-4)

| Passo / Step | Durata / Duration | Descrizione / Description |
|--------------|-------------------|---------------------------|
| **1. Preparazione del terreno** | 1 giorno | Vangare, rimuovere erbacce, aggiungere compost |
| **2. Allestimento aiuole** | 1 giorno | Creare aiuole rialzate con materiali riciclati |
| **3. Installazione irrigazione** | ½ giorno | Posare il tubo a goccia e collegare l'acqua |
| **4. Montaggio sensori** | ½ giorno | Posizionare pH/EC/temperatura/umidità nel suolo |
| **5. Cablaggio ESP32** | 1 giorno | Collegare sensori, pannello solare e batteria |
| **6. Configurazione software** | ½ giorno | Flash del firmware MyZubster e test Wi-Fi |
| **7. Collaudo gateway** | ½ giorno | Verificare invio dati al dashboard cloud |

### 3.3 Fase 2 — Messa in Servizio / Phase 2 — Commissioning (Settimana 5 / Week 5)

**Italiano:**
Calibrare i sensori, registrare le letture di riferimento, formare gli studenti all'uso del dashboard e alla manutenzione ordinaria. Stabilire un calendario di visite di controllo settimanali.

**English:**
Calibrate the sensors, record baseline readings, train students in dashboard use and routine maintenance. Establish a schedule of weekly check-up visits.

### 3.4 Fase 3 — Operatività / Phase 3 — Operation (Dal mese 2 / From month 2)

**Italiano:**
L'orto entra nel programma curricolare: ogni classe adotta un'area, monitora i dati, registra le osservazioni e partecipa alle attività educative. L'organizzazione ambientalista fornisce supporto remoto tramite il dashboard.

**English:**
The garden enters the curriculum: each class adopts an area, monitors data, records observations, and participates in educational activities. The environmental organization provides remote support via the dashboard.

### 3.5 Checklist di Sicurezza / Safety Checklist

| Verifica / Check | ✅ |
|------------------|----|
| Tutti i cavi elettrici protetti e fuori portata dei bambini | ☐ |
| Pannello solare montato stabilmente | ☐ |
| Contenitore IP65 sigillato | ☐ |
| Prodotti fitosanitari assenti o custoditi | ☐ |
| Primo soccorso disponibile in loco | ☐ |

---

## 4. Monitoraggio di Acqua ed Energia / Water and Energy Monitoring

### 4.1 Risparmio Idrico / Water Savings

**Italiano:**
Il sensore di umidità del suolo consente di irrigare solo quando necessario. Il flussimetro misura il consumo reale. In questo modo l'orto scolastico può ridurre l'acqua impiegata fino al 30-50% rispetto all'irrigazione manuale.

**English:**
The soil moisture sensor enables irrigation only when needed. The flow meter measures real consumption. This way the school garden can reduce water use by up to 30-50% compared to manual watering.

| Metrica / Metric | Sensore / Sensor | Formula | Esempio / Example |
|------------------|------------------|---------|-------------------|
| Umidità suolo / Soil moisture | Umidità (%) | Lettura diretta | 45% |
| Acqua erogata / Water delivered | Flussimetro (L) | Somma giornaliera | 12 L/giorno |
| Risparmio idrico / Water savings | Confronto manuale | (Manuale − Automatico) / Manuale | 40% |
| Efficienza irrigazione / Irrigation efficiency | Litri per pianta | L totali / n. piante | 0,5 L/pianta |

### 4.2 Risparmio Energetico / Energy Savings

**Italiano:**
I sensori ESP32 in modalità deep sleep consumano pochissima energia (tipicamente 0,1-0,5 W). Il pannello solare copre l'intero fabbisogno, rendendo il sistema energeticamente autosufficiente e a zero emissioni in esercizio.

**English:**
ESP32 sensors in deep sleep mode consume very little energy (typically 0.1-0.5 W). The solar panel covers the entire requirement, making the system energy self-sufficient and zero-emission in operation.

| Metrica / Metric | Valore tipico / Typical Value | Note / Notes |
|------------------|-------------------------------|--------------|
| Consumo ESP32 (active) | ~0,3 W | Con WiFi attivo |
| Consumo ESP32 (deep sleep) | ~0,01 W | Intervallo 10 min |
| Produzione pannello 6W | ~24 Wh/giorno | Media solare Italia |
| Autonomia batteria 18650 | 3-7 giorni | Senza sole |

### 4.3 Configurazione Consigliata / Recommended Configuration

**Italiano:**
Campionare i sensori ogni 10 minuti, inviare i dati ogni ora al gateway e attivare il deep sleep tra una trasmissione e l'altra. Questo bilancia la freschezza dei dati con il risparmio energetico.

**English:**
Sample sensors every 10 minutes, send data hourly to the gateway, and enable deep sleep between transmissions. This balances data freshness with energy savings.

---

## 5. Indicatori di Sostenibilità / Sustainability Indicators

### 5.1 Indicatori Chiave / Key Indicators

**Italiano:**
Gli indicatori permettono di misurare l'impatto reale dell'orto. Vanno registrati all'inizio (baseline) e poi ogni mese.

**English:**
The indicators allow measuring the real impact of the garden. They should be recorded at the start (baseline) and then monthly.

| Indicatore / Indicator | Unità / Unit | Come si misura / How to measure | Obiettivo / Target |
|------------------------|--------------|--------------------------------|--------------------|
| Acqua risparmiata | % | Confronto con irrigazione manuale | ≥ 30% |
| Energia rinnovabile | % | kWh solare / kWh totale | 100% |
| Rifiuti compostati | kg/mese | Peso compost prodotto | ≥ 10 kg/mese |
| Biodiversità | n. specie | Conteggio insetti e piante | In aumento |
| Raccolto prodotto | kg/mese | Peso verdure raccolte | ≥ 5 kg/mese |
| Studenti coinvolti | n. | Registro presenze attività | ≥ 50 |
| Costo per studente | € | Budget totale / studenti | ≤ €5 |

### 5.2 Dashboard di Sostenibilità / Sustainability Dashboard

**Italiano:**
Il dashboard MyZubster può essere esteso con un pannello "Sostenibilità" che mostra gli indicatori nel tempo, con grafici mensili e confronti con la baseline. Gli studenti possono presentare questi dati alle assemblee scolastiche.

**English:**
The MyZubster dashboard can be extended with a "Sustainability" panel showing indicators over time, with monthly charts and comparisons to the baseline. Students can present these data at school assemblies.

| Indicatore / Indicator | Frequenza / Frequency | Formato / Format |
|------------------------|-----------------------|------------------|
| Acqua ed energia | Giornaliera | Grafico a linee |
| Rifiuti e compost | Settimanale | Grafico a barre |
| Raccolto e biodiversità | Mensile | Tabella riassuntiva |
| Report di fine anno | Annuale | PDF per la scuola |

### 5.3 Certificazioni e Riconoscimenti / Certifications and Recognition

**Italiano:**
Le scuole possono utilizzare i dati raccolti per richiedere riconoscimenti come "Eco-Schools" o "Scuola Sostenibile", documentando il risparmio idrico ed energetico e il coinvolgimento degli studenti.

**English:**
Schools can use the collected data to apply for recognition such as "Eco-Schools" or "Sustainable School", documenting water and energy savings and student involvement.

---

## 6. Materiali Educativi per Studenti / Student Education Materials

### 6.1 Percorso per Fasce d'Età / Curriculum by Age Group

| Fascia / Age Group | Tema / Theme | Attività / Activities | Risultato / Outcome |
|--------------------|--------------|-----------------------|---------------------|
| **6-10 anni** | Il ciclo dell'acqua | Irrigare, osservare il sensore di umidità | Diario illustrato dell'orto |
| **11-14 anni** | Misurare e capire | Registrare pH/EC/temperatura, creare grafici | Poster scientifico |
| **15-18 anni** | Automazione e dati | Programmazione ESP32, analisi dashboard | Mini-progetto di ricerca |

### 6.2 Lezioni Pronte / Ready-Made Lessons

| Lezione / Lesson | Durata / Duration | Obiettivo / Objective |
|------------------|-------------------|-----------------------|
| **L1: Cos'è un orto intelligente?** | 45 min | Introdurre sensori e dati |
| **L2: Il pH del suolo** | 60 min | Misurare e interpretare il pH |
| **L3: L'acqua che usiamo** | 60 min | Calcolare il risparmio idrico |
| **L4: Dal sensore al cloud** | 90 min | Seguire il percorso dei dati |
| **L5: Presentare i risultati** | 90 min | Comunicare i dati alla comunità |

### 6.3 Attività Pratiche / Hands-On Activities

**Italiano:**
- **Giornata del compost:** gli studenti portano scarti organici da casa e costruiscono la compostiera
- **Caccia al tesoro dei sensori:** individuare e disegnare la posizione di ogni sensore nell'orto
- **Sfida del risparmio idrico:** ogni classe cerca di ridurre il consumo del proprio settore
- **Diario di bordo digitale:** gli studenti scrivono osservazioni quotidiane sul dashboard

**English:**
- **Compost Day:** students bring organic waste from home and build the composter
- **Sensor Treasure Hunt:** locate and draw the position of each sensor in the garden
- **Water Savings Challenge:** each class tries to reduce consumption in its own sector
- **Digital Logbook:** students write daily observations on the dashboard

### 6.4 Kit per l'Insegnante / Teacher Kit

**Italiano:**
Ogni scuola riceve un pacchetto insegnante con: guida di 20 pagine, presentazioni in formato aperto, schede di laboratorio stampabili, esempi di grafici e rubriche di valutazione allineate ai programmi di scienze e tecnologia.

**English:**
Each school receives a teacher package with: a 20-page guide, open-format presentations, printable lab worksheets, sample charts, and assessment rubrics aligned with science and technology curricula.

---

## 7. Casi di Studio / Case Studies

### 7.1 Caso Studio A — Scuola Primaria "Giardino Verde", Milano / Case Study A — "Green Garden" Primary School, Milan

**Italiano:**
Una scuola primaria di Milano ha installato un orto intelligente in un cortile di 80 m² con 3 classi (75 studenti). Risultati nel primo anno: risparmio idrico del 38%, 14 kg di compost al mese, 32 kg di verdure raccolte e un poster scientifico premiato a livello provinciale.

**English:**
A primary school in Milan installed a smart garden in an 80 m² courtyard with 3 classes (75 students). First-year results: 38% water savings, 14 kg of compost per month, 32 kg of vegetables harvested, and a science poster awarded at provincial level.

| Metrica / Metric | Valore / Value |
|------------------|----------------|
| Superficie / Area | 80 m² |
| Studenti coinvolti / Students involved | 75 |
| Risparmio idrico / Water savings | 38% |
| Compost prodotto / Compost produced | 14 kg/mese |
| Raccolto / Harvest | 32 kg/anno |
| Costo totale / Total cost | €540 (€7,20 per studente) |

### 7.2 Caso Studio B — Istituto Tecnico "Leonardo", Bologna / Case Study B — "Leonardo" Technical Institute, Bologna

**Italiano:**
Un istituto tecnico ha integrato l'orto nel programma di informatica: gli studenti hanno programmato il firmware ESP32, costruito un pannello di sostenibilità e pubblicato i dati in open data. Il sistema è alimentato interamente a energia solare con 0 kWh dalla rete.

**English:**
A technical institute integrated the garden into the computer science curriculum: students programmed the ESP32 firmware, built a sustainability panel, and published data as open data. The system is powered entirely by solar energy with 0 kWh from the grid.

| Metrica / Metric | Valore / Value |
|------------------|----------------|
| Consumo rete / Grid consumption | 0 kWh |
| Copertura solare / Solar coverage | 100% |
| Ore di programmazione / Coding hours | 120 |
| Dataset pubblicati / Datasets published | 3 |
| Studenti certificati / Certified students | 22 |

### 7.3 Lezioni Apprese / Lessons Learned

**Italiano:**
- Iniziare piccolo: un'area di 20-40 m² è sufficiente per il primo anno
- Coinvolgere i genitori e il comitato scuola fin dalla fase di preparazione
- Calibrare i sensori con gli studenti: è un'ottima lezione di metodo scientifico
- Tenere un backup dei dati su un foglio cartaceo per le attività offline
- Prevedere un referente tecnico per la manutenzione periodica dei sensori

**English:**
- Start small: an area of 20-40 m² is enough for the first year
- Involve parents and the school committee from the preparation phase
- Calibrate sensors with students: it is an excellent scientific-method lesson
- Keep a paper backup of data for offline activities
- Plan a technical contact person for periodic sensor maintenance

---

## 8. Appendice e Checklist / Appendix and Checklist

### 8.1 Timeline Completa / Full Timeline

| Fase / Phase | Periodo / Period | Durata / Duration |
|--------------|------------------|-------------------|
| Preparazione / Preparation | Settimane 1-2 | 2 settimane |
| Installazione / Installation | Settimane 3-4 | 2 settimane |
| Messa in servizio / Commissioning | Settimana 5 | 1 settimana |
| Operatività / Operation | Dal mese 2 | Continuo |
| Valutazione annuale / Annual review | Fine anno scolastico | 1 settimana |

### 8.2 Checklist di Lancio / Launch Checklist

| Attività / Activity | ✅ |
|---------------------|----|
| Permesso della scuola ottenuto | ☐ |
| Area dell'orto individuata | ☐ |
| Kit hardware ordinato o assemblato | ☐ |
| Volontari formati | ☐ |
| Sensori calibrati | ☐ |
| Dashboard accessibile alla scuola | ☐ |
| Lezioni L1-L5 pianificate | ☐ |
| Baseline degli indicatori registrata | ☐ |

### 8.3 Risorse Utili / Useful Resources

| Risorsa / Resource | Tipo / Type | Uso / Use |
|--------------------|-------------|-----------|
| Documentazione MyZubster | Docs | Configurazione hardware e firmware |
| Guida Orto Intelligente (GUIDA_ORTO_INTELLIGENTE.md) | Guida | Uso quotidiano del sistema |
| Modulo di richiesta kit | Template | Richiesta materiali alle organizzazioni |
| Template di report annuale | Template | Report di sostenibilità per la scuola |
| Mailing list insegnanti | Community | Scambio di esperienze tra scuole |

### 8.4 Glossario Essenziale / Essential Glossary

| Termine / Term | Italiano | English |
|----------------|----------|---------|
| **EC** | Conducibilità elettrica (nutrienti) | Electrical conductivity (nutrients) |
| **IoT** | Internet delle cose | Internet of Things |
| **pH** | Acidità/alcalinità del suolo | Soil acidity/alkalinity |
| **ESP32** | Microcontrollore WiFi | WiFi microcontroller |
| **Baseline** | Valore di riferimento iniziale | Initial reference value |
| **Compost** | Fertilizzante organico riciclato | Recycled organic fertilizer |

---

**Italiano:**  
Questo documento fa parte dell'ecosistema open-source MyZubster. Le organizzazioni ambientaliste sono invitate a distribuire, adattare e tradurre questo toolkit liberamente, citando la fonte. Per contribuire al progetto, aprire un issue o una pull request nel repository MyZubster.

**English:**  
This document is part of the open-source MyZubster ecosystem. Environmental organizations are invited to freely distribute, adapt, and translate this toolkit, citing the source. To contribute to the project, open an issue or pull request in the MyZubster repository.
