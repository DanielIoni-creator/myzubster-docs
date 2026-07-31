# Protocollo di Validazione Scientifica dei Sensori MyZubster / Scientific Validation Protocol for MyZubster Sensors

**Versione / Version:** 1.0.0  
**Data / Date:** 2026-07-31  
**Progetto / Project:** MyZubster Ecosystem  
**Issue di Riferimento / Reference Issue:** #14 — Validazione scientifica dei sensori / Scientific validation of sensors  
**Stato / Status:** Bozza per revisione community / Draft for community review

---

## Indice / Table of Contents

1. [Introduzione e Scopo / Introduction and Purpose](#1-introduzione-e-scopo--introduction-and-purpose)
2. [Metodologia / Methodology](#2-metodologia--methodology)
3. [Materiali Necessari / Required Materials](#3-materiali-necessari--required-materials)
4. [Procedura Passo-Passo / Step-by-Step Procedure](#4-procedura-passo-passo--step-by-step-procedure)
5. [Raccolta e Analisi Dati / Data Collection and Analysis](#5-raccolta-e-analisi-dati--data-collection-and-analysis)
6. [Risultati Attesi e Tolleranze / Expected Results and Tolerances](#6-risultati-attesi-e-tolleranze--expected-results-and-tolerances)
7. [Risoluzione Problemi / Troubleshooting](#7-risoluzione-problemi--troubleshooting)
8. [Template Report per Pubblicazione / Publication Report Template](#8-template-report-per-pubblicazione--publication-report-template)
9. [Documentazione Test di Ripetibilità / Repeatability Testing Documentation](#9-documentazione-test-di-ripetibilità--repeatability-testing-documentation)

---

## 1. Introduzione e Scopo / Introduction and Purpose

**Italiano:**  
Questo protocollo definisce una procedura scientifica, riproducibile e documentabile per validare l'accuratezza dei sensori MyZubster (pH, EC, temperatura) e dei dati raccolti dal sistema. Lo scopo è garantire che le misure pubblicate dal progetto open-source siano affidabili, confrontabili tra diversi orti e idonee a supportare decisioni agronomiche e pubblicazioni scientifiche. Il protocollo segue i principi della metrologia di base: calibrazione contro standard di riferimento, raccolta dati replicata, analisi statistica degli errori e report trasparente.

**English:**  
This protocol defines a scientific, reproducible, and documentable procedure to validate the accuracy of MyZubster sensors (pH, EC, temperature) and the data collected by the system. The goal is to ensure that measurements published by the open-source project are reliable, comparable across different gardens, and suitable for agronomic decisions and scientific publications. The protocol follows basic metrology principles: calibration against reference standards, replicated data collection, statistical error analysis, and transparent reporting.

### 1.1 Ambito di Applicazione / Scope of Application

| Sensore / Sensor | Misura / Measurement | Unità / Unit | Campo Tipico / Typical Range |
|------------------|----------------------|--------------|------------------------------|
| pH | Acidità/Alcalinità | pH | 0–14 (uso agricolo: 4.5–8.5) |
| EC | Conducibilità Elettrica | mS/cm | 0–10 (uso agricolo: 0.2–4.0) |
| Temperatura | Temperatura suolo/acqua | °C | −10 a +60 |

**Italiano:**  
Il protocollo si applica a tutti i nodi sensore Arduino/ESP32 che utilizzano i moduli standard MyZubster: sonda pH con elettrodo BNC, modulo EC K1.0, sensore temperatura DS18B20 (o equivalente calibrato).

**English:**  
The protocol applies to all Arduino/ESP32 sensor nodes using standard MyZubster modules: pH probe with BNC electrode, EC K1.0 module, DS18B20 temperature sensor (or calibrated equivalent).

---

## 2. Metodologia / Methodology

**Italiano:**  
La metodologia si articola in cinque fasi sequenziali, ciascuna con criteri di accettazione espliciti: **(1) Calibrazione** contro standard certificati (tamponi pH 4/7/10, standard EC 1413 µS/cm, termometro certificato); **(2) Misura di riferimento** con N ≥ 10 repliche per soluzione di prova; **(3) Confronto** con strumentazione certificata; **(4) Analisi statistica** (media, deviazione standard, errore percentuale, bias, limite di ripetibilità); **(5) Report e verdetto** PASS/FAIL secondo le tolleranze del §6.

**English:**  
The methodology consists of five sequential phases, each with explicit acceptance criteria: **(1) Calibration** against certified standards (pH buffers 4/7/10, EC standard 1413 µS/cm, certified thermometer); **(2) Reference measurement** with N ≥ 10 replicates per test solution; **(3) Comparison** with certified instrumentation; **(4) Statistical analysis** (mean, standard deviation, percentage error, bias, repeatability limit); **(5) Report and verdict** PASS/FAIL according to §6 tolerances.

### 2.1 Principi Guida / Guiding Principles

| Principio / Principle | Descrizione / Description |
|------------------------|---------------------------|
| Tracciabilità / Traceability | Ogni misura riconducibile a uno standard certificato / Every measurement traceable to a certified standard |
| Riproducibilità / Reproducibility | Procedura ripetibile da chiunque con lo stesso materiale / Procedure repeatable by anyone with the same material |
| Trasparenza / Transparency | Tutti i dati grezzi, inclusi gli anomali, vanno registrati / All raw data, including outliers, must be recorded |
| Indipendenza / Independence | Sensore in prova e riferimento non condividono lo stesso ADC / DUT and reference do not share the same ADC |

**Italiano:**  
Tutte le misure vanno registrate in un quaderno di laboratorio digitale (foglio di calcolo con timestamp). Nessun dato va scartato a posteriori senza giustificazione documentata.

**English:**  
All measurements must be recorded in a digital laboratory notebook (timestamped spreadsheet). No data point may be discarded retroactively without documented justification.

---

## 3. Materiali Necessari / Required Materials

| Materiale / Material | Specifiche / Specifications | Quantità / Qty | Scopo / Purpose |
|----------------------|------------------------------|----------------|-----------------|
| Tampone pH 4.00 / pH buffer 4.00 | Certificato, ±0.02 @ 25°C | 250 ml | Calibrazione punto basso / low point |
| Tampone pH 7.00 / pH buffer 7.00 | Certificato, ±0.02 @ 25°C | 250 ml | Calibrazione punto medio / mid point |
| Tampone pH 10.00 / pH buffer 10.00 | Certificato, ±0.02 @ 25°C | 250 ml | Verifica linearità / linearity check |
| Standard EC 1413 µS/cm / EC standard | Certificato (KCl), ±1% | 250 ml | Calibrazione EC |
| Acqua deionizzata / Deionized water | Resistività ≥ 18 MΩ·cm | 1 L | Pulizia sonde / probe cleaning |
| Termometro di riferimento / Reference thermometer | Certificato, risol. 0.1°C / cert., 0.1°C res. | 1 | Riferimento T° / temperature reference |
| Bicchieri 100 ml / Beakers 100 ml | Vetro/plastica puliti / clean glass/plastic | 6 | Contenitori di prova / test containers |
| Siringhe-pipette / Syringes-pipettes | 10 ml | 3 | Trasferimento liquidi / liquid transfer |
| Nodo in prova (DUT) / Device under test | Node ESP32 + moduli MyZubster | 1 | Dispositivo da validare / device to validate |
| Strumentazione logging / Logging setup | Dashboard / Serial Monitor → CSV | 1 | Acquisizione dati / data acquisition |

**Italiano:**  
Gli standard liquidi vanno conservati secondo le istruzioni del produttore e verificati per la data di scadenza prima dell'uso. Non riutilizzare soluzioni contaminate.

**English:**  
Liquid standards must be stored per manufacturer instructions and checked for expiry before use. Do not reuse contaminated solutions.

---

## 4. Procedura Passo-Passo / Step-by-Step Procedure

### 4.0 Preparazione Generale / General Preparation

**Italiano:**
1. Caricare il firmware MyZubster di test con logging grezzo (CSV: timestamp, ADC, valore convertito).
2. Collegare i sensori e lasciare stabilizzare ≥ 30 min a temperatura ambiente (20–25°C).
3. Etichettare i contenitori; registrare temperatura ambiente e orario di inizio.
4. Verificare disponibilità e validità del termometro di riferimento.

**English:**
1. Load the MyZubster test firmware with raw logging (CSV: timestamp, ADC, converted value).
2. Connect the sensors and let the system stabilize ≥ 30 min at room temperature (20–25°C).
3. Label all containers; record ambient temperature and start time.
4. Verify availability and validity of the reference thermometer.

### 4.1 Calibrazione Sensore pH / pH Sensor Calibration

**Italiano:**
1. **Pulizia / Cleaning**: immersione in acqua deionizzata 2 min, asciugare delicatamente.
2. **Punto 7.00**: immergere nel tampone pH 7.00, attendere 60 s; regolare il potenziometro offset finché il sistema legge 7.00 ± 0.05.
3. **Punto 4.00**: risciacquare, asciugare, immergere in pH 4.00, attendere 60 s; regolare il potenziometro slope finché legge 4.00 ± 0.05.
4. **Verifica 10.00**: risciacquare, immergere in pH 10.00, attendere 60 s, registrare. **Non regolare**: accettabile 10.00 ± 0.15 (linearità).
5. **Ripetizione**: ripetere 4.00 e 7.00; se la deriva supera ±0.10, ripetere l'intera calibrazione.

**English:**
1. **Cleaning**: immerse in deionized water 2 min, dry gently.
2. **Point 7.00**: immerse in pH 7.00 buffer, wait 60 s; adjust the offset potentiometer until the system reads 7.00 ± 0.05.
3. **Point 4.00**: rinse, dry, immerse in pH 4.00, wait 60 s; adjust the slope potentiometer until it reads 4.00 ± 0.05.
4. **10.00 check**: rinse, immerse in pH 10.00, wait 60 s, record. **Do not adjust**: acceptable 10.00 ± 0.15 (linearity).
5. **Repetition**: repeat 4.00 and 7.00; if drift exceeds ±0.10, repeat the entire calibration.

### 4.2 Calibrazione Sensore EC / EC Sensor Calibration

**Italiano:**
1. **Pulizia / Cleaning**: immergere la sonda in acqua deionizzata, asciugare.
2. **Punto 1413 µS/cm**: immergere nello standard a 25°C, attendere 60 s; regolare guadagno (o fattore K) finché legge 1.413 mS/cm ± 0.02.
3. **Compensazione T°**: abilitare la compensazione automatica (2%/°C per KCl); se assente, annotare la T° e correggere in post-analisi.
4. **Verifica opzionale**: con standard 2764 µS/cm, valore atteso 2.764 mS/cm ± 0.06.

**English:**
1. **Cleaning**: immerse the probe in deionized water, dry.
2. **Point 1413 µS/cm**: immerse in the standard at 25°C, wait 60 s; adjust gain (or K factor) until it reads 1.413 mS/cm ± 0.02.
3. **T° compensation**: enable automatic compensation (2%/°C for KCl); if absent, record T° and correct in post-analysis.
4. **Optional check**: with 2764 µS/cm standard, expected 2.764 mS/cm ± 0.06.

### 4.3 Verifica Sensore Temperatura / Temperature Sensor Verification

**Italiano:**
1. **Punto ghiaccio (0°C)**: bagno di ghiaccio fondente, immergere DS18B20 + riferimento, attendere 120 s, registrare. Atteso: 0.0 ± 0.5°C.
2. **Punto ambiente (20–25°C)**: 10 min all'ombra, confrontare con termometro certificato. Atteso: scostamento ≤ ±0.5°C.
3. **Punto caldo (≈40°C, opz.)**: acqua calda controllata, attendere 120 s. Atteso: ≤ ±0.5°C.
4. **Nota**: il DS18B20 non è regolabile in hardware; gli offset vanno corretti in software (`temp_offset`).

**English:**
1. **Ice point (0°C)**: melting ice bath, immerse DS18B20 + reference, wait 120 s, record. Expected: 0.0 ± 0.5°C.
2. **Ambient point (20–25°C)**: 10 min in shade, compare with certified thermometer. Expected: deviation ≤ ±0.5°C.
3. **Hot point (≈40°C, opt.)**: controlled warm water, wait 120 s. Expected: ≤ ±0.5°C.
4. **Note**: the DS18B20 cannot be calibrated in hardware; offsets must be corrected in software (`temp_offset`).

### 4.4 Esecuzione Misure di Validazione / Running Validation Measurements

**Italiano:**
1. Preparare **tre soluzioni di prova** distribuite sul campo operativo: acida (pH ~5.5, EC ~0.5 mS/cm), neutra (pH ~7.0, EC ~1.4), alcalina (pH ~8.0, EC ~2.5).
2. Per ogni soluzione e sensore, eseguire **N = 10 misure replicate** a intervalli di 60 s, a temperatura costante (25 ± 1°C).
3. Registrare ogni misura in CSV: timestamp, sensore, soluzione, ADC, valore convertito, temperatura.
4. Randomizzare l'ordine (es. A-B-C-B-A-C) per ridurre l'effetto deriva.
5. Al termine, misura di controllo su pH 7.00 per verificare assenza di deriva post-test (≤ ±0.10).

**English:**
1. Prepare **three test solutions** across the operating range: acidic (pH ~5.5, EC ~0.5 mS/cm), neutral (pH ~7.0, EC ~1.4), alkaline (pH ~8.0, EC ~2.5).
2. For each solution and sensor, run **N = 10 replicated measurements** at 60 s intervals, at constant temperature (25 ± 1°C).
3. Record every measurement in CSV: timestamp, sensor, solution, ADC, converted value, temperature.
4. Randomize the order (e.g., A-B-C-B-A-C) to reduce drift effects.
5. At the end, control measurement on pH 7.00 to verify no post-test drift (≤ ±0.10).

---

## 5. Raccolta e Analisi Dati / Data Collection and Analysis

### 5.1 Struttura Dati / Data Structure

| Campo / Field | Tipo / Type | Esempio / Example | Note / Notes |
|---------------|-------------|-------------------|--------------|
| timestamp | ISO 8601 | 2026-07-31T10:15:00+08:00 | Ora + fuso / time + zone |
| sensor_id | string | ph_01 | Identificativo univoco / unique ID |
| solution | string | A (acida / acidic) | Etichetta soluzione / solution label |
| adc_raw | int | 1823 | Valore grezzo ADC / raw ADC |
| value | float | 5.52 | Valore convertito / converted value |
| temp_c | float | 24.8 | Temperatura al momento / temperature at time |
| reference | float | 5.49 | Valore strumento di riferimento / reference value |

### 5.2 Statistiche da Calcolare / Statistics to Compute

**Italiano:**  
Per ogni combinazione sensore × soluzione, calcolare: **Media** `M = Σxᵢ/N`; **Deviazione standard** `SD = √(Σ(xᵢ−M)²/(N−1))`; **Errore percentuale** `E% = |M−R|/R × 100` (R = riferimento); **Bias sistematico** `B = M−R` (positivo = sovrastima); **Errore massimo** `Emax = max|xᵢ−R|`; **Limite di ripetibilità** `r = 2.77 × SD` (N=10, conf. 95%).

**English:**  
For each sensor × solution combination, compute: **Mean** `M = Σxᵢ/N`; **Standard deviation** `SD = √(Σ(xᵢ−M)²/(N−1))`; **Percentage error** `E% = |M−R|/R × 100` (R = reference); **Systematic bias** `B = M−R` (positive = overestimation); **Maximum error** `Emax = max|xᵢ−R|`; **Repeatability limit** `r = 2.77 × SD` (N=10, 95% conf.).

**Italiano:**  
Per N < 10 o distribuzioni non normali, riportare anche mediana e IQR. Segnalare esplicitamente gli outlier con giustificazione. Strumenti consigliati: Python (pandas/numpy), Google Sheets/Excel, Grafana.

**English:**  
For N < 10 or non-normal distributions, also report median and IQR. Explicitly flag outliers with justification. Recommended tools: Python (pandas/numpy), Google Sheets/Excel, Grafana.

---

## 6. Risultati Attesi e Tolleranze / Expected Results and Tolerances

**Italiano:**  
Le tolleranze definiscono il criterio PASS/FAIL per ciascuna grandezza e sono allineate alle specifiche dei moduli MyZubster e agli standard agricoli comuni.

**English:**  
The tolerances define the PASS/FAIL criterion for each quantity and are aligned with MyZubster module specifications and common agricultural standards.

#### pH

| Metrica / Metric | Tolleranza PASS / PASS Tolerance | Azione se FUORI / Action if OUT |
|------------------|----------------------------------|----------------------------------|
| Bias a pH 7.00 / Bias at pH 7.00 | ±0.10 | Ricalibrare offset / Recalibrate offset |
| Bias a pH 4.00 / Bias at pH 4.00 | ±0.15 | Ricalibrare slope / Recalibrate slope |
| Bias a pH 10.00 (linearità) | ±0.20 | Ricalibrazione completa / Full recalibration |
| Ripetibilità r (N=10) / Repeatability r | ≤ 0.10 pH | Verificare elettrodo/cavo / Check electrode/cable |
| Deriva post-test su 7.00 / Post-test drift | ≤ 0.10 pH | Pulire e ri-condizionare elettrodo / Clean and re-condition |

#### EC

| Metrica / Metric | Tolleranza PASS / PASS Tolerance | Azione se FUORI / Action if OUT |
|------------------|----------------------------------|----------------------------------|
| Bias a 1413 µS/cm / Bias at 1413 µS/cm | ±2% del valore / of value | Ricalibrare guadagno/K / Recalibrate gain/K |
| Bias a 2764 µS/cm (linearità) | ±3% del valore / of value | Verificare pulizia sonda / Check probe cleanliness |
| Ripetibilità r (N=10) | ≤ 2% del valore / of value | Verificare compensazione T° / Check T° compensation |
| Deriva in soluzione di prova (30 min) | ≤ 3% | Pulire sonda, controllare contatti / Clean probe, check contacts |

#### Temperatura

| Metrica / Metric | Tolleranza PASS / PASS Tolerance | Azione se FUORI / Action if OUT |
|------------------|----------------------------------|----------------------------------|
| Bias a 0°C (ghiaccio / ice) | ±0.5°C | Applicare offset software / Apply software offset |
| Bias a 20–25°C (ambiente) | ±0.5°C | Verificare contatto termico / Check thermal contact |
| Bias a 40°C (opz.) | ±0.5°C | Applicare offset software / Apply software offset |
| Ripetibilità r (N=10) | ≤ 0.3°C | Verificare cablaggio / Check wiring |

### 6.1 Verdetto Complessivo / Overall Verdict

| Verdetto / Verdict | Criterio / Criterion |
|--------------------|-----------------------|
| PASS | Tutte le metriche in tolleranza / All metrics within tolerance |
| FAIL con azione correttiva / FAIL with corrective action | Una sola metrica fuori tolleranza / A single metric out of tolerance |
| FAIL | ≥ 2 metriche fuori tolleranza o calibrazione non completabile / ≥ 2 metrics out of tolerance or calibration cannot be completed |

---

## 7. Risoluzione Problemi / Troubleshooting

| Sintomo / Symptom | Causa Probabile / Probable Cause | Soluzione / Solution |
|-------------------|----------------------------------|----------------------|
| Lettura pH instabile (±0.3) / Unstable pH | Elettrodo sporco/disidratato / dirty/dehydrated electrode | Pulire con HCl 0.1 M, ri-condizionare in KCl 3 M 24 h / clean with HCl 0.1 M, re-condition in KCl 3 M 24 h |
| pH fisso / Fixed pH | Cavo BNC danneggiato, elettrodo saturo / damaged BNC cable, saturated electrode | Sostituire elettrodo o cavo / Replace electrode or cable |
| Calibrazione pH impossibile / pH calibration fails | Elettrodo esaurito / exhausted electrode | Sostituire l'elettrodo / Replace the electrode |
| EC troppo alta/negativa / EC too high/negative | Sonda sporca o bolle d'aria / dirty probe or air bubbles | Pulire, agitare delicatamente / Clean, agitate gently |
| EC deriva durante il test / EC drift | Compensazione T° disabilitata / T° compensation disabled | Abilitare o correggere in post / Enable or correct post-hoc |
| T° errata 0.5–1°C / Wrong T° | Scarsa contatto termico / poor thermal contact | Immergere completamente, pasta termica / fully immerse, thermal paste |
| T° fissa (85/−55°C) / Fixed T° | Pull-up OneWire mancante / missing OneWire pull-up | Verificare pull-up 4.7 kΩ / Check 4.7 kΩ pull-up |
| Dati mancanti nel CSV / Missing CSV data | WiFi timeout, alimentazione instabile / WiFi timeout, unstable power | Buffer locale su SD, verificare alimentazione / local SD buffer, check power |
| Letture fuori scala / Out-of-range readings | Vref ADC errato / wrong ADC reference | Verificare tensione di riferimento / Check reference voltage |

**Italiano:**  
Registrare ogni intervento di manutenzione nel quaderno di laboratorio (data, problema, causa, azione, esito). Le manutenzioni invalidano le misure precedenti e richiedono una nuova calibrazione completa.

**English:**  
Record every maintenance intervention in the laboratory notebook (date, problem, cause, action, outcome). Maintenance invalidates previous measurements and requires full recalibration.

---

## 8. Template Report per Pubblicazione / Publication Report Template

**Italiano:**  
Template da compilare per ogni campagna di validazione e allegare alla documentazione dell'issue #14. Utilizzabile come base per pubblicazioni scientifiche o rapporti tecnici.

**English:**  
Template to complete for every validation campaign and attach to issue #14 documentation. Usable as a basis for scientific publications or technical reports.

### 8.1 Intestazione / Header

| Campo / Field | Valore / Value |
|---------------|----------------|
| Titolo / Title | Validazione sensori MyZubster — Campagna n. ___ |
| Data inizio / Start date | |
| Data fine / End date | |
| Operatore / Operator | |
| Posizione / Location | |
| Nodo sensore (ID) / Sensor node (ID) | |
| Firmware (versione) / Firmware (version) | |
| Condizioni ambientali / Ambient conditions | T: ___ °C, UR: ___ % |
| Riferimenti usati / References used | pH 4/7/10 lotto ___, EC 1413 lotto ___, termometro cert. n. ___ |

### 8.2 Risultati pH / pH Results

| Soluzione / Solution | Rif. / Ref. | Media / Mean | SD | E% | Bias | Emax | r (2.77·SD) | Verdetto / Verdict |
|----------------------|-------------|--------------|-----|----|------|------|-------------|---------------------|
| A (acida / acidic) | 5.49 | | | | | | | |
| B (neutra / neutral) | 7.00 | | | | | | | |
| C (alcalina / alkaline) | 8.02 | | | | | | | |

### 8.3 Risultati EC / EC Results

| Soluzione / Solution | Rif. (mS/cm) | Media / Mean | SD | E% | Bias | Emax | r (2.77·SD) | Verdetto / Verdict |
|----------------------|--------------|--------------|-----|----|------|------|-------------|---------------------|
| A (acida / acidic) | 0.51 | | | | | | | |
| B (neutra / neutral) | 1.41 | | | | | | | |
| C (alcalina / alkaline) | 2.48 | | | | | | | |

### 8.4 Risultati Temperatura / Temperature Results

| Punto / Point | Rif. (°C) | Media / Mean | SD | E% | Bias | Emax | r (2.77·SD) | Verdetto / Verdict |
|---------------|-----------|--------------|-----|----|------|------|-------------|---------------------|
| Ghiaccio / Ice | 0.00 | | | | | | | |
| Ambiente / Ambient | 22.4 | | | | | | | |
| Caldo / Hot | 39.8 | | | | | | | |

### 8.5 Sezione Narrativa / Narrative Section

- **Osservazioni / Observations** (outlier, eventi imprevisti, sostituzioni / outliers, unexpected events, replacements):  
- **Deviazioni dal protocollo / Deviations from the protocol** (se presenti e perché / if any, and why):  
- **Conclusioni / Conclusions** (verdetto complessivo, raccomandazioni / overall verdict, recommendations):  

### 8.6 Firme / Signatures

| Ruolo / Role | Nome / Name | Firma / Signature | Data / Date |
|--------------|-------------|-------------------|-------------|
| Operatore / Operator | | | |
| Revisore / Reviewer | | | |

---

## 9. Documentazione Test di Ripetibilità / Repeatability Testing Documentation

**Italiano:**  
I test di ripetibilità documentano la stabilità del sistema nel tempo e tra campagne. Obbligatori: (a) all'accensione di un nuovo nodo, (b) dopo ogni manutenzione, (c) almeno una volta per stagione di coltivazione.

**English:**  
Repeatability tests document system stability over time and across campaigns. Mandatory: (a) when commissioning a new node, (b) after any maintenance, (c) at least once per growing season.

### 9.1 Protocollo / Protocol

1. Eseguire la procedura completa del §4 sullo stesso nodo in **tre giorni distinti** (es. lun/mer/ven), alla stessa ora. / Run the complete §4 procedure on the same node on **three distinct days** (e.g., Mon/Wed/Fri), at the same time.
2. Usare soluzioni di prova **appena preparate** ogni giorno; conservare un campione del giorno 1 per confronto. / Use **freshly prepared** test solutions each day; keep a day-1 sample for comparison.
3. Per ogni giorno calcolare media, SD ed E% come da §5. / For each day compute mean, SD, and E% per §5.
4. La **deviazione massima tra le medie dei giorni** non deve superare 2 × r. / The **maximum deviation between daily means** must not exceed 2 × r.
5. Compilare il registro sottostante. / Complete the register below.

### 9.2 Registro / Register

| Giorno / Day | Data / Date | Media pH (B) | Media EC (B) | Media T° | SD pH | SD EC | SD T° | E% pH | E% EC | E% T° | Esito / Outcome |
|--------------|-------------|--------------|--------------|----------|-------|-------|-------|-------|-------|-------|-----------------|
| 1 | | | | | | | | | | | |
| 2 | | | | | | | | | | | |
| 3 | | | | | | | | | | | |
| Max Δ tra giorni / Max Δ across days | | | | | | | | | | | |
| Limite 2 × r / Limit 2 × r | | | | | | | | | | | |

### 9.3 Criterio di Accettazione / Acceptance Criterion

**Italiano:**  
Il nodo è **ripetibile** se: (1) ogni giornata singola è PASS secondo §6, e (2) la deviazione massima tra le medie dei tre giorni non supera 2 × r per nessuna grandezza. Altrimenti, investigare cause ambientali/hardware e ripetere il ciclo.

**English:**  
The node is **repeatable** if: (1) each individual day is PASS per §6, and (2) the maximum deviation between the three daily means does not exceed 2 × r for any quantity. Otherwise, investigate environmental/hardware causes and repeat the cycle.

---

## Appendice A: Checklist Rapida / Quick Checklist

- [ ] Standard liquidi in data di validità / liquid standards within expiry
- [ ] Termometro certificato disponibile / certified thermometer available
- [ ] Firmware di test con logging CSV attivo / test firmware with CSV logging active
- [ ] Stabilizzazione 30 min pre-calibrazione / 30-min stabilization before calibration
- [ ] Calibrazione pH: punti 7.00 e 4.00, verifica 10.00 / pH calibration: points 7.00 and 4.00, 10.00 check
- [ ] Calibrazione EC: punto 1413, verifica opz. 2764 / EC calibration: 1413 point, optional 2764 check
- [ ] Verifica temperatura: ghiaccio + ambiente (+ caldo opz.) / T° verification: ice + ambient (+ hot opt.)
- [ ] N = 10 repliche per ogni soluzione / N = 10 replicates per solution
- [ ] Statistiche calcolate (media, SD, E%, bias, Emax, r) / statistics computed
- [ ] Verdetto PASS/FAIL assegnato / PASS/FAIL verdict assigned
- [ ] Report compilato e registrato nell'issue #14 / report completed and recorded in issue #14
- [ ] Test di ripetibilità 3 giorni eseguito (se richiesto) / 3-day repeatability test performed (if required)

---

## Appendice B: Riferimenti / References

**Italiano:**  
- ISO 5725-1:1994 — Accuratezza (veridicità e precisione) dei metodi di misura / Accuracy (trueness and precision) of measurement methods
- Linee guida NIST per calibrazione di pH-metri e conduttimetri / NIST guidelines for pH and conductivity meter calibration
- Specifiche tecniche moduli MyZubster (repository ufficiale) / MyZubster module specs (official repo)
- Documentazione sensori: pH-4502C, EC K1.0, DS18B20 / Sensor documentation: pH-4502C, EC K1.0, DS18B20

---

**Licenza / License:** CC BY-SA 4.0 — Documento open-source della community MyZubster / Open-source document of the MyZubster community.
