## Panoramica
Questo progetto è un'applicazione Angular che fornisce funzionalità per l'autenticazione degli utenti e la gestione dei clienti. Gli utenti possono accedere e gestire i clienti nel sistema.

# Caratteristiche
- Autenticazione dell'utente:
Gli utenti possono accedere con le proprie credenziali.
Credenziali di accesso non valide visualizzano un avviso.
- Gestione dei clienti:
Gli utenti possono visualizzare un elenco di clienti.
Gli utenti possono aggiungere, aggiornare e eliminare clienti.

# Tecnologie Utilizzate
- Angular: Framework front-end per la costruzione dell'applicazione.
- RxJS: Per gestire flussi di dati asincroni.
- Json-server: Per simulare una REST API con capacità CRUD.
- HTML/CSS: Per strutturare e stilizzare l'applicazione.

# Componenti
- LoginComponent
# Modulo
- Visualizza un modulo di accesso.
# Campi del modulo:
- username: Campo obbligatorio.
- password: Obbligatorio, lunghezza minima di 2 caratteri.
# Funzionalità:
Alla sottomissione del modulo, chiama il metodo authenticate dal servizio AuthService.
Alla riuscita dell'accesso, naviga verso l'elenco dei clienti.
Mostra un avviso in caso di credenziali non valide.

# AuthService
- Autenticazione:
Recupera le informazioni degli utenti dal server JSON in base a nome utente e password.
Restituisce i dettagli dell'utente se vengono fornite credenziali valide.

# ClientService
- Gestione dei clienti:
Recupera l'elenco dei clienti.
Metodi per ottenere clienti tramite ID, aggiungere un nuovo cliente, aggiornare un cliente esistente e eliminare un cliente.

# Endpoint API
Il backend è simulato utilizzando json-server con i seguenti endpoint:

- Autenticazione utente: GET http://localhost:3000/users
- Gestione dei clienti:
- GET http://localhost:3000/clients: Recupera tutti i clienti.
- GET http://localhost:3000/clients?userId={id}: Recupera i clienti associati a uno specifico utente.
- POST http://localhost:3000/clients: Aggiunge un nuovo cliente.
- PUT http://localhost:3000/clients/{id}: Aggiorna un cliente esistente.
- DELETE http://localhost:3000/clients/{id}: Elimina un cliente.