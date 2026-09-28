# Diva Presets

Colección de presets para **[u-he Diva](https://u-he.com/products/diva/)**: la librería de fábrica, las bibliotecas de terceros instaladas y una carpeta propia con los patches favoritos/seleccionados.

Son **~9.000 archivos `.h2p`** repartidos en 67 carpetas más 83 presets sueltos en la raíz.

## Estructura

### Librería de fábrica (u-he)

Las carpetas numeradas son la organización original de Diva por tipo de sonido:

| Carpeta | Presets |
|---|---|
| `1 BASS` | 78 |
| `2 LEAD` | 99 |
| `3 POLY SYNTH` | 90 |
| `4 DREAM SYNTH` | 68 |
| `5 PERCUSSIVE` | 33 |
| `6 RHYTHMIC` | 52 |
| `7 EFFECTS` | 56 |
| `8 TEMPLATES` | 11 |

`8 TEMPLATES` contiene los patches `INIT …` (Jupe-6/8, June-60, MS-Rev1/2, Minimono, Minipoly, Mongrel, Alpha, Digi-Uhbie): puntos de partida limpios por modelo de sintetizador emulado.

`THIRD PARTY` (883) es el banco de contribuciones de la comunidad que viene con Diva, con subcarpetas por autor (Basari, Bigtone, BrontoScorpio, Fernando's hardware factory, Ingo Weidner, MCnoone, Mr Wobble, Sjoerd van Geffen, Tasmodia, TREASURE TROVE!).

Los presets sueltos de la raíz son la librería original con prefijo de autor (`HS` Howard Scarr, `MK`, `IW` Ingo Weidner, `SG`, `ROY`, `TUC`, `XS`…).

### Carpeta propia

- **`MIS PRESETS`** (44) — selección personal: los patches que uso de verdad, copiados desde el resto de las librerías más algunos propios.

### Bibliotecas de terceros

Packs comerciales / de autor instalados, una carpeta por pack:

- **Plughugger** — Analog House Drums, Classic House Chords, DBX-d, Dark Techno, Modern Bass Expander (227), Stylewalker (255), The Second Renaissance, Twilight 1-3 *(150 c/u)*
- **The Unfinished** — Ex Machina, Phenom Vol.1-2, Praxis, Skyline Vol.1-2, Synthwave, Rekkerd.org Contest
- **PML (Production Music Live)** — Deep Melodic Foundations, Melodic Techno by Tim Engelhardt Vol.2, Melodic House – Rise, Organic House, Organic Sounds 2-3
- **Transitions** — Aiyn Zahev Vol.1 y Vol.3, Resonance Sound Vol.2
- **Luftrum** — 9, 11, Synthwave
- **Sounds Divine** — Director's Cut, Original Score
- **Sonic Elements** — Overload Vol.1, Overload Vol.2 MAXX
- **Otros** — Blue-eyed Blond Ape Rezo (646), Kyhon DEFORM (540), Monomo Sound Design PULSE (240), Twolegs Toneworks Late Night Deep House Chords Vol.3 (208), SoundDUST FRICTION, Subsonic Artz Nexus 49, Performer by Howard Scarr, Waveformless Prima, Xenos Nostalgic Circuits, ZenSound Aethra, Bjulin Waves Flavors, Arksun, Oblivion Sound Lab Neon Circuits, Triple Spiral Audio Pagan V, Trance Techno by Lukas Jankowski, Swan Classic OB, NewLoops Diva Expansion, Rob Lee EDM, Patchbay The Midnight, Binary Oblivion, Bronto Scorpio Additions, Tunesurge Cosmos

`MIDI Programs` sólo guarda el `Midi.Bank.Cache.txt` que genera Diva para el mapeo de Program Change.

## Instalación

Este repo **es** la carpeta de presets de Diva. Clonalo (o copiá su contenido) en:

- **Windows** — `C:\ProgramData\u-he\Diva.data\Presets\Diva`
- **macOS** — `/Library/Application Support/u-he/Diva.data/Presets/Diva`

Después, en Diva: menú de presets → **Rescan Folders** (o reiniciá el host) para que aparezcan.

Para instalar sólo una carpeta, copiala suelta dentro de ese directorio; Diva toma cada subcarpeta como una categoría navegable en el browser.

## Formato `.h2p`

Los presets de u-he son texto plano. Un bloque `/*@Meta … */` con los metadatos que usa el browser para filtrar, seguido de los parámetros del motor:

```
/*@Meta

Author:
'Mr Wobble'

Description:
'techno stab ~ "The Vamp"?'

Categories:
'Keys:Chords, Stabs:Chords, Stabs:Digital'

Features:
'Mono, Glide, Percussive, Unison'

Character:
'Bright, Harmonic, Wide, Modern, Synthetic'

*/

#AM=Diva
#Vers=10001
...
```

Al ser texto, se pueden editar tags (`Categories`, `Features`, `Character`) y buscar por parámetros con grep sin abrir el plugin.

## Notas

- Los packs comerciales están acá para respaldo personal; los derechos son de sus autores respectivos. No redistribuir.
- Los archivos `.h2p` se versionan como binarios en git (contienen bytes no UTF-8), así que los diffs no se muestran línea por línea.
