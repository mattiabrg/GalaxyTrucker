# Prova Finale di Ingegneria del Software – A.A. 2024/2025
Politecnico di Milano – Corso di Ingegneria del Software  
Docente: Alessandro Margara

### Introduzione
Il progetto **Galaxy Trucker** è stato sviluppato come prova finale del corso di **Ingegneria del Software (a.a 2024/2025)** presso il *Politecnico di Milano*.  
L’obiettivo consiste nella realizzazione di una versione software distribuita del gioco da tavolo **Galaxy Trucker**, conforme alle regole ufficiali e ai requisiti di progetto forniti.

Il lavoro mira a dimostrare la capacità di progettare e implementare un sistema complesso secondo i principi di buona ingegneria del software, ponendo particolare attenzione a:
- correttezza e completezza funzionale;
- progettazione modulare basata su **pattern architetturali**;
- gestione della **concorrenza e comunicazione distribuita**;
- robustezza, tolleranza ai guasti e persistenza dei dati.

---

### Architettura del sistema
Il progetto adotta un’architettura **client–server** basata sul pattern **Model–View–Controller (MVC)**, con implementazione in linguaggio **Java SE**.

- **Server**
  - Gestisce la logica di gioco, lo stato condiviso e la sincronizzazione tra i client.
  - Supporta comunicazione tramite **RMI** e **Socket TCP/IP**.
  - Implementa funzionalità avanzate di **persistenza**, **resilienza alle disconnessioni** e **partite multiple**.

- **Client**
  - Permette a ciascun giocatore di partecipare a una partita attraverso un’interfaccia **grafica (GUI)** o **testuale (TUI)**.
  - All’avvio consente di selezionare la tecnologia di comunicazione.
  - Visualizza lo stato del gioco in tempo reale, sia per la propria nave che per quelle degli altri giocatori.

---

### Funzionalità implementate
- ✔️ Implementazione completa del gioco **Galaxy Trucker** (livello II)  
- ✔️ Comunicazione tramite **RMI**  
- ✔️ Comunicazione tramite **Socket TCP/IP** 
- ✔️ **Gestione partite multiple** sul server  
- ✔️ **Persistenza** dello stato di gioco  
- ✔️ **Resilienza alle disconnessioni** dei client  
- ✔️ Interfacce **TUI** e **GUI**  

---

### Esecuzione del programma

**Server**
```
java -jar GalaxyTrucker.jar -s
```
**Client GUI**
```
java -jar GalaxyTrucker.jar -g
```
**Client TUI** ([Guida Galattica](./deliverables/guida_galattica_tui.md))
```
java -jar GalaxyTrucker.jar -t
```
**Porte utilizzate**  
RMI: 1234  
Socket: 1235, 1236
