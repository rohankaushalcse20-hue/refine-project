# Przykład Refine i18n Next.js

Ten przykład pokazuje, jak połączyć Refine z routingiem i lokalizacją w aplikacji Next.js. Skupia się na `i18nProvider`, wyborze locale oraz utrzymaniu spójnych kluczy tłumaczeń między stronami i zasobami.

## Najważniejsze punkty

- Integruje `i18nProvider` z aplikacją Next.js.
- Pokazuje, jak locale może wpływać na routing i tekst UI.
- Zachowuje nazwy pakietów, ścieżki, komendy i API w oryginalnej formie.
- Nadaje się jako punkt startowy dla aplikacji admin z wieloma językami.

## Uruchomienie

```sh
npm install
npm run dev
```

## Kiedy używać?

Użyj tego przykładu, gdy aplikacja Refine ma działać w Next.js i potrzebuje przełączania języka bez rozbijania konfiguracji `resources`, providerów i stron CRUD.
