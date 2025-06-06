# Enigma2 Emulator Web

Emulatore web modulare per il firmware Enigma2 (OpenATV), progettato per eseguire e fare il debug in tempo reale di plugin Enigma2, inclusi quelli con interfaccia grafica.

---

## Descrizione

Questo progetto implementa un ambiente di emulazione basato su microservizi per simulare il comportamento del firmware OpenATV, con:

- Backend in FastAPI (Python) per core, file system, gestione plugin, logging e rendering GUI.
- Frontend React per l’interfaccia web utente, gestione input remoto, installazione plugin e preview live della GUI.
- Comunicazione tra servizi via API REST e WebSocket.
- Supporto a plugin installabili da file o repository Git remoti.
- Debugging e logging interattivo in tempo reale.
- Snapshot dello stato per ripresa dell’esecuzione.
- UI responsive e compatibilità multi-browser.

---

## Struttura del progetto
enigma2-emulator/
├── backend/ # Microservizi FastAPI
│ ├── app.py
│ ├── requirements.txt
├── frontend/ # Frontend React
│ ├── package.json
│ └── src/
├── .github/
│ └── workflows/
│ └── ci.yml # Pipeline GitHub Actions
└── README.md

## Prerequisiti

- Python 3.10+
- Node.js 16+
- Git

---

## Setup e avvio locale

### Backend

```bash
cd backend
pip install -r requirements.txt
uvicorn app:app --reload --host 0.0.0.0 --port 8000

### Frontend
cd frontend
npm install
npm start
Aprire il browser su http://localhost:3000 per accedere all’interfaccia web.

Utilizzo
Carica/installare plugin da file .ipk o da repository Git.
Visualizza la GUI Enigma2 emulata direttamente nel browser.
Interagisci con la GUI tramite input virtuali (tasti remoti).
Monitora i log e lo stato di esecuzione in tempo reale.
Effettua snapshot e ripristino dello stato dell’emulatore.

CI/CD
Il progetto integra una pipeline GitHub Actions per:

Installare dipendenze backend e frontend

Eseguire build e test

(opzionale) Deploy automatico

Tecnologie utilizzate
Backend: Python, FastAPI, Uvicorn, pyfakefs, WebSocket

Frontend: React, HTML5, CSS3, WebSocket

DevOps: Docker, GitHub Actions

Contributi
Contributi sono benvenuti! Apri una issue o una pull request per miglioramenti o bugfix.


