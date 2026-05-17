# Inferencer dla Refine

`@refinedev/inferencer` automatycznie generuje widoki dla resources na podstawie struktury danych. Pomaga szybko uzyskać kod startowy dla stron listy, tworzenia, edycji i podglądu, a potem dopasować go do wymagań produktu.

## Instalacja

```sh
npm install @refinedev/inferencer
```

## Podstawowe użycie

Wybierz komponent Inferencer odpowiadający używanej integracji UI i podłącz go do resource albo route.

```tsx
import { AntdInferencer } from "@refinedev/inferencer/antd";
```

Inferencer jest szczególnie przydatny na wczesnym etapie projektu, gdy trzeba szybko zobaczyć działający interfejs CRUD i dostać kod do dalszej ręcznej adaptacji.

## Dokumentacja

- Przeczytaj [dokumentację Inferencer](https://refine.dev/docs/packages/documentation/inferencer/).
- Podstawy resources opisuje [dokumentacja Refine component](https://refine.dev/docs/core/refine-component/).
