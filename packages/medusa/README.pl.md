# Integracja Medusa dla Refine

`@refinedev/medusa` udostępnia data provider dla [Medusa](https://medusajs.com/). Pakiet pomaga budować interfejsy administracyjne i operacyjne wokół danych commerce Medusa, używając standardowych hooków Refine.

## Instalacja

```sh
npm install @refinedev/medusa
```

## Podstawowe użycie

Zaimportuj provider z `@refinedev/medusa`, skonfiguruj połączenie z Medusa API i przekaż provider do `Refine`.

```tsx
import { Refine } from "@refinedev/core";
import dataProvider from "@refinedev/medusa";
```

Integracja jest przydatna dla ekranów back-office: list produktów, zamówień, klientów i innych encji obsługiwanych już przez Medusa.

## Dokumentacja

- Otwórz [dokumentację Medusa data provider](https://refine.dev/docs/data/packages/medusa/).
- Oficjalne materiały znajdziesz w [dokumentacji Medusa](https://docs.medusajs.com/).
