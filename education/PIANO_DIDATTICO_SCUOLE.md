# Piano Didattico per le Scuole / School Teaching Plan — MyZubster Orto Intelligente

**Versione / Version:** 1.0.0  **Data / Date:** 2026-07-31
**Progetto / Project:** MyZubster Ecosystem  **Pubblico / Audience:** Studenti 11-18 anni / Students aged 11-18
**Riferimento / Reference:** Issue #13 — [EDUCATION] Piano didattico scolastico / School teaching plan
**Durata / Duration:** 5 lezioni / 5 lessons (45-60 min ciascuna / each)

---

## Indice / Table of Contents
1. [Introduzione / Introduction](#1-introduzione--introduction)
2. [Panoramica del Corso / Course Overview](#2-panoramica-del-corso--course-overview)
3. [Allineamento STEM / STEM Alignment](#3-allineamento-stem--stem-alignment)
4. [Lezione 1: Introduzione all'Agricoltura Intelligente / Introduction to Smart Farming](#4-lezione-1-introduzione-allagricoltura-intelligente--introduction-to-smart-farming)
5. [Lezione 2: I Sensori (pH, EC, Temperatura) / Sensors (pH, EC, Temperature)](#5-lezione-2-i-sensori-ph-ec-temperatura--sensors-ph-ec-temperature)
6. [Lezione 3: Costruiamo il Primo Sensore / Building the First Sensor](#6-lezione-3-costruiamo-il-primo-sensore--building-the-first-sensor)
7. [Lezione 4: Raccolta e Interpretazione dei Dati / Collecting and Interpreting Data](#7-lezione-4-raccolta-e-interpretazione-dei-dati--collecting-and-interpreting-data)
8. [Lezione 5: Il Futuro del Cibo: IoT e Sostenibilità / The Future of Food: IoT and Sustainability](#8-lezione-5-il-futuro-del-cibo-iot-e-sostenibilità--the-future-of-food-iot-and-sustainability)
9. [Valutazione / Assessment](#9-valutazione--assessment)
10. [Risorse e Collegamenti / Resources and Links](#10-risorse-e-collegamenti--resources-and-links)

---

## 1. Introduzione / Introduction
**Italiano:** Questo piano introduce studenti di 11-18 anni all'agricoltura intelligente con MyZubster, ecosistema open-source che combina hardware Arduino/ESP32, sensori IoT (pH, EC, temperatura, umidità) e piattaforma cloud. In cinque lezioni pratiche si costruiscono sensori, si raccolgono dati reali dal suolo e si riflette sul futuro del cibo e della sostenibilità. Nessuna conoscenza preliminare è richiesta.
**English:** This plan introduces students aged 11-18 to smart agriculture with MyZubster, an open-source ecosystem combining Arduino/ESP32 hardware, IoT sensors (pH, EC, temperature, humidity) and a cloud platform. Across five hands-on lessons students build sensors, collect real soil data and reflect on the future of food and sustainability. No prior knowledge is required.

### 1.1 Filosofia Educativa / Educational Philosophy
**Italiano:** Il corso segue il principio "imparare facendo": ogni concetto teorico è collegato a un'attività pratica, con ruoli diversi per studenti di abilità diverse (costruttore, programmatore, data analyst, presentatore), favorendo lavoro di squadra e apprendimento cooperativo.
**English:** The course follows the "learning by doing" principle: every concept is linked to a hands-on activity, with different roles for students of different abilities (builder, programmer, data analyst, presenter), fostering teamwork and cooperative learning.

### 1.2 Sicurezza e Norme / Safety and Rules
| Regola / Rule | Descrizione / Description |
|---------------|---------------------------|
| **Elettricità / Electricity** | Usare solo alimentazione USB 5V; mai collegare sensori a prese di rete / Use only 5V USB power; never connect sensors to mains outlets |
| **Sonde pH/EC / pH/EC probes** | Sonde di vetro: maneggiare con cura, mai toccare l'elettrodo / Glass probes: handle with care, never touch the electrode |
| **Acqua / Water** | Mani asciutte prima dei circuiti; liquidi lontani dalle breadboard / Dry hands before circuits; keep liquids away from breadboards |
| **Supervisione / Supervision** | Un insegnante supervisiona sempre le attività pratiche / A teacher always supervises hands-on activities |

---

## 2. Panoramica del Corso / Course Overview
| # | Titolo Lezione / Lesson Title | Durata / Duration | Attività principale / Main activity |
|---|-------------------------------|-------------------|--------------------------------------|
| 1 | Introduzione all'Agricoltura Intelligente / Introduction to Smart Farming | 45-60 min | Brainstorming + mappa concettuale / Brainstorming + concept map |
| 2 | I Sensori: pH, EC, Temperatura / Sensors: pH, EC, Temperature | 45-60 min | Esperimenti con liquidi reali / Experiments with real liquids |
| 3 | Costruiamo il Primo Sensore / Building the First Sensor | 45-60 min | Assemblaggio ESP32 + sensore umidità / ESP32 + moisture sensor assembly |
| 4 | Raccolta e Interpretazione dei Dati / Collecting and Interpreting Data | 45-60 min | Registrazione dati e grafici / Data logging and charting |
| 5 | Il Futuro del Cibo: IoT e Sostenibilità / The Future of Food: IoT and Sustainability | 45-60 min | Progetto finale + dibattito / Final project + debate |

---

## 3. Allineamento STEM / STEM Alignment
**Italiano:** Il corso si allinea alle discipline STEM (Scienze, Tecnologia, Ingegneria, Matematica) e può essere integrato in diversi programmi curricolari.
**English:** The course aligns with STEM subjects (Science, Technology, Engineering, Mathematics) and can be integrated into different curricula:

| Disciplina STEM / STEM Subject | Contenuto del corso / Course content |
|--------------------------------|--------------------------------------|
| **Scienze / Science** | Chimica del suolo (pH, nutrienti/EC), biologia delle piante, ciclo dell'acqua / Soil chemistry (pH, nutrients/EC), plant biology, water cycle |
| **Tecnologia / Technology** | Sistemi IoT, sensori, cloud computing, dashboard dati / IoT systems, sensors, cloud computing, data dashboards |
| **Ingegneria / Engineering** | Montaggio circuiti, troubleshooting hardware, progettazione / Circuit assembly, hardware troubleshooting, design |
| **Matematica / Mathematics** | Medie, minimo/massimo, grafici, serie temporali / Averages, min/max, charts, time-series interpretation |
| **Informatica / Computer Science** | Programmazione base, logica, lettura di codice (opzionale: Arduino IDE) / Basic programming, logic, code reading (optional: Arduino IDE) |
| **Competenze trasversali / Soft skills** | Lavoro di gruppo, comunicazione, pensiero critico, cittadinanza digitale / Teamwork, communication, critical thinking, digital citizenship |

### 3.1 Competenze Chiave Europee / European Key Competences
**Italiano:** Il piano supporta le 8 competenze chiave europee, in particolare: competenza matematica e in scienze/tecnologia; competenza digitale; competenza sociale e civica; imparare a imparare.
**English:** The plan supports the 8 European key competences, especially: mathematical and science/technology competence; digital competence; social and civic competence; learning to learn.

---

## 4. Lezione 1: Introduzione all'Agricoltura Intelligente / Introduction to Smart Farming
**Italiano:** Gli studenti scoprono cos'è l'agricoltura intelligente e perché è importante, con MyZubster come esempio concreto di ecosistema open-source per il monitoraggio delle colture.
**English:** Students discover what smart farming is and why it matters, with MyZubster as a concrete example of an open-source ecosystem for crop monitoring.

### 4.1 Obiettivi di Apprendimento / Learning Objectives
| Obiettivo / Objective | Livello / Level |
|------------------------|-----------------|
| Definire l'agricoltura intelligente e i suoi vantaggi / Define smart farming and its benefits | Conoscenza / Knowledge |
| Identificare i componenti di un sistema IoT (sensori, gateway, cloud, dashboard) / Identify components of an IoT system (sensors, gateway, cloud, dashboard) | Comprensione / Comprehension |
| Spiegare perché i dati aiutano a risparmiare acqua e risorse / Explain why data helps save water and resources | Comprensione / Comprehension |
| Discutere criticamente le sfide alimentari globali / Critically discuss global food challenges | Analisi / Analysis |

### 4.2 Materiali Necessari / Required Materials
| Materiale / Material | Quantità / Quantity |
|----------------------|---------------------|
| Lavagna interattiva o proiettore / Interactive whiteboard or projector | 1 per classe / per class |
| Immagini/video di fattorie intelligenti / Smart farm images/videos | 5-10 |
| Poster o strumenti digitali per mappe concettuali / Posters or digital tools for concept maps | 1 per gruppo / per group |
| Kit dimostrativo MyZubster (ESP32 + sensori) / MyZubster demo kit (ESP32 + sensors) | 1 |
| Scheda di lavoro 1 (stampabile) / Worksheet 1 (printable) | 1 per studente / per student |

### 4.3 Attività e Fasi / Activity Steps
| Fase / Step | Durata / Duration | Attività / Activity |
|-------------|-------------------|---------------------|
| 1. Apertura / Opening | 5 min | Domanda stimolo: "Da dove viene il nostro cibo?" / Trigger question: "Where does our food come from?" |
| 2. Brainstorming / Brainstorming | 10 min | Elencare problemi dell'agricoltura tradizionale / List problems of traditional farming |
| 3. Presentazione / Presentation | 15 min | L'insegnante presenta MyZubster e i componenti IoT / Teacher presents MyZubster and IoT components |
| 4. Attività di gruppo / Group activity | 15 min | Mappa concettuale "dal campo al cloud" / Concept map "from field to cloud" |
| 5. Condivisione / Sharing | 5 min | Ogni gruppo presenta la propria mappa / Each group presents its map |
| 6. Chiusura / Wrap-up | 5 min | Domande di verifica e compito a casa / Review questions and homework |

### 4.4 Punti Dimostrativi per l'Insegnante / Teacher Demo Points (IT/EN)
- Mostrare dal vivo il kit MyZubster collegato al sensore: dati sulla dashboard cloud / Show the MyZubster kit live with the sensor: data on the cloud dashboard
- Evidenziare il percorso: sensore → ESP32 → gateway → cloud → grafico / Highlight the path: sensor → ESP32 → gateway → cloud → chart
- Chiedere di prevedere cosa succede se il suolo è troppo secco o troppo bagnato / Ask students to predict what happens if soil is too dry or too wet

### 4.5 Scheda di Lavoro 1 (Stampabile) / Worksheet 1 (Printable)
**Italiano:** Nome: ____  Data: ____
1. Scrivi 3 problemi dell'agricoltura tradizionale: (a) ______ (b) ______ (c) ______
2. Collega con frecce: Sensore → ____ → ____ → ____ → Grafico
3. Un sistema IoT è composto da: ______, ______, ______, ______
4. Perché l'agricoltura intelligente può risparmiare acqua? 2 motivi: ______
5. Disegna la tua fattoria del futuro ed etichetta i sensori.
**English:** Name: ____  Date: ____
1. Write 3 problems of traditional farming: (a) ______ (b) ______ (c) ______
2. Connect with arrows: Sensor → ____ → ____ → ____ → Chart
3. An IoT system is made of: ______, ______, ______, ______
4. Why can smart farming save water? 2 reasons: ______
5. Draw your farm of the future and label the sensors.

---

## 5. Lezione 2: I Sensori (pH, EC, Temperatura) / Sensors (pH, EC, Temperature)
**Italiano:** Gli studenti esplorano i tre sensori chiave di MyZubster e conducono esperimenti con liquidi reali (acqua, succo di limone, acqua fertilizzata, bicarbonato) misurando pH ed EC.
**English:** Students explore MyZubster's three key sensors and run experiments with real liquids (water, lemon juice, fertilized water, baking soda) measuring pH and EC.

### 5.1 Obiettivi di Apprendimento / Learning Objectives
| Obiettivo / Objective | Livello / Level |
|------------------------|-----------------|
| Spiegare cosa misura il pH e la scala 0-14 / Explain what pH measures and the 0-14 scale | Conoscenza / Knowledge |
| Spiegare cosa misura l'EC e perché indica i nutrienti / Explain what EC measures and why it indicates nutrients | Comprensione / Comprehension |
| Eseguire misure con sonde pH/EC su campioni reali / Take pH/EC measurements on real samples | Applicazione / Application |
| Confrontare e classificare i campioni in base ai dati / Compare and classify samples based on data | Analisi / Analysis |

### 5.2 Materiali Necessari / Required Materials
| Materiale / Material | Quantità / Quantity |
|----------------------|---------------------|
| Sensore pH + sonda BNC / pH sensor + BNC probe | 2-3 |
| Sensore EC + sonda K1.0 / EC sensor + K1.0 probe | 2-3 |
| Sensore temperatura DS18B20 / DS18B20 temperature sensor | 2-3 |
| Becher o bicchieri trasparenti / Beakers or transparent cups | 8-10 |
| Campioni: acqua, limone, acqua fertilizzata, bicarbonato / Samples: water, lemon, fertilized water, baking soda | 1 set per gruppo / per group |
| Acqua distillata per risciacquo / Distilled water for rinsing | 1 litro / liter |
| Guanti e occhiali di sicurezza / Gloves and safety goggles | 1 per studente / per student |
| Scheda di lavoro 2 (stampabile) / Worksheet 2 (printable) | 1 per gruppo / per group |

### 5.3 Attività e Fasi / Activity Steps
| Fase / Step | Durata / Duration | Attività / Activity |
|-------------|-------------------|---------------------|
| 1. Introduzione / Introduction | 10 min | Spiegazione della scala pH e del concetto di EC / Explanation of pH scale and EC concept |
| 2. Dimostrazione / Demo | 10 min | L'insegnante misura il pH del primo campione / Teacher measures pH of first sample |
| 3. Esperimento / Experiment | 20 min | Ogni gruppo misura pH, EC e temperatura dei 4 campioni / Each group measures pH, EC, temperature of 4 samples |
| 4. Registrazione / Recording | 10 min | Compilazione della tabella dati / Completing the data table |
| 5. Discussione / Discussion | 10 min | Confronto dei risultati tra gruppi / Comparing results across groups |

### 5.4 Punti Dimostrativi per l'Insegnante / Teacher Demo Points (IT/EN)
- Calibrare il sensore pH con soluzioni tampone (4.0 e 7.0) spiegando perché serve / Calibrate the pH sensor with buffer solutions (4.0 and 7.0) explaining why it is needed
- Mostrare la differenza di EC tra acqua distillata (basso) e fertilizzata (alto) / Show the EC difference between distilled (low) and fertilized water (high)
- Evidenziare che la temperatura influisce sulle misure: i sensori compensano / Highlight that temperature affects readings: sensors compensate

### 5.5 Scheda di Lavoro 2 (Stampabile) / Worksheet 2 (Printable)
**Italiano:** Gruppo: ____  Data: ____ — Tabella dati (compila per ogni campione):
| Campione / Sample | pH | EC (mS/cm) | Temp (°C) | Acido/Base/Neutro? / Acid/Base/Neutral? |
|-------------------|----|------------|-----------|------------------------------------------|
| Acqua / Water | | | | |
| Succo di limone / Lemon juice | | | | |
| Acqua fertilizzata / Fertilized water | | | | |
| Bicarbonato / Baking soda | | | | |
1. Quale campione è il più acido? ______  Il più alcalino? ______
2. Perché l'acqua fertilizzata ha un EC più alto? ______
3. Quale pH è migliore per le piante? (Cerca: la maggior parte ama pH 6-7) ______
**English:** Group: ____  Date: ____ — Data table (fill in for each sample):
| Sample | pH | EC (mS/cm) | Temp (°C) | Acid/Base/Neutral? |
|--------|----|------------|-----------|--------------------|
| Water | | | | |
| Lemon juice | | | | |
| Fertilized water | | | | |
| Baking soda | | | | |
1. Which sample is the most acidic? ______  The most alkaline? ______
2. Why does fertilized water have a higher EC? ______
3. Which pH is best for plants? (Research: most plants like pH 6-7) ______

---

## 6. Lezione 3: Costruiamo il Primo Sensore / Building the First Sensor
**Italiano:** Lezione pratica: ogni gruppo assembla un circuito ESP32 con sensore di umidità del suolo (capacitivo), lo collega e osserva i dati in tempo reale. È il cuore pratico del corso.
**English:** A hands-on lesson: each group assembles an ESP32 circuit with a capacitive soil moisture sensor, connects it and observes real-time data. It is the practical heart of the course.

### 6.1 Obiettivi di Apprendimento / Learning Objectives
| Obiettivo / Objective | Livello / Level |
|------------------------|-----------------|
| Identificare i componenti del circuito (ESP32, breadboard, cavi, sensore) / Identify circuit components (ESP32, breadboard, wires, sensor) | Conoscenza / Knowledge |
| Montare un circuito funzionante seguendo uno schema / Assemble a working circuit following a diagram | Applicazione / Application |
| Collegare il sensore e avviare la lettura dati / Connect the sensor and start data reading | Applicazione / Application |
| Risolvere problemi base di collegamento / Troubleshoot basic connection issues | Analisi / Analysis |

### 6.2 Materiali Necessari / Required Materials
| Materiale / Material | Quantità / Quantity |
|----------------------|---------------------|
| ESP32 DevKit V1 / ESP32 DevKit V1 | 1 per gruppo / per group |
| Sensore umidità capacitivo / Capacitive moisture sensor | 1 per gruppo / per group |
| Breadboard e cavi jumper / Breadboard and jumper wires | 1 set per gruppo / per group |
| Cavo USB + power bank / USB cable + power bank | 1 per gruppo / per group |
| Vaso con terreno umido e vaso con terreno asciutto / Pot with wet soil and pot with dry soil | 2 per gruppo / per group |
| Schema di montaggio stampato / Printed wiring diagram | 1 per gruppo / per group |
| Scheda di lavoro 3 (stampabile) / Worksheet 3 (printable) | 1 per gruppo / per group |

### 6.3 Attività e Fasi / Activity Steps
| Fase / Step | Durata / Duration | Attività / Activity |
|-------------|-------------------|---------------------|
| 1. Richiamo / Recap | 5 min | Ripasso del percorso sensore → cloud / Review of sensor → cloud path |
| 2. Spiegazione schema / Diagram explanation | 10 min | L'insegnante spiega lo schema di montaggio / Teacher explains the wiring diagram |
| 3. Montaggio / Assembly | 20 min | Ogni gruppo monta il circuito e collega il sensore / Each group assembles the circuit and connects the sensor |
| 4. Test / Testing | 10 min | Sensore nel terreno umido e asciutto, osservare i valori / Sensor in wet and dry soil, observe values |
| 5. Verifica / Check | 5 min | Ogni gruppo mostra i dati raccolti / Each group shows collected data |
| 6. Pulizia / Cleanup | 5 min | Smontaggio e riordino / Disassembly and tidy-up |

### 6.4 Punti Dimostrativi per l'Insegnante / Teacher Demo Points (IT/EN)
- Mostrare il corretto orientamento del sensore capacitivo (mai i pin verso il terreno) / Show correct capacitive sensor orientation (never pins facing the soil)
- Terreno asciutto: valore alto (es. 3500+); terreno umido: valore basso (es. <1500). Spiegare la scala relativa / Dry soil: high value (e.g. 3500+); wet soil: low value (e.g. <1500). Explain the relative scale
- Differenza tra sensore capacitivo (non corrosivo) e resistivo (si corrode) / Difference between capacitive (non-corrosive) and resistive (corroding) sensors

### 6.5 Scheda di Lavoro 3 (Stampabile) / Worksheet 3 (Printable)
**Italiano:** Gruppo: ____  Data: ____ — Schema di montaggio (colora i collegamenti):
ESP32 Pin: 3V3 → ______  GND → ______  GPIO 34 (VP) → ______
1. Disegna il tuo circuito nello spazio sottostante:
2. Valore nel terreno asciutto: ______  Nel terreno umido: ______
3. Quale valore è più alto? Perché? ______
4. Un problema incontrato e come lo abbiamo risolto: ______
**English:** Group: ____  Date: ____ — Wiring diagram (color the connections):
ESP32 Pins: 3V3 → ______  GND → ______  GPIO 34 (VP) → ______
1. Draw your circuit in the space below:
2. Value in dry soil: ______  In wet soil: ______
3. Which value is higher? Why? ______
4. A problem we encountered and how we solved it: ______

---

## 7. Lezione 4: Raccolta e Interpretazione dei Dati / Collecting and Interpreting Data
**Italiano:** Gli studenti raccolgono dati dal sensore, li registrano e li interpretano: calcolano medie, minimi e massimi, disegnano grafici e traggono conclusioni sullo stato delle piante.
**English:** Students collect sensor data, record and interpret it: they calculate averages, minimums and maximums, draw charts and draw conclusions about plant health.

### 7.1 Obiettivi di Apprendimento / Learning Objectives
| Obiettivo / Objective | Livello / Level |
|------------------------|-----------------|
| Registrare dati in modo sistematico in una tabella / Record data systematically in a table | Applicazione / Application |
| Calcolare media, minimo e massimo di un insieme di dati / Calculate average, minimum and maximum of a data set | Applicazione / Application |
| Disegnare un grafico a linee dei dati nel tempo / Draw a line chart of data over time | Applicazione / Application |
| Interpretare i dati per decidere quando innaffiare / Interpret data to decide when to water | Valutazione / Evaluation |

### 7.2 Materiali Necessari / Required Materials
| Materiale / Material | Quantità / Quantity |
|----------------------|---------------------|
| Kit ESP32 + sensore montato in Lezione 3 / ESP32 + sensor kit built in Lesson 3 | 1 per gruppo / per group |
| Vaso con piantina reale (basilico o lattuga) / Pot with real seedling (basil or lettuce) | 1 per gruppo / per group |
| Cronometro / Timer | 1 per gruppo / per group |
| Carta millimetrata o laptop con foglio di calcolo / Graph paper or laptop with spreadsheet | 1 per gruppo / per group |
| Righello e matite colorate / Ruler and colored pencils | 1 set per gruppo / per group |
| Scheda di lavoro 4 (stampabile) / Worksheet 4 (printable) | 1 per gruppo / per group |

### 7.3 Attività e Fasi / Activity Steps
| Fase / Step | Durata / Duration | Attività / Activity |
|-------------|-------------------|---------------------|
| 1. Preparazione / Preparation | 10 min | Posizionare il sensore nel vaso della piantina / Place sensor in the seedling pot |
| 2. Raccolta / Collection | 20 min | Una lettura ogni 3 minuti (6-7 letture) / A reading every 3 minutes (6-7 readings) |
| 3. Elaborazione / Processing | 15 min | Calcolare media, min, max e disegnare il grafico / Calculate average, min, max and draw the chart |
| 4. Interpretazione / Interpretation | 10 min | Rispondere: "Quando innaffieresti la pianta?" / Answer: "When would you water the plant?" |
| 5. Confronto / Comparison | 5 min | Confrontare i grafici tra gruppi / Compare charts across groups |

### 7.4 Punti Dimostrativi per l'Insegnante / Teacher Demo Points (IT/EN)
- Mostrare la dashboard cloud MyZubster e i grafici storici / Show the MyZubster cloud dashboard and historical charts
- Differenza tra dato grezzo e informazione: un valore è un dato, una tendenza è informazione / Difference between raw data and information: a value is data, a trend is information
- Collegare i valori alla decisione: "umidità < 30% → la pianta ha sete" / Connect values to a decision: "moisture < 30% → the plant is thirsty"

### 7.5 Scheda di Lavoro 4 (Stampabile) / Worksheet 4 (Printable)
**Italiano:** Gruppo: ____  Data: ____
| Tempo (min) / Time (min) | 0 | 3 | 6 | 9 | 12 | 15 | 18 |
|--------------------------|---|---|---|---|----|----|----|
| Umidità (valore grezzo) / Moisture (raw) | | | | | | | |
1. Media: ______  Minimo: ______  Massimo: ______
2. Disegna il grafico a linee qui sotto:
3. Secondo i dati, la pianta ha bisogno di acqua? Perché? ______
4. Quale valore di umidità useresti come soglia per innaffiare automaticamente? ______
**English:** Group: ____  Date: ____
| Time (min) | 0 | 3 | 6 | 9 | 12 | 15 | 18 |
|------------|---|---|---|---|----|----|----|
| Moisture (raw) | | | | | | | |
1. Average: ______  Minimum: ______  Maximum: ______
2. Draw the line chart below:
3. According to the data, does the plant need water? Why? ______
4. Which moisture value would you use as a threshold for automatic watering? ______

---

## 8. Lezione 5: Il Futuro del Cibo: IoT e Sostenibilità / The Future of Food: IoT and Sustainability
**Italiano:** Lezione conclusiva: gli studenti collegano ciò che hanno imparato alle grandi sfide globali (cambiamento climatico, spreco alimentare, crescita demografica) e progettano una "fattoria intelligente" per il futuro.
**English:** Concluding lesson: students connect what they have learned to major global challenges (climate change, food waste, population growth) and design a "smart farm" for the future.

### 8.1 Obiettivi di Apprendimento / Learning Objectives
| Obiettivo / Objective | Livello / Level |
|------------------------|-----------------|
| Collegare i dati IoT ai temi della sostenibilità (acqua, energia, cibo) / Connect IoT data to sustainability themes (water, energy, food) | Analisi / Analysis |
| Valutare benefici e rischi delle tecnologie agricole / Evaluate benefits and risks of agricultural technologies | Valutazione / Evaluation |
| Progettare una soluzione "smart farm" di gruppo / Design a group "smart farm" solution | Sintesi / Synthesis |
| Presentare il progetto finale alla classe / Present the final project to the class | Comunicazione / Communication |

### 8.2 Materiali Necessari / Required Materials
| Materiale / Material | Quantità / Quantity |
|----------------------|---------------------|
| Poster o strumenti digitali per il progetto / Posters or digital tools for the project | 1 per gruppo / per group |
| Dati raccolti nelle lezioni precedenti / Data collected in previous lessons | 1 set per gruppo / per group |
| Materiale per prototipi (cartone, sensori extra opzionali) / Prototype materials (cardboard, optional extra sensors) | 1 set per gruppo / per group |
| Rubrica di valutazione (stampabile) / Evaluation rubric (printable) | 1 per studente / per student |
| Scheda di lavoro 5 (stampabile) / Worksheet 5 (printable) | 1 per gruppo / per group |

### 8.3 Attività e Fasi / Activity Steps
| Fase / Step | Durata / Duration | Attività / Activity |
|-------------|-------------------|---------------------|
| 1. Introduzione / Introduction | 5 min | Dati globali su cibo e acqua (FAO) / Global food and water facts (FAO) |
| 2. Dibattito / Debate | 15 min | Pro e contro dell'agricoltura digitale / Pros and cons of digital farming |
| 3. Progettazione / Design | 20 min | Ogni gruppo progetta la propria smart farm / Each group designs its smart farm |
| 4. Presentazione / Presentation | 15 min | Ogni gruppo presenta il progetto (3 min) / Each group presents (3 min) |
| 5. Riflessione finale / Final reflection | 5 min | Cosa ho imparato in 5 lezioni? / What did I learn in 5 lessons? |

### 8.4 Punti Dimostrativi per l'Insegnante / Teacher Demo Points (IT/EN)
- Presentare dati reali: ~1/3 del cibo prodotto è sprecato; l'agricoltura usa ~70% dell'acqua dolce mondiale / Present real facts: ~1/3 of produced food is wasted; agriculture uses ~70% of the world's fresh water
- L'irrigazione basata sui dati può risparmiare fino al 30% di acqua / Data-driven irrigation can save up to 30% of water
- Guidare il dibattito tra ottimismo tecnologico e pensiero critico / Guide the debate between technological optimism and critical thinking

### 8.5 Scheda di Lavoro 5 (Stampabile) / Worksheet 5 (Printable)
**Italiano:** Gruppo: ____  Data: ____ — Progetto "Smart Farm del Futuro":
1. Nome della fattoria: ______
2. Quali colture coltiveresti? ______
3. Quali sensori useresti e perché? (pH/EC/temperatura/umidità/altro) ______
4. Come useresti i dati per risparmiare acqua? ______
5. Un rischio o limite della tecnologia considerato: ______
6. Disegna il tuo progetto qui sotto:
**English:** Group: ____  Date: ____ — "Smart Farm of the Future" project:
1. Farm name: ______
2. Which crops would you grow? ______
3. Which sensors would you use and why? (pH/EC/temperature/humidity/other) ______
4. How would you use data to save water? ______
5. A risk or limitation of technology you considered: ______
6. Draw your project below:

---

## 9. Valutazione / Assessment
**Italiano:** La valutazione è formativa e basata su rubriche: ogni scheda è valutata da 1 a 4; la valutazione finale considera il progetto di gruppo della Lezione 5.
**English:** Assessment is formative and rubric-based: each worksheet is scored from 1 to 4; the final evaluation considers the Lesson 5 group project.

### 9.1 Rubrica di Valutazione / Evaluation Rubric
| Criterio / Criterion | 1 (Base / Basic) | 2 (In sviluppo / Developing) | 3 (Competente / Proficient) | 4 (Eccellente / Excellent) |
|----------------------|------------------|------------------------------|-----------------------------|----------------------------|
| Dati e misurazioni / Data and measurements | Dati incompleti / Incomplete data | Dati con errori / Data with errors | Dati accurati e organizzati / Accurate, organized data | Dati accurati + analisi extra / Accurate data + extra analysis |
| Comprensione concetti / Concept understanding | Non spiega i concetti / Cannot explain concepts | Spiega con aiuto / Explains with help | Spiega autonomamente / Explains independently | Spiega e collega più concetti / Explains and connects concepts |
| Lavoro di gruppo / Teamwork | Non collabora / Does not collaborate | Collabora se sollecitato / Collaborates when prompted | Collabora attivamente / Collaborates actively | Guida e supporta il gruppo / Leads and supports the group |
| Progetto finale / Final project | Incompleto / Incomplete | Semplice / Simple | Completo e coerente / Complete, coherent | Innovativo e ben presentato / Innovative, well-presented |

### 9.2 Compito Finale Opzionale / Optional Final Task
**Italiano:** Gli studenti possono creare un poster o un breve video sul loro percorso con MyZubster, da presentare alla fiera della scuola o ai genitori.
**English:** Students can create a poster or short video about their MyZubster journey, to present at the school fair or to parents.

---

## 10. Risorse e Collegamenti / Resources and Links
| Risorsa / Resource | Descrizione / Description | Link / Link |
|--------------------|---------------------------|-------------|
| Guida pratica all'orto intelligente / Practical smart garden guide | Manuale tecnico completo di MyZubster / Full MyZubster technical manual | `guides/GUIDA_ORTO_INTELLIGENTE.md` |
| Documentazione Arduino / Arduino documentation | Reference per ESP32 e sensori / ESP32 and sensor reference | arduino.cc/reference |
| MyZubster GitHub / MyZubster GitHub | Codice sorgente open-source / Open-source source code | github.com/MyZubster |
| FAO — Cibo e agricoltura / FAO — Food and agriculture | Dati globali su cibo e acqua / Global food and water data | fao.org |
| Foglio di calcolo dati / Data spreadsheet | Modello per l'analisi dati (Lezione 4) / Template for data analysis (Lesson 4) | `assets/dati_esempio.csv` |

**Italiano:** Il piano è open-source e liberamente adattabile: gli insegnanti possono modificare durate, materiali e attività in base al livello della classe. Per contribuire o segnalare problemi, aprire un issue nel repository MyZubster.
**English:** The plan is open-source and freely adaptable: teachers can modify durations, materials and activities based on class level. To contribute or report issues, open an issue in the MyZubster repository.

---

*MyZubster — Coltivare il futuro, un dato alla volta / Growing the future, one data point at a time.*
