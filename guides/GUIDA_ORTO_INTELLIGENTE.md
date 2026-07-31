# Guida Pratica per l'Uso dell'Orto Intelligente / Practical Guide to Smart Gardening

**Versione / Version:** 1.0.0  
**Data / Date:** 2026-07-31  
**Progetto / Project:** MyZubster Ecosystem  
**Pubblico / Audience:** Agricoltori, appassionati di giardinaggio / Farmers, gardening enthusiasts

---

## Indice / Table of Contents

1. [Introduzione a MyZubster / Introduction to MyZubster](#1-introduzione-a-myzubster--introduction-to-myzubster)
2. [Configurazione dell'Orto Intelligente / Smart Garden Setup](#2-configurazione-dellorto-intelligente--smart-garden-setup)
3. [Interpretazione dei Dati / Data Interpretation](#3-interpretazione-dei-dati--data-interpretation)
4. [Manutenzione e Calibrazione / Maintenance and Calibration](#4-manutenzione-e-calibrazione--maintenance-and-calibration)
5. [Risoluzione dei Problemi / Troubleshooting](#5-risoluzione-dei-problemi--troubleshooting)

---

## 1. Introduzione a MyZubster / Introduction to MyZubster

### 1.1 Cos'è MyZubster? / What is MyZubster?

**Italiano:**  
MyZubster è un ecosistema open-source per l'agricoltura intelligente che combina hardware Arduino/ESP32, sensori IoT e una piattaforma cloud per monitorare e ottimizzare la crescita delle piante. Il sistema raccoglie dati in tempo reale su pH, EC (Conducibilità Elettrica), temperatura e umidità del suolo, permettendoti di prendere decisioni informate per colture più sane e produttive.

**English:**  
MyZubster is an open-source ecosystem for smart agriculture that combines Arduino/ESP32 hardware, IoT sensors, and a cloud platform to monitor and optimize plant growth. The system collects real-time data on pH, EC (Electrical Conductivity), temperature, and soil moisture, enabling you to make informed decisions for healthier, more productive crops.

### 1.2 Componenti Principali / Main Components

| Componente / Component | Descrizione / Description | Funzione / Function |
|------------------------|---------------------------|---------------------|
| **Arduino/ESP32** | Microcontrollore principale | Elabora i dati dei sensori e li invia al gateway |
| **Sensore pH** | Elettrodo pH | Misura l'acidità/alcalinità del suolo (0-14 pH) |
| **Sensore EC** | Sensore di conducibilità | Misura i nutrienti disciolti nel suolo (mS/cm) |
| **Sensore Temperatura** | DS18B20 o simile | Monitora la temperatura del suolo e dell'aria |
| **Sensore Umidità** | Capacitivo o resistivo | Misura il contenuto d'acqua del suolo (%) |
| **MyZubsterGateway** | Server API | Riceve, archivia e visualizza i dati raccolti |
| **Dashboard Web** | Interfaccia utente | Mostra mappe, grafici e alert in tempo reale |

### 1.3 Vantaggi per l'Agricoltore / Benefits for Farmers

**Italiano:**  
- Risparmio idrico fino al 30% grazie al monitoraggio preciso dell'umidità  
- Ottimizzazione della fertilizzazione basata su dati reali  
- Riduzione dei costi di manutenzione grazie alla diagnostica predittiva  
- Tracciabilità completa per certificazioni biologiche  
- Accesso mobile per il monitoraggio da qualsiasi luogo  

**English:**  
- Up to 30% water savings through precise moisture monitoring  
- Fertilization optimization based on real data  
- Reduced maintenance costs thanks to predictive diagnostics  
- Complete traceability for organic certifications  
- Mobile access for monitoring from anywhere  

---

## 2. Configurazione dell'Orto Intelligente / Smart Garden Setup

### 2.1 Hardware Consigliato / Recommended Hardware

#### Kit Base per Piccoli Orti / Basic Kit for Small Gardens

| Componente / Component | Specifiche / Specifications | Costo Stimato / Estimated Cost |
|------------------------|----------------------------|--------------------------------|
| **ESP32 DevKit V1** | WiFi + Bluetooth, 30 pin | €8-12 |
| **Sensore pH** | Elettrodo pH con sonda BNC | €15-25 |
| **Sensore EC** | Modulo EC con sonda K1.0 | €10-18 |
| **Sensore Temperatura** | DS18B20 (impermeabile) | €3-5 |
| **Sensore Umidità** | Capacitivo FC-28 (non corrosivo) | €3-6 |
| **Alimentazione** | Pannello solare 5V + batteria LiPo | €20-35 |
| **Cavi e Connettori** | Impermeabili, 20AWG | €5-10 |
| **Contenitore** | Scatola stagna IP65 | €8-15 |
| **Totale / Total** | | **€72-126** |

#### Kit Avanzato per Orti Professionali / Advanced Kit for Professional Gardens

| Componente / Component | Specifiche / Specifications | Costo Stimato / Estimated Cost |
|------------------------|----------------------------|--------------------------------|
| **ESP32-S3** | Più potente, AI edge | €12-18 |
| **Sensore pH industriale** | Sonda PH-4502C, precisione ±0.1 | €40-60 |
| **Sensore EC industriale** | Conducibilità 0-20 mS/cm | €30-45 |
| **Sensore Temperatura** | PT100, precisione ±0.1°C | €15-25 |
| **Sensore Umidità** | Teros 10 o VWC professionale | €25-40 |
| **Alimentazione** | Pannello solare 10W + batteria 12V | €40-60 |
| **Colonnina montante** | Alluminio, 1.5m, con morsetti | €30-50 |
| **Schermatur UV** | Protezione sensori | €10-15 |
| **Totale / Total** | | **€222-313** |

### 2.2 Installazione Hardware / Hardware Installation

**Italiano:**

1. **Posizionamento dei Sensori**  
   - Inserire il sensore di umidità a 10-15 cm di profondità, nella zona radicolare  
   - Posizionare il sensore pH e EC a 20 cm di distanza per evitare interferenze  
   - Il sensore temperatura va in ombra, a contatto con il suolo  

2. **Collegamento Elettrico**  
   - Collegare i sensori analogici ai pin ADC dell'ESP32 (GPIO 34, 35, 36)  
   - Usare resistenze pull-up per i sensori digitali (DS18B20)  
   - Proteggere tutti i collegamenti con guaina termoretraibile  

3. **Alimentazione**  
   - Per esterni, preferire pannello solare + batteria LiFePO₄  
   - Dimensionare la batteria per 3 giorni di autonomia (senza sole)  
   - Usare regolatore di carica MPPT per massima efficienza  

**English:**

1. **Sensor Placement**  
   - Insert the moisture sensor at 10-15 cm depth, in the root zone  
   - Position pH and EC sensors 20 cm apart to avoid interference  
   - Place the temperature sensor in shade, in contact with the soil  

2. **Electrical Connections**  
   - Connect analog sensors to ESP32 ADC pins (GPIO 34, 35, 36)  
   - Use pull-up resistors for digital sensors (DS18B20)  
   - Protect all connections with heat-shrink tubing  

3. **Power Supply**  
   - For outdoor use, prefer solar panel + LiFePO₄ battery  
   - Size the battery for 3 days of autonomy (without sun)  
   - Use MPPT charge controller for maximum efficiency  

### 2.3 Configurazione Software / Software Setup

**Italiano:**

1. **Installazione Firmware ESP32**  
   ```cpp
   // Esempio codice Arduino per MyZubster
   #include <WiFi.h>
   #include <HTTPClient.h>
   
   const char* ssid = "TUA_RETE_WIFI";
   const char* password = "TUA_PASSWORD";
   const char* serverUrl = "http://myzubster-gateway/api/garden/data";
   
   void setup() {
     Serial.begin(115200);
     WiFi.begin(ssid, password);
     
     while (WiFi.status() != WL_CONNECTED) {
       delay(500);
       Serial.print(".");
     }
     Serial.println("Connesso al WiFi");
   }
   
   void loop() {
     float ph = readPH();
     float ec = readEC();
     float temp = readTemperature();
     float humidity = readHumidity();
     
     String payload = "{\"gardenId\":\"mio-orto\",";
     payload += "\"ph\":" + String(ph) + ",";
     payload += "\"ec\":" + String(ec) + ",";
     payload += "\"temperature\":" + String(temp) + ",";
     payload += "\"humidity\":" + String(humidity) + "}";
     
     HTTPClient http;
     http.begin(serverUrl);
     http.addHeader("Content-Type", "application/json");
     int httpCode = http.POST(payload);
     http.end();
     
     delay(300000); // Invia ogni 5 minuti
   }
   ```

2. **Configurazione Gateway**  
   - Clonare il repository `MyZubsterGateway`  
   - Configurare il file `.env` con le credenziali del database  
   - Avviare il servizio con PM2 o Docker  

3. **Accesso alla Dashboard**  
   - Aprire `http://localhost:3000` nel browser  
   - Creare un account utente  
   - Registrare il proprio orto tramite l'app mobile o la dashboard web  

**English:**

1. **ESP32 Firmware Installation**  
   ```cpp
   // Example Arduino code for MyZubster
   #include <WiFi.h>
   #include <HTTPClient.h>
   
   const char* ssid = "YOUR_WIFI_NETWORK";
   const char* password = "YOUR_PASSWORD";
   const char* serverUrl = "http://myzubster-gateway/api/garden/data";
   
   void setup() {
     Serial.begin(115200);
     WiFi.begin(ssid, password);
     
     while (WiFi.status() != WL_CONNECTED) {
       delay(500);
       Serial.print(".");
     }
     Serial.println("Connected to WiFi");
   }
   
   void loop() {
     float ph = readPH();
     float ec = readEC();
     float temp = readTemperature();
     float humidity = readHumidity();
     
     String payload = "{\"gardenId\":\"my-garden\",";
     payload += "\"ph\":" + String(ph) + ",";
     payload += "\"ec\":" + String(ec) + ",";
     payload += "\"temperature\":" + String(temp) + ",";
     payload += "\"humidity\":" + String(humidity) + "}";
     
     HTTPClient http;
     http.begin(serverUrl);
     http.addHeader("Content-Type", "application/json");
     int httpCode = http.POST(payload);
     http.end();
     
     delay(300000); // Send every 5 minutes
   }
   ```

2. **Gateway Configuration**  
   - Clone the `MyZubsterGateway` repository  
   - Configure the `.env` file with database credentials  
   - Start the service with PM2 or Docker  

3. **Dashboard Access**  
   - Open `http://localhost:3000` in your browser  
   - Create a user account  
   - Register your garden via the mobile app or web dashboard  

---

## 3. Interpretazione dei Dati / Data Interpretation

### 3.1 Guida Rapida ai Parametri / Quick Parameter Guide

| Parametro / Parameter | Simbolo / Symbol | Range Ottimale / Optimal Range | Unità / Unit | Significato / Meaning |
|----------------------|------------------|--------------------------------|--------------|----------------------|
| **pH del Suolo / Soil pH** | pH | 6.0 - 7.0 | pH | Acidità/Alcalinità / Acidity/Alkalinity |
| **Conducibilità Elettrica / EC** | EC | 1.0 - 2.5 | mS/cm | Nutrienti disponibili / Available nutrients |
| **Temperatura Suolo / Soil Temp** | T | 18 - 25 | °C | Attività microbica / Microbial activity |
| **Umidità Suolo / Soil Moisture** | H | 40 - 70 | % | Acqua disponibile / Available water |

### 3.2 pH: La Scala del Suolo / pH: The Soil Scale

**Italiano:**

Il pH del suolo misura l'acidità o l'alcalinità su una scala da 0 a 14:

- **pH < 6.0 (Acido):** Le piante come fragole, patate e mirtilli prosperano in terreni acidi. Aggiungi solfato di calcio (gesso) per alzare il pH.
- **pH 6.0-7.0 (Neutro):** Range ideale per la maggior parte delle verdure (pomodori, lattuga, zucchine). I nutrienti sono massimamente disponibili.
- **pH > 7.0 (Alcalino):** Le piante come asparagi e olive tollerano suoli alcalini. Aggiungi zolfo o torba per abbassare il pH.

**Esempio Pratico - Pomodori:**
- pH ottimale: 6.2-6.8
- Se pH = 5.5: aggiungere 50g/m² di calce dolomitica
- Se pH = 7.5: aggiungere 30g/m² di zolfo

**English:**

Soil pH measures acidity or alkalinity on a scale from 0 to 14:

- **pH < 6.0 (Acidic):** Plants like strawberries, potatoes, and blueberries thrive in acidic soils. Add calcium sulfate (gypsum) to raise pH.
- **pH 6.0-7.0 (Neutral):** Ideal range for most vegetables (tomatoes, lettuce, zucchini). Nutrients are maximally available.
- **pH > 7.0 (Alkaline):** Plants like asparagus and olives tolerate alkaline soils. Add sulfur or peat moss to lower pH.

**Practical Example - Tomatoes:**
- Optimal pH: 6.2-6.8
- If pH = 5.5: add 50g/m² of dolomitic lime
- If pH = 7.5: add 30g/m² of sulfur

### 3.3 EC: I Nutrienti del Suolo / EC: Soil Nutrients

**Italiano:**

La conducibilità elettrica (EC) misura la concentrazione di sali e nutrienti disciolti nella soluzione del suolo:

| EC (mS/cm) | Livello / Level | Azione Consigliata / Recommended Action |
|------------|-----------------|----------------------------------------|
| < 0.5 | Molto Basso / Very Low | Aggiungere fertilizzante bilanciato |
| 0.5 - 1.5 | Ottimale / Optimal | Nessun intervento necessario / No action needed |
| 1.5 - 2.5 | Accettabile / Acceptable | Monitorare, ridurre fertilizzanti |
| 2.5 - 3.5 | Alto / High | Lavare il suolo con acqua pulita / Flush with clean water |
| > 3.5 | Tossico / Toxic | Sospendere fertilizzazione, aumentare irrigazione |

**Tabella di Riferimento per Colture Comuni / Reference Table for Common Crops:**

| Coltura / Crop | EC Ottimale / Optimal EC | Note |
|----------------|---------------------------|------|
| Pomodori / Tomatoes | 2.0 - 3.5 mS/cm | Aumentare EC durante la fruttificazione / Increase EC during fruiting |
| Lattuga / Lettuce | 1.0 - 1.5 mS/cm | EC troppo alto causa bruciature fogliari / High EC causes leaf burn |
| Patate / Potatoes | 1.5 - 2.5 mS/cm | Ridurre EC alla fine del ciclo / Reduce EC at end of cycle |
| Fragole / Strawberries | 1.0 - 1.8 mS/cm | EC basso favorisce zuccheri / Low EC favors sugars |

**English:**

Electrical conductivity (EC) measures the concentration of dissolved salts and nutrients in the soil solution:

| EC (mS/cm) | Level | Recommended Action |
|------------|-------|-------------------|
| < 0.5 | Very Low | Add balanced fertilizer |
| 0.5 - 1.5 | Optimal | No action needed |
| 1.5 - 2.5 | Acceptable | Monitor, reduce fertilizers |
| 2.5 - 3.5 | High | Flush soil with clean water |
| > 3.5 | Toxic | Stop fertilization, increase irrigation |

### 3.4 Esempio Completo: Giornata Tipo per Pomodori / Full Example: Typical Day for Tomatoes

**Italiano:**

```
Data: 15 Luglio 2026
Ort: Orto di Marco - Fila A

08:00 - Lettura Sensori (automatica):
  - pH: 6.4 ✓ (ottimale)
  - EC: 2.2 mS/cm ✓ (ottimale)
  - Temperatura: 22°C ✓
  - Umidità: 55% ⚠ (leggera sotto il range)

10:30 - Alert Sistema:
  "Umidità suolo sotto il 40% - Attivare irrigazione"

12:00 - Intervento Manuale:
  - Irrigazione: 15 litri/m²
  - Concimazione: sospesa (EC già ottimale)

14:00 - Nuova Lettura:
  - Umidità: 68% ✓
  - Altri parametri invariati

Settimana Prossima:
  - Controllare pH ogni 3 giorni
  - Prevedere aumento EC a 2.5 per fase di fruttificazione
```

**English:**

```
Date: July 15, 2026
Garden: Marco's Garden - Row A

08:00 - Sensor Reading (automatic):
  - pH: 6.4 ✓ (optimal)
  - EC: 2.2 mS/cm ✓ (optimal)
  - Temperature: 22°C ✓
  - Moisture: 55% ⚠ (slightly below range)

10:30 - System Alert:
  "Soil moisture below 40% - Activate irrigation"

12:00 - Manual Intervention:
  - Irrigation: 15 liters/m²
  - Fertilization: suspended (EC already optimal)

14:00 - New Reading:
  - Moisture: 68% ✓
  - Other parameters unchanged

Next Week:
  - Check pH every 3 days
  - Plan EC increase to 2.5 for fruiting phase
```

---

## 4. Manutenzione e Calibrazione / Maintenance and Calibration

### 4.1 Calibrazione dei Sensori / Sensor Calibration

#### Sensore pH / pH Sensor

**Italiano:**

**Frequenza:** Ogni 30 giorni o dopo ogni sostituzione elettrodo  
**Soluzioni di Calibrazione:**
- pH 4.00 (per terreni acidi)
- pH 6.86 (per terreni neutri)
- pH 9.18 (per terreni alcalini)

**Procedura:**
1. Sciacquare l'elettrodo con acqua distillata
2. Immergere in soluzione pH 6.86 per 2-3 minuti
3. Regolare il potenziometro di calibrazione finché il valore non corrisponde
4. Ripetere con pH 4.00 e pH 9.18 per calibrazione a 2 o 3 punti
5. Asciugare delicatamente con carta assorbente

**English:**

**Frequency:** Every 30 days or after electrode replacement  
**Calibration Solutions:**
- pH 4.00 (for acidic soils)
- pH 6.86 (for neutral soils)
- pH 9.18 (for alkaline soils)

**Procedure:**
1. Rinse the electrode with distilled water
2. Immerse in pH 6.86 solution for 2-3 minutes
3. Adjust the calibration potentiometer until the value matches
4. Repeat with pH 4.00 and pH 9.18 for 2 or 3-point calibration
5. Gently dry with absorbent paper

#### Sensore EC / EC Sensor

**Italiano:**

**Frequenza:** Ogni 60 giorni  
**Soluzioni di Calibrazione:**
- 1.413 mS/cm (standard basso)
- 12.88 mS/cm (standard alto)

**Procedura:**
1. Sciacquare la sonda con acqua distillata
2. Immergere in soluzione 1.413 mS/cm
3. Regolare il trimmer di calibrazione
4. Verificare con soluzione 12.88 mS/cm
5. Se la deviazione è > 5%, sostituire la sonda

**English:**

**Frequency:** Every 60 days  
**Calibration Solutions:**
- 1.413 mS/cm (low standard)
- 12.88 mS/cm (high standard)

**Procedure:**
1. Rinse the probe with distilled water
2. Immerse in 1.413 mS/cm solution
3. Adjust the calibration trimmer
4. Verify with 12.88 mS/cm solution
5. If deviation is > 5%, replace the probe

### 4.2 Piano di Manutenzione / Maintenance Schedule

| Intervento / Task | Frequenza / Frequency | Note |
|-------------------|------------------------|------|
| **Pulizia Sensori** / Sensor Cleaning | Settimanale / Weekly | Rimuovere residui di terra e vegetazione |
| **Controllo Cablaggi** / Wiring Check | Mensile / Monthly | Verificare connessioni e impermeabilizzazione |
| **Calibrazione pH** / pH Calibration | Mensile / Monthly | Con soluzioni standard a 2 punti |
| **Calibrazione EC** / EC Calibration | Bimestrale / Bi-monthly | Con soluzioni standard 1.413 e 12.88 mS/cm |
| **Aggiornamento Firmware** / Firmware Update | Trimestrale / Quarterly | Controllare GitHub per nuove release |
| **Sostituzione Elettrodi** / Electrode Replacement | Annuale / Annual | pH: €15-25; EC: €10-18 |
| **Controllo Batteria** / Battery Check | Mensile / Monthly | Per sistemi a batteria/solare |

### 4.3 Conservazione delle Soluzioni di Calibrazione / Calibration Solution Storage

**Italiano:**
- Conservare in bottiglie di plastica scure (preferibilmente ambra)
- Temperatura ambiente (15-25°C), evitare luce diretta
- Controllare la data di scadenza (solitamente 6-12 mesi)
- Non riutilizzare soluzioni già usate
- Etichettare chiaramente concentrazione e data di preparazione

**English:**
- Store in dark plastic bottles (preferably amber)
- Room temperature (15-25°C), avoid direct light
- Check expiration date (usually 6-12 months)
- Do not reuse previously used solutions
- Clearly label concentration and preparation date

---

## 5. Risoluzione dei Problemi / Troubleshooting

### 5.1 Problemi Comuni e Soluzioni / Common Issues and Solutions

| Problema / Problem | Possibile Causa / Possible Cause | Soluzione / Solution |
|-------------------|----------------------------------|----------------------|
| **Lettura pH instabile** / Unstable pH reading | Elettrodo contaminato o vecchio | Pulire con soluzione di pulizia HCl 0.1M, ricalibrare |
| **Valori EC sempre bassi** / Always low EC values | Cattiva connessione sonda | Controllare cavi, verificare alimentazione sonda |
| **Disconnessioni WiFi** / WiFi disconnections | Segnale debole | Aggiungere ripetitore WiFi o antenna esterna |
| **Dati non sincronizzati** / Data not syncing | Gateway offline | Verificare logs PM2, riavviare servizio |
| **Batteria scarica velocemente** / Battery draining fast | Pannello solare ombreggiato | Riposizionare pannello, pulire superficie |
| **Alert eccessivi** / Excessive alerts | Soglie troppo basse | Modificare soglie nella dashboard |

### 5.2 Codici di Errore / Error Codes

| Codice / Code | Descrizione / Description | Azione / Action |
|---------------|---------------------------|-----------------|
| `ERR_PH_CALIBRATION` | Calibrazione pH fallita | Verificare soluzioni, sostituire elettrodo |
| `ERR_EC_OVERFLOW` | EC sopra il range massimo | Verificare collegamenti, controllare suolo |
| `ERR_WIFI_TIMEOUT` | Timeout connessione WiFi | Controllare credenziali, riavviare ESP32 |
| `ERR_GATEWAY_500` | Errore server gateway | Controllare logs, riavviare servizio Node.js |
| `ERR_SENSOR_FAULT` | Guasto sensore | Sostituire componente, verificare alimentazione |
| `ERR_LOW_BATTERY` | Batteria sotto il 20% | Caricare batteria, controllare pannello solare |

### 5.3 Checklist per il Supporto / Support Checklist

**Italiano:**

Prima di contattare il supporto tecnico, raccogliere:
1. **ID Dispositivo:** Trovato nella dashboard sotto "Impostazioni > Dispositivi"
2. **Log Recenti:** Scaricare dalla sezione "Diagnostica"
3. **Foto del Setup:** Includere foto dell'hardware installato
4. **Condizioni Ambientali:** Note su pioggia, temperatura estrema, ecc.
5. **Azioni Già Tentate:** Lista delle operazioni di troubleshooting già effettuate

**Canali di Supporto:**
- GitHub Issues: https://github.com/MyZubster-Ecosystem/myzubster-docs/issues
- Email: support@myzubster.com
- Telegram: @MyZubster_bot

**English:**

Before contacting technical support, gather:
1. **Device ID:** Found in the dashboard under "Settings > Devices"
2. **Recent Logs:** Download from the "Diagnostics" section
3. **Setup Photos:** Include photos of installed hardware
4. **Environmental Conditions:** Notes on rain, extreme temperature, etc.
5. **Actions Already Attempted:** List of troubleshooting operations already performed

**Support Channels:**
- GitHub Issues: https://github.com/MyZubster-Ecosystem/myzubster-docs/issues
- Email: support@myzubster.com
- Telegram: @MyZubster_bot

### 5.4 Risorse Aggiuntive / Additional Resources

| Risorsa / Resource | Link / URL | Descrizione / Description |
|-------------------|------------|---------------------------|
| **Repository GitHub** | github.com/MyZubster-Ecosystem | Codice sorgente, firmware, issues |
| **Wiki della Community** | github.com/MyZubster-Ecosystem/wiki | Tutorial, FAQ, progetti condivisi |
| **Forum di Discussione** | github.com/MyZubster-Ecosystem/discussions | Domande, idee, collaborazioni |
| **Video Tutorial** | YouTube/@MyZubster | Guide video per principianti |
| **Documentazione API** | docs.myzubster.com | Riferimento tecnico per sviluppatori |

---

## Appendice A: Schede di Lavoro per l'Utente / Appendix A: User Worksheets

### Settimanale / Weekly

| Giorno / Day | pH | EC (mS/cm) | Temp (°C) | Umidità (%) | Note / Notes |
|--------------|----|------------|-----------|-------------|--------------|
| Lunedì / Monday | | | | | |
| Mercoledì / Wednesday | | | | | |
| Venerdì / Friday | | | | | |
| Domenica / Sunday | | | | | |

### Mensile / Monthly

| Data / Date | Intervento Effettuato / Performed Action | Materiali Utilizzati / Materials Used | Costo / Cost | Note / Notes |
|-------------|------------------------------------------|--------------------------------------|--------------|--------------|
| | | | | |
| | | | | |
| | | | | |

---

## Appendice B: Codici di Risposta HTTP / Appendix B: HTTP Response Codes

| Codice / Code | Significato / Meaning | Azione Consigliata / Recommended Action |
|---------------|----------------------|----------------------------------------|
| 200 | Dati salvati con successo | Nessuna / None |
| 400 | Payload malformato | Verificare formato JSON |
| 401 | Token non valido | Rigenerare API key |
| 413 | Payload troppo grande | Comprimere dati o aumentare limite |
| 500 | Errore interno server | Contattare supporto tecnico |
| 503 | Gateway non disponibile | Attendere e riprovare |

---

## Appendice C: Riferimenti Incrociati / Appendix C: Cross-References

| Documento / Document | Riferimento / Reference |
|----------------------|-------------------------|
| `AI_CONTRACT.md` | Contratto AI per analisi dati sensore |
| `BOT_CONTRACT.md` | Automazione notifiche via Telegram |
| `legal/TERMS_OF_SERVICE.md` | Termini di servizio della piattaforma |
| `legal/GDPR_COMPLIANCE_CHECKLIST.md` | Conformità trattamento dati |
| `README.md` | Panoramica progetto e architettura |

---

**📝 Note sulla Versione / Version Notes:**  
Questa è la versione 1.0 della guida pratica. Per suggerimenti o correzioni, aprire una issue su GitHub o contattare il team di documentazione.

**📝 Version Notes:**  
This is version 1.0 of the practical guide. For suggestions or corrections, open an issue on GitHub or contact the documentation team.
