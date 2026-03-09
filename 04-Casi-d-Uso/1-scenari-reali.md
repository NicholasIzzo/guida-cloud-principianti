# 🛠️ Casi d'Uso: Perché le aziende usano il Cloud?

La teoria è bella, ma in pratica a cosa serve tutto questo? Ecco tre scenari classici in cui il Cloud "salva la vita" alle aziende.

### 📈 1. Il problema dell'E-commerce e del Black Friday (Scalabilità)
**Problema On-Premise:** Hai 2 server. Per tutto l'anno vanno benissimo. Arriva il Black Friday, il traffico aumenta di 10 volte, i server esplodono, il sito va offline, perdi migliaia di euro. Se compri altri 8 server per gestire il picco, poi per il resto dell'anno rimarranno a prendere polvere (ma li hai pagati carissimi).
**Soluzione Cloud (Auto-Scaling):** Dici al Cloud: *"Se il traffico sale troppo, accendi automaticamente altri server. Appena il traffico scende, spegnili"*. Tu paghi i server extra **solo** per le 24 ore del Black Friday. Geniale, no?

### 💾 2. Svuotare le cantine (Disaster Recovery e Backup)
**Problema On-Premise:** Tieni i backup aziendali in un hard disk nell'ufficio del capo. Un giorno c'è un allagamento o un ladro entra e ruba tutto. L'azienda fallisce.
**Soluzione Cloud:** Salvi tutto su *AWS S3* o *Azure Blob Storage*. I tuoi dati vengono replicati in automatico in 3 edifici diversi, magari in nazioni diverse, garantendoti il 99.999999999% di sicurezza di non perderli mai. Paghi pochi centesimi al mese per Giga.

### ⚡ 3. Codice senza Server (Serverless)
**Problema On-Premise:** Devi eseguire un piccolo script Python ogni notte a mezzanotte. Per farlo, devi tenere acceso un intero server 24 ore su 24, 7 giorni su 7.
**Soluzione Cloud (AWS Lambda / Azure Functions):** Carichi solo il tuo pezzetto di codice sul Cloud. Il Cloud lo "sveglia" a mezzanotte, lo fa girare in 2 secondi, lo spegne. Tu non paghi i server, paghi solo per i **2 secondi** effettivi di calcolo. Costo stimato? Spesso letteralmente 0€ (rientra nei piani gratuiti).
