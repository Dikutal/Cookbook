title: Chiles Kong Arne
type: recipe
category: recipes/danish
tags: [dinner]
---
*Tilføjet af Ulrik Rasmussen*

Dependencies
------------
(Angivet i brøker. Gang op med antallet af brugere).

  * 3/4 løg.
  * 3/4 fed hvidløg.
  * 3/4 gulerod.
  * 1/10 stilk bladselleri.
  * 1/4 rød peberfrugt.
  * 1/4 grøn peberfrugt.
  * 3/4 frisk chilipeber.
  * 1/2 dåse flåede tomater.
  * 125+ g hakket oksekød.
  * 5/4 oksekødsbouillon.
  * 1/4 spsk frisk timian.
  * 1/4 tsk sambal oelek.
  * 1/4 tsk salt.
  * 1/4 tsk peber.
  * 1/4 dåse kidneybønner.

Spidskommen smager også fråder!


Algoritme
---------
  * Tilføj følgende arbejdsopgaver til en fælles, trådsikker arbejdskø:
    - Finhakning af løg og hvidløg.
    - Skrælning af gulerødder.
    - Udskæring af gulerødder (i skiver).
    - Udskæring af peberfrugter (i tern).
    - Udskæring af chili (tynde skiver).
  * `pthread_create()` et vilkårligt antal tråde til at udføre
    arbejdet, alt efter hvor mange ressourcer der er
    tilgængelige. Bemærk at en begrænset mængde af delte ressourcer
    såsom spækbræt og knive kan begrænse paralleliteten hvormed
    opgaverne kan udføres.
  * `pthread_join()` alle tråde inden der fortsættes. Resten af opskriften kan kun udføres sekventielt.
  * Hent stor gryde fra statisk lager, og alloker en plads på komfuret. Hæld olie i. `while (!olie->varm) dance_and_sing();`
  * Tilsæt kød. `while (!koed->brunt) do_the_chicken();`
  * Tilsæt løg, hvidløg, chili. Steg igennem i et stykke tid.
  * Tilsæt gulerødder, selleri og peberfrugt. Steg lidt mere igennem.
  * Tilsæt tomater med saft.
  * Tilsæt boullion og krydderier. `while       (!food->tasty) spice_it_up();`.
  * Læg låg på, og lad det simre i 1 times tid.
  * Tag låget af, hæld bønnerne i en sigte og skyl dem, og lad dem simre i 15 minutter.
  * Gør retten lækker med ekstra krydderier og mere chili!
