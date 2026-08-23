# CEIART Light Controller — Firmware

Repository pubblico ufficiale delle release binarie per **CEIART Light Controller** su scheda Waveshare ESP32-S3-ETH-8DI-8RO.

Il codice sorgente non e' pubblicato in questo repository. I file compilati sono disponibili nella sezione **Releases**.

Versione corrente: **2.4.1**.

La cartella `firmware` contiene inoltre `CEIART-Light-Controller-latest.update.bin`: e' la copia della release piu' recente utilizzata dal pulsante di aggiornamento della pagina web. Il firmware ne verifica dimensione e SHA-256 confrontandoli con i dati ufficiali della Release prima del riavvio.

## Quale file usare

- `CEIART-Light-Controller-vX.Y.Z.update.bin`: aggiornamento di una scheda gia' configurata. Conserva configurazione, password, nomi, scheduling, registro eventi e stati salvati.
- `CEIART-Light-Controller-vX.Y.Z.merged.bin`: immagine completa per prima installazione o ripristino di fabbrica. Cancella i dati presenti.

Per l'aggiornamento dalla pagina web della scheda utilizzare esclusivamente il file `.update.bin`.

Ogni allegato di release include nel servizio GitHub il proprio digest SHA-256, verificato dal firmware prima del riavvio quando si usa l'aggiornamento automatico.

## Prima versione con aggiornamento via LAN

La versione `2.4.0` introduce la pagina **Aggiornamento firmware** riservata all'amministratore. La 2.4.0 deve essere installata una sola volta con il caricatore esterno; la `2.4.1` e' la prima release installabile direttamente dalla nuova pagina web per collaudare l'aggiornamento via LAN.
