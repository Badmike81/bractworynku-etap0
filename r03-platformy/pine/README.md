# Skrypty Pine Script — Rozdział 3

## mes-etap0.pine
**Wskaźnik: Bractwo Rynku — MES Etap 0**

Jeden wskaźnik zastępujący siedem osobnych. Zajmuje 1 slot.

### Co zawiera:
- VWAP sesyjny ze wstęgami (odchylenie standardowe 1σ, 2σ)
- EMA 8, 20, 50, 200 z prawidłowymi nazwami w eksporcie CSV
- ATR(14) i RVOL w Data Window
- Dane cross-asset: VIX, NQ, RTY, US10Y, DXY
- Tabela danych na żywo (opcjonalna)

### Jak użyć:
**Opcja 1 — TradingView (najłatwiej):**
Wskaźniki → Społeczność → wyszukaj "Bractwo Rynku MES Etap 0" → Dodaj do wykresu

**Opcja 2 — ręcznie:**
1. Skopiuj zawartość pliku mes-etap0.pine
2. TradingView → ikona Pine (prawy pasek) → Stwórz nowy → Nowy wskaźnik
3. Ctrl+A → Ctrl+V → Dodaj do wykresu

### Eksport CSV:
Po dodaniu wskaźnika: menu layoutu (prawy górny róg) → Pobierz dane wykresu → Download.
Kolumny: time, open, high, low, close, VWAP, VWAP_Upper1, VWAP_Lower1, VWAP_Upper2, VWAP_Lower2, EMA_8, EMA_20, EMA_50, EMA_200, ATR_14, RVOL, VIX, NQ, RTY, US10Y, DXY

### Wersja Pine Script: v6
### Sekcja książki: 3.2.2
```

Commit message: `Dodano README dla skryptów Pine Script`

**3. Wrzuć przykładowy CSV:**

Jeszcze raz **"Add file"** → tym razem **"Upload files"**

Przeciągnij plik `CME_MINI_MES1___1__5_.csv` (ten ostatni, czysty eksport z 21 kolumnami). Przed uplodem zmień mu nazwę na komputerze na `mes-m1-sample.csv`.

Ale uwaga — GitHub wymaga, żeby plik trafił do konkretnego folderu. Najpierw utwórz plik placeholder:

**"Add file"** → **"Create new file"** → nazwa:
```
r03-platformy/csv/README.md

# Przykładowe dane CSV — Rozdział 3

## mes-m1-sample.csv
Eksport M1 z TradingView z wskaźnikiem "Bractwo Rynku — MES Etap 0".

21 kolumn: time, open, high, low, close, VWAP, VWAP_Upper1, VWAP_Lower1, VWAP_Upper2, VWAP_Lower2, EMA_8, EMA_20, EMA_50, EMA_200, ATR_14, RVOL, VIX, NQ, RTY, US10Y, DXY

Format czasu: UNIX timestamp (sekundy od 1970-01-01).
Dane z sesji: marzec 2026, CME_MINI:MES1!, interwał 1 minuta.
