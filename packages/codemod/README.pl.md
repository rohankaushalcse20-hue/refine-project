# Codemod dla Refine

`@refinedev/codemod` pomaga automatyzować migracje kodu między wersjami Refine z breaking changes. Narzędzie analizuje kod źródłowy projektu i stosuje transformacje, które inaczej trzeba byłoby wykonać ręcznie.

## Instalacja i pomoc

Dostępne scenariusze można sprawdzić przez `--help`.

```sh
npx @refinedev/codemod --help
```

## Podstawowe użycie

Uruchamiaj codemod z katalogu głównego projektu, aby transformacje mogły znaleźć pliki źródłowe i ustawienia pakietów.

```sh
npx @refinedev/codemod
```

Przed uruchomieniem warto zapisać czyste drzewo robocze w git, aby łatwo przejrzeć zmiany i wycofać nietrafione poprawki.

## Dokumentacja

- Przeczytaj [dokumentację codemod](https://refine.dev/docs/packages/codemod/).
- Ogólne instrukcje aktualizacji znajdziesz w [dokumentacji Refine](https://refine.dev/docs/).
