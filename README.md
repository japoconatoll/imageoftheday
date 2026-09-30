# IMAGE OF THE DAY

Ogni notte a mezzanotte (ora di Roma) guarda le prime pagine del giorno appena chiuso (~60 quotidiani dalla rassegna del Post), trova le fotografie stampate e sceglie la foto del giorno con una regola fissa: quella che compare su più prime pagine; a parità, la più grande. La ritaglia e la pubblica con la data. Gratis, niente chiavi API.

## Messa online

1. Crea un repository pubblico su GitHub e carica tutti i file di questa cartella (inclusa `.github`, che è nascosta: su Mac Cmd+Shift+. nel Finder).
2. Settings → Pages → Source: GitHub Actions.
3. Actions → image of the day → Run workflow, nel campo: `2026-09-27,2026-09-28,2026-09-29` (la prova).
4. Dopo qualche minuto il sito è su `https://<tuo-utente>.github.io/image-of-the-day/`.

## Note

- Una foto sbagliata: cancella la riga in `days.json` e il file in `images/`, poi rilancia il workflow con quella data.
- I quotidiani sportivi sono esclusi (vincerebbero sempre per dimensione): si cambia in `SKIP_PAPERS` dentro `generate.py`.
