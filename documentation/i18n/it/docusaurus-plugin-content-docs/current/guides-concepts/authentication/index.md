---
title: "Authentication | Refine v5"
display_title: "Authentication"
sidebar_label: "Authentication"
description: "Gestisci login, logout, identità utente e route protette nelle applicazioni Refine con auth provider."
---

Authentication è il processo con cui si verifica l'identità dell'utente e si gestisce lo stato della sessione nell'applicazione. Refine astrae questo comportamento tramite `authProvider`.

## Auth provider

`authProvider` definisce operazioni come login, logout, identity e permission. Anche se l'applicazione usa JWT, session cookie, OAuth o un identity provider diverso, Refine lavora tramite lo stesso contratto.

```ts title=authProvider.ts
export const authProvider = {
  login: async ({ email, password }) => {
    // Verifica l'utente e avvia la sessione.
  },
  logout: async () => {
    // Termina la sessione.
  },
  check: async () => {
    // Controlla se la sessione utente è valida.
  },
};
```

## Contenuti protetti

Refine può usare il risultato di `check` prima di consentire l'accesso alle route. Se non esiste una sessione, l'utente può essere reindirizzato alla pagina di login; se la sessione è valida, viene mostrata la pagina richiesta.

## Identità utente

`getIdentity` restituisce i dati del profilo dell'utente attivo. Questi dati possono essere usati in menu, header o contesti come audit log.

## Error handling

`onError` può intercettare centralmente gli errori di authentication restituiti dalle chiamate API. Ad esempio, quando arriva una response 401 puoi eseguire logout o avviare un flusso di refresh token.

## Differenza da authorization

Authentication stabilisce chi è l'utente. Authorization stabilisce se quell'utente può eseguire una determinata azione su una resource.
