# Låtens delar – spelet

Pedagogiskt webbspel om **låtdelar** (intro, vers, brygga, refräng, stick, outro, hook,
riff, mellanspel, ad-lib) för musik åk 4–6. Ska ligga på Dannes skolhemsida.

## Vad det är
- **En enda självbärande HTML-fil**: `index.html`. Inga externa filer, inget
  bygge, ingen server. Öppnas med dubbelklick eller laddas upp som den är.
- Fyra lägen: **Ordlista** (lär dig), **Memory** (ord ↔ betydelse), **Bygg låten**
  (placera delarnas namn på rätt textblock i "Regn på rutan"), **Testet** (8 frågor).

## Källa till innehållet
Ordlistan, exemplen, strukturtrappan och låten "Regn på rutan" kommer från Dannes
dokument `Latdelar-ordlista.docx` – texterna är återgivna ordagrant i `DELAR` och `LATEN`.

## Gotchor
- **Färgkoden är genomgående**: varje låtdel har en CSS-variabel `--c-<id>` i `:root`.
  Byter du färg där ändras den i alla fyra lägen. Delens `id` styr allt (`farg(id)`).
- **Ljud AV som standard** (KONFIG.LJUD_PA_START = false) – 25 elevdatorer med ljud
  blir kaos. Web Audio-oscillatorer, aldrig ljudfiler.
- **Distraktorerna i `FRAGOR` är riktiga förväxlingar** (brygga↔stick, hook↔riff,
  intro↔outro), inte slumpade fel. Byt inte ut dem mot slump.
- Fel svar ger alltid en **mikrolektion** (förklaring + delens definition), aldrig bara "fel".
- Svarsalternativens ordning slumpas varje fråga – annars lär sig eleven positionen.
- **Ingen elevdata sparas** utöver rekord i localStorage (`latdelar_*`). Inga namn,
  inget skickas någonstans. Håll det så.
- Touch: allt funkar med tryck (välj kloss → tryck ruta). Drag & släpp finns som bonus
  för mus. Lägg inte in mönster som kräver hover.
- Öka versionsnumret i `<title>` vid varje leverans.
- Filen heter `index.html` för att GitHub Pages ska servera den på repots rot-URL.
