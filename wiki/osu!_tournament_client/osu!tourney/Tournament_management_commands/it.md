# Comandi per la gestione dei tornei

I seguenti comandi di chat sono forniti per la gestione remota delle sale da torneo multigiocatore:

- `!mp make <nome>` - Crea una stanza da torneo con il nome specificato. Possono essere create al massimo 4 stanze di questo tipo.
  - Questa stanza è speciale in quanto non viene chiusa quando tutti i giocatori hanno lasciato la stanza ed è protetta da una password che impedisce ai giocatori di entrarci autonomamente.
  - Quando la stanza è terminata, usare `!mp close` per chiuderla.
- `!mp makeprivate <nome>` - Crea una stanza da torneo privata con il nome specificato. Questo comando funziona come `!mp make`, ma la cronologia delle partite è visibile solo al creatore della stanza e ai suoi partecipanti.
- `!mp name <titolo>` - Aggiorna il nome della stanza.
- `!mp invite <nomeutente>` - Invita un giocatore nella stanza.
  - Nota: questa operazione *non* aggira i blocchi dei messaggi privati disponibili nel client di osu!, quindi lo staff del torneo dovrà dire ai giocatori di disabilitare "Blocca messaggi privati da non-amici" nelle opzioni di osu!.
- `!mp lock` - Blocca la stanza in modo che i giocatori non possano cambiare squadra e slot.
- `!mp unlock` - Annulla l'operazione sovrastante.
- `!mp size <dimensione>` - Imposta la quantità di slot disponibili (1-16) nella stanza.
- `!mp set <modalità_squadre> [<condizione_di_vittoria>] [<dimensione>]` - Imposta varie proprietà della stanza.
  - `modalità_squadre` - 0: Head To Head, 1: Tag Coop, 2: Team Vs, 3: Tag Team Vs
  - `condizione_di_vittoria` - 0: Score, 1: Accuracy, 2: Combo, 3: Score V2
- `!mp move <nomeutente> <slot>` - Sposta un giocatore all'interno della stanza nello slot specificato.
- `!mp host <nomeutente>` - Trasferisce l'host al giocatore.
- `!mp clearhost` - Rimuove l'host della stanza.
- `!mp settings` - Visualizza i dettagli completi della stanza.
- `!mp start [<tempo>]` - Avvia la partita dopo un tempo prestabilito (in secondi) o istantaneamente se il tempo non è presente.
- `!mp abort` - Interrompe la partita.
- `!mp team <nomeutente> <colore>` - Sposta un giocatore nella squadra specificata.
  - `colore` - red, blue
- `!mp map <idmappa> [<modalità_di_gioco>]` - Cambia la beatmap e la modalità di gioco della stanza.
  - `modalità_di_gioco` - 0: osu!, 1: Taiko, 2: Catch The Beat, 3: osu!Mania
- `!mp mods <mod> [<mod>] [<mod>] …` - Rimuove tutte le mod attualmente applicate e applica le nuove alla stanza.
  - È possibile inserire qualsiasi quantità di mod.
  - `mod` - HR, DT, FL, HD, FI, Freemod, None
- `!mp timer [<tempo>]` - Inizia un conto alla rovescia.
  - `tempo` è 30s di default.
  - Gli annunci del timer avvengono ogni minuto, 30s, 10s, 5s e prima.
- `!mp aborttimer` - Ferma il timer corrente (sia quello normale che quello di inizio partita).
- `!mp kick <nomeutente>` - Caccia il giocatore dalla stanza.
- `!mp ban <nomeutente>` - Bandisce il giocatore dalla stanza.
- `!mp password [<password>]` - Cambia la password della stanza. La password verrà rimossa se `<password>` non viene fornita.
- `!mp addref <nomeutente> [<nomeutente>] …` - Aggiunge un arbitro alla stanza. È possibile aggiungere un massimo di 8 arbitri. Solo il creatore della stanza può aggiungere un arbitro.
  - Gli arbitri devono unirsi alla stanza in gioco, oppure entrando nel canale di chat della stanza tramite `/join #mp_<room_id>` in IRC.
  - Gli arbitri possono gestire la stanza come il creatore, ma non possono aggiungere o rimuovere altri arbitri.
  - L'[osu!tourney client](/wiki/osu!tourney) mostrerà la chat della stanza per gli arbitri.
- `!mp removeref <nomeutente> [<nomeutente>] …` - Rimuove un arbitro dalla stanza. Solo il creatore della stanza può rimuovere un arbitro.
- `!mp listrefs` - Elenca tutti gli arbitri della stanza.
- `!mp close` - Chiude la stanza.
