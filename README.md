# Piattaforma di Home Booking - Laboratorio Basi di Dati 2021/22

Questo progetto mira a sviluppare una base di dati per una piattaforma che consente agli utenti di affittare e prenotare alloggi di varie tipologie, come appartamenti interi, camere private e spazi condivisi. L'idea è ispirata a servizi esistenti come [Airbnb](https://www.airbnb.it/).

---

## Caratteristiche principali

### Utenti
Gli utenti possono registrarsi al servizio fornendo:
- **Dati personali**: email, password, nome, cognome, numero/i di telefono.
- **Verifica**: foto della carta d'identità (per essere riconosciuti come verificati).
- **Metodo di pagamento**: necessario per effettuare prenotazioni.

Gli utenti possono assumere due ruoli:
- **Ospiti**: possono prenotare alloggi.
- **Host**: possono affittare i propri alloggi. Gli host possono diventare **superhost** se soddisfano i seguenti criteri:
  - Completamento di almeno 10 soggiorni (per un totale di almeno 100 notti).
  - Tasso di cancellazione massimo dell'1%.
  - Valutazione complessiva pari o superiore a 4.8.

### Alloggi
Ogni alloggio è descritto da:
- **Informazioni generali**: nome, indirizzo (il comune è visibile prima della prenotazione), descrizione.
- **Dettagli**: prezzo per notte/persona, costi di pulizia, orari di check-in e check-out.
- **Caratteristiche**: numero di letti, servizi disponibili (cucina, Wi-Fi, ecc.).
- **Valutazioni**: rating medio e numero di recensioni.
- **Media**: foto rappresentative.

### Preferiti
Gli utenti possono creare liste personalizzate di preferiti per organizzare gli alloggi in base ai viaggi o ai loro interessi.

### Prenotazioni
- Gli utenti possono prenotare alloggi indicando:
  - Intervallo di date.
  - Numero di ospiti (opzionalmente i nomi, se sono registrati al servizio).
- Le prenotazioni devono essere confermate o rifiutate dall'host.
- **Cancellazione**: possibile sia da parte dell'ospite che dell'host.
- **Pagamenti**: il costo totale viene addebitato al momento della conferma.

---

## Recensioni e Valutazioni
Dopo il soggiorno, ospiti e host possono recensirsi reciprocamente.

### Recensioni degli ospiti:
- Due testi distinti:
  - Per l'appartamento.
  - Per l'host.
- Punteggi (da 1 a 5) su:
  - Pulizia
  - Comunicazione
  - Posizione
  - Qualità/prezzo
- Valutazione complessiva: media dei punteggi sopra elencati.

### Recensioni degli host:
- Solo un commento testuale.

### Visibilità delle recensioni:
- Le recensioni diventano visibili:
  - Quando entrambe le parti le hanno completate.
  - Dopo 7 giorni dalla fine del soggiorno, se una delle parti non ha recensito.
- È possibile aggiungere commenti alle recensioni, creando un thread di discussione.

---

## Operazioni periodiche
La base di dati supporta le seguenti operazioni automatizzate:
1. **Aggiornamento settimanale** del tasso di cancellazione degli host.
2. **Verifica giornaliera** dei criteri per la qualifica a superhost.
3. **Classifica mensile** degli alloggi più apprezzati.

---

## Struttura del progetto
Il progetto comprende:
- **Schema del database**: progettato per supportare tutte le funzionalità descritte.
- **Operazioni CRUD**: per la gestione di utenti, alloggi, prenotazioni e recensioni.
- **Automazioni**: implementazione delle operazioni periodiche richieste.

---

## Requisiti
- Database relazionale (es. PostgreSQL, MySQL).
- Software per la gestione delle query (es. DBeaver, pgAdmin).
- Linguaggi di supporto per l’interfaccia utente o script (opzionale).

---

## Ispirazione
Questo progetto prende ispirazione da [Airbnb](https://www.airbnb.it/), e può essere usato come base per implementare una piattaforma di home booking completa.

