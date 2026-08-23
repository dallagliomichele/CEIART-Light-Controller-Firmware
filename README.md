# CEIART Light Controller — Firmware

Repository pubblico ufficiale delle release binarie per **CEIART Light Controller** su scheda Waveshare ESP32-S3-ETH-8DI-8RO.

Il codice sorgente non e' pubblicato in questo repository. I file compilati sono disponibili nella sezione **Releases**.

## Quale file usare

- `CEIART-Light-Controller-vX.Y.Z.update.bin`: aggiornamento di una scheda gia' configurata. Conserva configurazione, password, nomi, scheduling, registro eventi e stati salvati.
- `CEIART-Light-Controller-vX.Y.Z.merged.bin`: immagine completa per prima installazione o ripristino di fabbrica. Cancella i dati presenti.

Per l'aggiornamento dalla pagina web della scheda utilizzare esclusivamente il file `.update.bin`.

Ogni allegato di release include nel servizio GitHub il proprio digest SHA-256, verificato dal firmware prima del riavvio quando si usa l'aggiornamento automatico.

## Prima versione con aggiornamento via LAN

La versione `2.4.0` introduce la pagina **Aggiornamento firmware** riservata all'amministratore. La 2.4.0 deve essere installata una sola volta con il caricatore esterno; le versioni successive potranno essere installate dalla pagina web.

