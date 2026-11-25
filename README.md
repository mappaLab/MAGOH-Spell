<p align="center">
  <img src="magoh_spell/icons/hat_m.png" width="160" alt="Cappello di MAGOH Spell">
</p>

<h1 align="center">MAGOH Spell</h1>

<p align="center"><b>Italiano</b> · <a href="README.en.md">English</a></p>

<p align="center">
  <a href="https://github.com/francesco-dantoni/MAGOH-Spell/releases/latest"><img src="https://img.shields.io/badge/Scarica_il_plugin-MAGOH__Spell__V1.0.zip-1e78b4?style=for-the-badge" alt="Scarica il plugin: MAGOH_Spell_V1.0.zip"></a>
</p>

MAGOH Spell è un plugin QGIS per documentare e consultare interventi, ritrovamenti ed evidenze archeologiche secondo il modello MAGOH. Consente di lavorare in un GeoPackage locale, importare dati dalle API MAGOH, produrre schede PDF e convertire i dati nel Template GNA 1.6.0.

Sviluppato da **Francesco D’Antoni** e **Lorena Bravi** con il [MAPPA Lab](https://www.mappalab.eu/en/home-eng/) dell’Università di Pisa ([@mappaLab](https://github.com/mappaLab)).

## MAGOH e MAGOH Wiki

- **[MAGOH](https://magoh.cfs.unipi.it/web/guest)** (*Managing Archaeological data for a sustainable Governance of Heritage*) è il portale web per la consultazione dei dati archeologici sviluppato dal MAPPA Lab del Dipartimento di Civiltà e Forme del Sapere dell’Università di Pisa. MAGOH Spell ne importa le schede tramite le API.
- **[MAGOH Wiki](https://magoh-wiki.cfs.unipi.it/index.html)** è la documentazione tecnica del modello dati: Scheda di Intervento, Ritrovamento (III livello), Evidenza archeologica (IV livello), sepolture e thesauri. Le maschere del plugin aprono direttamente la pagina della Wiki relativa alla scheda. È disponibile anche [in inglese](https://magoh-wiki.cfs.unipi.it/en/index.html).

## Installazione in QGIS

> **Attenzione:** per installare il plugin usa lo ZIP della release, non il pulsante verde **Code → Download ZIP** né «Source code». Quegli archivi contengono il codice sorgente dell’intero repository e QGIS non li riconosce come plugin.

1. Clicca **Scarica il plugin** qui sopra, oppure apri la sezione **Releases**, e scarica l’allegato `MAGOH_Spell_V1.0.zip`.
2. In QGIS apri **Plugin → Gestisci e installa plugin → Installa da ZIP** e seleziona l’archivio ancora compresso.
3. Attiva **MAGOH Spell** e apri **Plugin → MAGOH Spell**. Da **Progetto e dati** puoi creare un progetto o aprirne uno esistente.

Prima di aggiornare un progetto già in uso, salva le modifiche e crea una copia del GeoPackage. I metadati dichiarano compatibilità da QGIS 3.34 a 4.x.

## Lavorare con le schede

- Consulta i collegamenti tra interventi, ritrovamenti ed evidenze. Per un progetto con prefisso LSF, le rispettive serie locali iniziano da `LSF-1`, `LSFR-1` e `LSFE-1`. Le schede importate mostrano il loro identificativo MAGOH.
- Cerca una scheda per attributo, ID o voce di vocabolario. Il pannello **Cronologia e categorie** consente di esplorare intervalli cronologici e livelli di caratterizzazione.
- Esporta schede PDF oppure genera il progetto GNA nella cartella con suffisso `_GNA`. Il registro di conversione permette di risalire alle schede di origine.

[Guida illustrata (PDF)](docs/MAGOH_Spell_Guida_1.0.pdf) · [Guida funzionale](magoh_spell/README.md) · [Note della versione](magoh_spell/CHANGELOG.md)

## Licenza e risorse

Il codice originale è distribuito con licenza **GPL-2.0-or-later**. Il template GNA incluso proviene dalla pagina download del Geoportale Nazionale per l’Archeologia ed è adattato per l’uso nel plugin. Le illustrazioni dei cappelli sono di Vittoria Bellon. Le attribuzioni di dati e risorse di terzi sono riportate separatamente. [Licenza](LICENSE) · [Attribuzioni](magoh_spell/ATTRIBUZIONI.md) · [Fonte del Template GNA](https://gna.cultura.gov.it/download.html)

## Creare lo ZIP installabile

Dalla radice del repository esegui `python tools/package_plugin.py`. Troverai l’archivio in `dist/MAGOH_Spell_V1.0.zip`. È il file da allegare alla release su GitHub.
