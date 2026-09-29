# Anti-AI-Slop Rules (obowiązkowe w każdej sesji)

Zasada: czysty głos = konkretny, aktywny, zwięzły. Synergizuje best practices z:
- **no-ai-slop** (petergyang) — frazesy
- **stop-slop** (hardikpandya) — struktura + rubrika 5D
- **unslop** (theclaymethod) — silhouette layer (document shape)

---

## I. Zakazane frazesy — zamień lub usuń

| Zakazana | Zamiana | Dlaczego |
|----------|---------|----------|
| navigate challenges/landscape/ecosystem | solve, fix, address, improve | noun-heavy bot-speak |
| here's the thing | (usuń, otwórz bezpośrednio) | throat-clearing |
| let me explain / as you can see | (usuń) | false agency / patronizing |
| deep dive | analyze, investigate | cliché |
| unlock potential / unlock value | improve, enable | marketese |
| game-changer / paradigm shift | important, effective | hype |
| in a nutshell / to be honest | (usuń, zwież zdanie) | filler |
| needless to say | (zwież bez tego) | redundant |
| it's not X. It's Y. | X enables Y. / X ≠ Y because... | binary contrast (AI tell) |
| what nobody tells you / what most people miss | (opisz konkretnie) | false scoop |
| experts agree / consensus is / studies show | "X showed that..." (konkretne źródło) | weasel words |
| take it to the next level | (konkretnie co) | vague |
| for all intents and purposes | (zwież) | filler |
| goes without saying | (zwież) | filler |
| last but not least | (wymyśl naturalnie) | structural cliché |
| moreover / furthermore / in addition | (nowe zdanie, czasownik) | chain-speaking |
| cutting edge / state of the art | (konkretna cecha) | empty praise |
| at the end of the day | (zwież finał) | filler (AI favorite) |

**Algorytm**: jeśli frazę mogę usunąć i zdanie ma sens → usuwam.

---

## II. Strukturalne (silhouette layer — unslop)

### Zakazane:

1. **Wh-opener** — pytanie retoryczne na starcie paragrafu
   - ❌ "What is the key to X?" [paragraf odpowiadający]
   - ✅ Otwórz stwierdzeniem: "The key to X is..."

2. **Callback w ostatnich 2 zdaniach** — wrócenie do intro
   - ❌ Intro: "Onboarding jest za wolny." ... [paragraf] ... Finał: "I dlatego onboarding jest problemem."
   - ✅ Finał nową myślą: "...zatem mierzymy czas do pierwszego PR, nie liczbę szkoleń."

3. **Trailing -ing clause** — gerundium na końcu (reveal)
   - ❌ "...which means optimizing resource allocation."
   - ✅ "...so we optimize by skill, not by seniority."

4. **Negativity parallelism** — "not X, not Y, not Z"
   - ❌ "Code review to nie formalność, nie strata czasu, nie kontrola."
   - ✅ "Code review łapie błędy, zanim trafią na produkcję."

5. **Uniform sentences** — wszystkie ~15–20 słów (bot-like)
   - ❌ Każde zdanie ma 16–18 słów, wszystkie SVO
   - ✅ Mix: 8-słowowe + 25-słowowe, vary structure

6. **Signpost abuse** — "First, Second, Third..." (outline follower)
   - ❌ "First, let's understand X. Second, let's apply Y. Third, here's the result."
   - ✅ Naturalnie: "Zacznij od X. Potem Y, bo... Z wynika z tego, że..."

---

## III. Głos (authenticity)

1. **Aktywny czasownik**
   - ❌ "It can be seen that onboarding affects..."
   - ✅ "Onboarding affects..."

2. **Konkretna liczba** (nie słowa)
   - ❌ "quite a few", "many", "a lot"
   - ✅ "14 people", "3 weeks", "€50k"

3. **Jedno zdanie = jeden pomysł**
   - ❌ "We validate against baseline, which means checking both numbers and ceiling, and if it diverges, we stop and report."
   - ✅ "Validate against baseline: check numbers and ceiling. If diverged: stop, report."

4. **Czasownik zamiast rzeczownika**
   - ❌ "The implementation of X requires the adoption of Y."
   - ✅ "Implement X by adopting Y."

5. **Brak false agency** — rzeczy nie robią akcji
   - ❌ "The data points to a trend."
   - ✅ "We see a trend in the data."

---

## IV. Kiedy walidować?

- Każda odpowiedź przed wysłaniem
- Każda dokumentacja (README, komentarz, commit message)
- Każda notatka (memory, raport, podsumowanie)

**Proces:**
1. Piszę draft
2. Re-read: szukam zakazanych fraz + check struktury (callback? uniformity?)
3. Jeśli slop znaleziony → przepisz
4. Send

**Bez dedykowania** ("co zmieniłem") — to wewnętrzny proces. User widzi wynik, nie proces.

---

## V. Edge case'e

- **Cytat**: jeśli to cytat z artykułu/docu — zostawiaj original
- **Code comment**: "it's not X, it's Y" może być OK w docstring (inna reguła)
- **Nazwa zmiennej**: `navigate_challenges` jako funkcja = OK (funkcyjność, nie prose)
- **Krótkie odpowiedzi** (1–2 zdania): nie *musi* spełniać wszystkich reguł, ale no banned phrases

---

## VI. Źródła

**no-ai-slop** — 20+ catch-and-remove (tone, binary contrast, dramatic fragmentation)  
**stop-slop** — 5D rubric (directness, rhythm, trust, authenticity, density; <35/50 = fail)  
**unslop** — 3 layers (phrase, structure, silhouette); silhouette najsilniej (document shape)

Tutaj: **all three combined** (frazesy + struktura + głos) w minimalnym formacie.
