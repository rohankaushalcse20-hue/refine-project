---
title: "Tables | Refine v5"
display_title: "Tables"
sidebar_label: "Tables"
description: "Gestisci pagination, filtering e sorting in tabelle e liste collegate al data provider con Refine."
---

Tables e list views sono tra le schermate più comuni nelle applicazioni Refine. Refine combina recupero dati, pagination, sorting, filtering e row actions in un modello basato su provider.

## Dati della lista

`useTable` e gli hooks tabellari delle integrazioni UI usano internamente `useList` e `dataProvider.getList`. In questo modo lo state della tabella resta sincronizzato con le query API.

## Pagination

Le informazioni di pagination possono essere inviate come page, pageSize o con il modello cursor supportato dal provider. Refine traduce lo state del componente UI nella chiamata al data provider.

## Sorting e filtering

Sorters e filters vengono raccolti dai componenti tabellari e passati a `getList`. Se il backend richiede un formato query diverso, puoi fare la trasformazione nel data provider.

## Row actions

Nelle righe della tabella puoi usare button `show`, `edit`, `delete` o azioni personalizzate. Grazie alle definizioni di resource, questi button possono puntare alla route o alla mutation corretta.

## Sincronizzazione con URL

Sincronizzare lo state della lista con l'URL rende condivisibili viste filtrate o ordinate e rende più prevedibile il comportamento della browser navigation.
