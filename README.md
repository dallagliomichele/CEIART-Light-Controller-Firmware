# CEIART Light Controller — Firmware

Repository pubblico ufficiale delle release binarie per **CEIART Light Controller** su scheda Waveshare ESP32-S3-ETH-8DI-8RO.

Il codice sorgente non e' pubblicato in questo repository. I file compilati sono disponibili nella sezione **Releases**.

Versione stabile per il vecchio layout 4 MB: **2.4.3**.

Versione di conversione al nuovo layout 16 MB: **2.5.0 pre-release**.

La cartella `firmware` contiene inoltre `CEIART-Light-Controller-latest.update.bin`: e' la copia della release piu' recente utilizzata dal pulsante di aggiornamento della pagina web. Il firmware ne verifica dimensione e SHA-256 confrontandoli con i dati ufficiali della Release prima del riavvio.

## Quale file usare

- `CEIART-Light-Controller-vX.Y.Z.update.bin`: aggiornamento di una scheda gia' configurata. Conserva configurazione, password, nomi, scheduling, registro eventi e stati salvati.
- `CEIART-Light-Controller-vX.Y.Z.merged.bin`: immagine completa per prima installazione o ripristino di fabbrica. Cancella i dati presenti.

Per l'aggiornamento dalla pagina web della scheda utilizzare esclusivamente il file `.update.bin`.

## Conversione una tantum alla versione 2.5.0

La versione 2.5.0 utilizza tutti i 16 MB fisicamente presenti sulla scheda e introduce due slot OTA da 6,25 MiB. Il primo passaggio da una versione 2.4.x richiede il file completo `CEIART-Light-Controller-v2.5.0.merged.bin`, caricato via USB a partire dall'indirizzo `0x0000`.

La conversione cancella tutti i dati precedenti. Il file `.update.bin` non modifica la tabella delle partizioni e non deve essere usato per questo primo passaggio. La release 2.5.0 e' pubblicata come pre-release e non viene proposta automaticamente alle schede con layout 4 MB.

Dopo la conversione, gli aggiornamenti successivi torneranno a utilizzare il normale `.update.bin` via LAN.

Ogni allegato di release include nel servizio GitHub il proprio digest SHA-256, verificato dal firmware prima del riavvio quando si usa l'aggiornamento automatico.

## Prima versione con aggiornamento via LAN

La versione `2.4.0` introduce la pagina **Aggiornamento firmware** riservata all'amministratore. Le versioni fino alla `2.4.3` usano il vecchio layout 4 MB; la `2.5.0` richiede la conversione USB descritta sopra.
