---
name: anti-slop
description: Pisz i redaguj bez śladów AI (frazesy, struktura, głos). Stosuj do każdej odpowiedzi, dokumentu, commita, notatki i raportu. Tryby na żądanie - "odslopuj / humanize / brzmi jak AI" (redakcja cudzego tekstu), "sprawdź czy to slop" (detekcja bez przepisywania). Triggers - "anti-slop", "unslop", "brzmi jak AI", "sounds like AI", "humanize this", "za robotycznie", "is this AI slop".
---

# Anti-slop

Czysty głos: konkretny, aktywny, zwięzły. Pakiet łączy trzy warstwy:

1. **Frazesy** - zakazane słowa i zwroty.
2. **Struktura** - kształt tekstu, który zdradza szablon (callback na końcu, "First/Second/Third", zdania równej długości).
3. **Głos** - strona czynna, liczby zamiast "sporo", jedno zdanie = jedna myśl.

Szybka lista reguł: `references/rules.md`. Czytaj ją przy każdym dłuższym tekście.

## Tryb 1: własne pisanie (domyślny, zawsze)

Dotyczy każdej odpowiedzi, README, commita, notatki, raportu, podsumowania.

1. Napisz draft.
2. Przeczytaj go jeszcze raz pod kątem `references/rules.md`: zakazane frazy, callback w ostatnich 2 zdaniach, signposty, jednakowa długość zdań, strona bierna, puste przymiotniki.
3. Jeśli znalazłeś slop, przepisz.
4. Wyślij. Nie opisuj userowi, co poprawiłeś. To proces wewnętrzny.

Krótkie odpowiedzi (1-2 zdania) nie muszą spełniać każdej reguły strukturalnej. Zakazanych fraz nie mogą mieć nigdy.

## Tryb 2: redakcja cudzego tekstu

User wkleja draft i chce go poprawić ("odslopuj", "humanize", "brzmi jak AI").

- Domyślnie: minimalna skuteczna edycja z zachowaniem głosu autora. Procedura i zasady: `references/edit-and-detect.md`, po edycji sprawdź wynik z `references/edit-eval.md`.
- "Mocno" / `--aggressive`: 8 przebiegów z `references/humanize-8-pass.md` (lista słów: `references/ai-tells.md`).
- Pełny katalog 31 wzorców z przykładami poprawek: `references/unslop-patterns.md`.

## Tryb 3: detekcja

User pyta "czy to slop?" albo prosi o audyt bez przepisywania. Nazwij każdy wzorzec, zacytuj linię, podaj poprawkę w kilku słowach. Nie przepisuj, nie wystawiaj oceny, nie zgaduj, czy pisało to AI. Na końcu zaproponuj edycję.

## Konflikty między źródłami

- **Em dash (—).** We własnym tekście: zero. W cudzym drafcie: max 1-2 w długim tekście, jeśli naprawdę pomagają.
- **"I think", "szczerze mówiąc".** Wycinaj jako wypełniacz. Zostaw, gdy wyrażają realną niepewność albo są częścią głosu autora.
- **Cytaty, nazwy zmiennych, kod.** Nie ruszaj.
- **Fakty, liczby, nazwy, daty.** Nigdy nie zmieniaj ani nie dopisuj. Gdy brakuje źródła, zapytaj zamiast wymyślać.

## Język

Tekst PL, więc odpowiedź PL. Tekst EN, więc EN. Polskie odpowiedniki frazesów są w `references/ai-tells.md` (sekcja "Polish-specific").
