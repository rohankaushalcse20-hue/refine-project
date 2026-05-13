# @refinedev/simple-rest

`@refinedev/simple-rest` dostarcza data provider dla prostych API REST. Tłumaczy operacje Refine, takie jak `getList`, `getOne`, `create`, `update` i `deleteOne`, na żądania HTTP zgodne z konwencją pakietu.

## Co obejmuje pakiet?

- Podstawowe metody `dataProvider` dla zasobów REST.
- Obsługę paginacji, sortowania i filtrowania przekazywanych z hooków Refine.
- Prosty punkt startowy dla przykładów, prototypów i API o przewidywalnych endpointach.

## Kiedy używać?

Użyj tego providera, gdy backend REST pasuje do prostego kontraktu albo gdy chcesz szybko uruchomić aplikację Refine przed napisaniem własnego `dataProvider`. Nazwy metod, endpointów i pakietów pozostają bez tłumaczenia.
