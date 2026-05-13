# @refinedev/simple-rest

`@refinedev/simple-rest` è un data provider leggero per collegare API REST al contratto `dataProvider` di Refine.

## Cosa offre?

- Metodi CRUD di base come `getList`, `getOne`, `create`, `update`, `deleteOne`
- Integrazione rapida con endpoint REST
- Comportamento iniziale per pagination, sorting e filtering

## Quando usarlo?

Se il backend espone endpoint REST classici e vuoi collegare rapidamente i dati a Refine senza scrivere un provider personalizzato, questo pacchetto è adatto. Se il formato dell'API è diverso, puoi estendere il comportamento o scrivere il tuo `dataProvider`.

Nome del package e metodi API restano invariati per compatibilità tecnica.
