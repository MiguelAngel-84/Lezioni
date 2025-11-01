# 📘 Lezione Completa su Markdown  
**Autore:** Miguel Angel Ninaquispe Bardales  
**Ultimo aggiornamento:** 01/11/2025  
**Fonte:** Rielaborazione di fonti universitarie e istituzionali (Oregon State University, Wikipedia, Markdownguide.org, Arxiv.org)

---

## 🧭 Sommario
1. [Cos’è Markdown](#1-cosè-markdown)
2. [Fondamenti e Sintassi Base](#2-fondamenti--sintassi-base)
3. [Utilità e Contesti d’Uso](#3-utilità-e-contesti-duso)
4. [Esempi Pratici Reali](#4-esempi-pratici-reali)
5. [Consigli per Iniziare](#5-consigli-per-iniziare)
6. [Limiti e Varianti](#6-limiti-e-varianti)
7. [Conclusione](#7-conclusione)

---

## 1️⃣ Cos’è Markdown

**Markdown** è un linguaggio di *markup leggero* che permette di scrivere testo formattato (titoli, grassetto, liste, link, immagini) usando una sintassi semplice e leggibile.

📚 **Origine:**  
Creato nel 2004 da *John Gruber* con il contributo di *Aaron Swartz*.

📖 **Obiettivo:**  
Consentire di scrivere documenti testuali che siano leggibili anche nel formato “grezzo”, senza dover vedere il codice HTML sottostante.

🔗 **Fonti istituzionali:**
- [Wikipedia - Markdown](https://it.wikipedia.org/wiki/Markdown)
- [Markdown Guide](https://www.markdownguide.org)
- [Oregon State University - Introduction to Markdown](https://blogs.oregonstate.edu/inspire/2022/04/18/an-introduction-to-markdown/)
- [Arxiv.org - R Markdown Applications](https://arxiv.org/abs/1501.01613)

### 💡 Perché usarlo
- **Semplice e leggibile** anche come testo puro.  
- **Portabile:** apribile con qualsiasi editor.  
- **Versionabile:** perfetto con Git.  
- **Concentrato sul contenuto:** niente distrazioni grafiche.  
- **Convertibile:** esportabile in HTML, PDF, DOCX, slides, wiki, ecc.

---

## 2️⃣ Fondamenti & Sintassi Base

### 📑 Titoli
```markdown
# Titolo livello 1
## Titolo livello 2
### Titolo livello 3
```

Esempio:
```markdown
# Introduzione
## Obiettivi
### Dettagli operativi
```

---

### ✍️ Paragrafi e interruzioni
- Un nuovo paragrafo richiede una **riga vuota**.  
- Per un *a capo rigido*: due spazi + invio.

---

### 🔠 Enfasi (corsivo, grassetto, barrato)
```markdown
*corsivo* oppure _corsivo_
**grassetto** oppure __grassetto__
~~barrato~~
```

---

### 📋 Liste

**Non ordinate:**
```markdown
- elemento 1
- elemento 2
  - sotto-elemento 2.1
```

**Ordinate:**
```markdown
1. primo
2. secondo
   a. sotto-punto
```

---

### 🔗 Link e immagini
```markdown
[Nome del link](https://esempio.com)
![Alt text immagine](https://esempio.com/img.png)
```

Esempio:
```markdown
[Vai a Google](https://www.google.com)
![Logo Markdown](https://upload.wikimedia.org/wikipedia/commons/4/48/Markdown-mark.svg)
```

---

### 💻 Blocchi di codice

**Inline code:**
```markdown
Usa il comando `git init`.
```

**Blocco di codice:**
````markdown
```bash
git clone https://github.com/utente/progetto.git
```
````

---

### 💬 Citazioni e linee
```markdown
> Questa è una citazione.
---
***
```

---

### 📊 Tabelle
```markdown
| Colonna A | Colonna B |
|-----------|-----------|
| Valore 1  | Valore 2  |
| Valore 3  | Valore 4  |
```

---

### ✅ Task list
```markdown
- [ ] Attività da completare
- [x] Attività completata
```

---

## 3️⃣ Utilità e Contesti d’Uso

### 🎯 Dove è utile
- File README per progetti software  
- Documentazione tecnica o interna  
- Blog o siti statici (Jekyll, Hugo)  
- Wiki aziendali  
- Appunti accademici o corsi (R Markdown, LiaScript)  
- Note personali (Obsidian, Notion, ecc.)

### ⚙️ Vantaggi pratici
- Riduce la complessità dei documenti  
- Perfettamente integrato con Git  
- Leggibile e modificabile ovunque  
- Conversione multipiattaforma (HTML, PDF, slides)

### 🧪 Ambiti reali
- **GitHub / GitLab:** file `README.md`  
- **R Markdown:** report e analisi dati  
- **Wiki interne:** documentazione di procedure  
- **Didattica:** creazione di corsi e materiali interattivi  

---

## 4️⃣ Esempi Pratici Reali

### 🔹 Esempio A – README progetto GitHub
```markdown
# Siray Branding-Kit
Kit di avvio per il brand *Siray*

## Descrizione
Contiene:
- Mock-up T-shirt  
- Font montagna  
- Palette colori  
- Logo in formato SVG/PNG  

## Installazione
```bash
git clone https://github.com/tuoutente/Siray-Branding-Kit.git
cd Siray-Branding-Kit
```

## Utilizzo
Apri `logo.svg` nel tuo editor vettoriale (Inkscape, Illustrator).  
Modifica la palette nel file `palette.md`.

## Contribuire
- [ ] Aggiungi una variante colore  
- [x] Versione iniziale logo  

## Licenza
MIT License – vedi `LICENSE`
```

---

### 🔹 Esempio B – Documentazione tecnica interna
```markdown
# Procedura Backup – Servizio MSP
## Scope
Descrive i passi operativi per eseguire il backup giornaliero dei server cliente.

## Frequenza
| Server | Frequenza | Responsabile |
|--------|------------|--------------|
| DB-Prod | ogni giorno h 02:00 | Team DB |
| Web-Prod | ogni giorno h 03:00 | Team Web |

## Passi
1. Accedere al server `backup01` via SSH.  
2. Eseguire:
   ```bash
   /usr/local/bin/backup.sh --full
   ```
3. Verificare log:
   ```bash
   tail -100 /var/log/backup.log
   ```
4. Inviare report via email:
   ```bash
   cat /var/log/backup.log | mail -s "Backup Report" ops@azienda.it
   ```

> ✅ Assicurarsi che la destinazione sia montata (`/mnt/backup`)  
> ❌ Non procedere se lo spazio libero < 10%
```

---

### 🔹 Esempio C – Note per blog o brand
```markdown
# Siray – Collezione “Mountain Essence”
**Siray** è una linea di abbigliamento ispirata alle montagne: semplicità, minimalismo, avventura.

## Ispirazione
- Cime innevate  
- Silhouette nette  
- Palette colori: #2E3A4F, #F4F4F9, #A7B6C2  

## Citazione
> “Less is more” – la forza della semplicità

## Mockup
![T-shirt Siray](assets/ts-mockup.png)

## Call to Action
Visita il sito e ricevi il codice sconto del 10% per la pre-order!
```

---

## 5️⃣ Consigli per Iniziare

1. Installa un editor con supporto Markdown (VS Code, Typora, Obsidian, ecc.)  
2. Crea un file `getting_started.md` e prova titoli, liste e link.  
3. Usa **Git** per versionare e visualizzare i cambiamenti.  
4. Se lavori su GitHub, aggiungi un `README.md` per ogni progetto.  
5. Impara a usare **Pandoc** per convertire in PDF o HTML.  
6. Pratica quotidianamente: appunti, riunioni, note tecniche.  
7. Consulta le estensioni più comuni (tabelle, task list, blocchi di codice).  

---

## 6️⃣ Limiti e Varianti

- Markdown “puro” ha una sintassi limitata  
- Ogni piattaforma può avere **estensioni proprie** (GitHub Flavored Markdown, Pandoc, CommonMark)  
- Non adatto per layout grafici complessi  
- Il rendering può variare a seconda del visualizzatore  

🔗 **Risorse utili:**
- [CommonMark Specification](https://commonmark.org/)
- [GitHub Flavored Markdown](https://github.github.com/gfm/)
- [Pandoc](https://pandoc.org/)

---

## 7️⃣ Conclusione

Markdown è uno strumento **leggero, portabile e potente**, perfetto per chi scrive, documenta e collabora in ambito tecnico o creativo.

> “Il miglior markup è quello che sparisce quando leggi.”  
> — *John Gruber*

---

**© 2025 Miguel Angel Ninaquispe Bardales – Tutti i diritti riservati**
