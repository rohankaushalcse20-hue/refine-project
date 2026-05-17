# Integracja React Hook Form dla Refine

`@refinedev/react-hook-form` łączy formularze Refine z [React Hook Form](https://react-hook-form.com/). Pakiet pomaga budować formularze tworzenia i edycji z walidacją, stanem wysyłki oraz integracją z data provider.

## Instalacja

```sh
npm install @refinedev/react-hook-form react-hook-form
```

## Podstawowe użycie

Użyj `useForm` z `@refinedev/react-hook-form`, aby otrzymać właściwości formularza i powiązać wysyłkę z resources Refine.

```tsx
import { useForm } from "@refinedev/react-hook-form";
```

Integracja pasuje do headlessowych interfejsów i własnych komponentów UI, w których trzeba w pełni kontrolować markup formularza.

## Dokumentacja

- Przeczytaj [dokumentację React Hook Form integration](https://refine.dev/docs/packages/react-hook-form/use-form/).
- Ogólne zasady formularzy opisuje [guide forms](https://refine.dev/docs/guides-concepts/forms/).
