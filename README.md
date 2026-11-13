# Prove bottone

Cinque prototipi di hero e bottoni costruiti su un design system "carta e inchiostro": Inter Tight per il testo, Cambo come serif decorativo, Pixelify come accento pixel e una palette bianco, nero e arancio.

HTML e CSS statici, senza build e senza dipendenze (tranne Google Fonts).

## Anteprima

Apri `index.html` nel browser, oppure avvia un server locale:

```bash
python -m http.server 8000
```

e vai su http://localhost:8000. La barra in basso porta da un prototipo all'altro (`#p1` … `#p5`).

## I prototipi

| # | Hero | Bottoni |
|---|------|---------|
| 01 | **Editoriale**: titolo display con la "&" in Cambo corsivo | Pillola nera in cui la freccia esce e ne rientra un'altra, link con sottolineatura che si ritrae |
| 02 | **Inchiostro**: fondo scuro, testo centrato | Riempimento arancio dal basso con bordo curvo, testo che rotola verso l'alto |
| 03 | **Flash**: tattoo old school in pixel art, solo bianco e nero | Blocco d'inchiostro con cucitura tratteggiata, bottone a cartiglio, timbro "walk-in" rotante |
| 04 | **Griglia**: titolo su 12 colonne e meta a lato | Righe di lista a tutta larghezza con riempimento da sinistra |
| 05 | **Arancio**: fondo pieno con nastro di testo che scorre | Bottone circolare che segue il cursore |

## Struttura

- `index.html`: markup dei cinque hero e il JavaScript (pixel art, bottone magnetico, navigazione)
- `prova.css`: token del design system, base e un blocco CSS per ogni prototipo

## Note

- Le animazioni usano `--ease-brand` (`cubic-bezier(.65, .05, 0, 1)`) e `--ease-out-expo`. Il prototipo 03 usa `steps()` per un movimento a scatti.
- Viene rispettato `prefers-reduced-motion`. L'effetto magnetico si attiva solo con il mouse.
- I disegni del prototipo 03 sono griglie di caratteri nell'oggetto `FLASH` in `index.html`: `X` è inchiostro, `o` è carta, `d` è il retino. Si usano con `data-flash="nome"`.
