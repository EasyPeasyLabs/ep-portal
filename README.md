# EasyPeasy Lab - Portale Iscrizioni (Progetto C)

Questo repository contiene il **Portale Iscrizioni** dell'ecosistema EasyPeasy Lab. Il portale funge da interfaccia pubblica per la finalizzazione delle iscrizioni da parte dei lead.

## Architettura e Sicurezza

Il progetto implementa la **Gateway Isolation**: l'URL Del Gestionale (Progetto A) viene mantenuto segreto tramite l'uso di rewrites su Vercel. 

- **URL�Pubblico:** `https://ep-portal-chi.vercel.app/i/:leadId`
- **Gateway:** Le richieste vengono inoltrate in modo trasparente a Google Cloud Run per la generazione delle anteprime WhatsApp.

## Funzionalità((- **Integrazione Dati:** Recupero automatico dei dati pre-inseriti dal Progetto B.
- **Scelta Corso:** Visualizzazione dinamica dei posti disponibili e degli orari.
- **Pagamento:** Integrazione con Stripe per il blocco del posto.
- **Fatturazione:** Raccolta dati fiscali certificata.

## Deploy

Il deploy è gestito automaticamente tramite Vercel al push sul branch `main`.

### Comandi Rapidi
```powershell
# Installazione dipendenze
npm install

# Sviluppo locale
npm run dev

# Deploy manuale
vercel --prod
```