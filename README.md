# Prog2 projekt
## A játékról:
Egy open world játék, amiben egy házban tudunk menni egy kicsi autóval. Helyenként található verseny, amit időre kell teljesíteni. Gyerekkori emlékeket idéz fel, mint amikor lent ültünk a kis szőnyegen és ott toltuk ide-oda a kocsit.

## Tevékenységek:
* szeptember:
    * Elkezdtem készíteni a projektet, ami elég nehéz így az elején. Létrehoztam egy előre elkészített világot, amiben nagyjából készen van egy mozgásképtelen kocsi.
    * A kocsit sikerült mozgásra bírni. Ezzel együtt újabb hiba jött.
        * ha egy pillanatra is megáll a kocsi, akkor megint nem lehet vele mozogni.
    * Sebességváltót sikerült összerakni, hogy manuális legyen. Itt is hibába ütköztem és régebbi hiba nem oldódott meg vele. Ide vissza fogok térni később, addig is átrakom a váltót automatára.
        * ha megáll a kocsi továbbra sem tudok vele mozogni.
        * a váltótól teljesen függetlenül képes a kocsi nagyon gyorsan menni.
    * 2021.09.27:
        * sikerült megoldani a mozgásképtelen problémát egy videóval (https://www.youtube.com/watch?v=TNPTyQUS63A&t=167s). Mostmár, ha megáll a kocsi, akkor is tudunk vele tovább mozogni.
        * ![0927mozgokocsi](https://user-images.githubusercontent.com/71563655/134878946-09a86e6c-41c2-4e75-bd1f-41e4f3c3cfc6.png)
        * Hozzáadtam pár assets-et
            * https://www.unrealengine.com/marketplace/en-US/product/a4907129f69c44a892f76782489736ab#
![0927houseassets](https://user-images.githubusercontent.com/71563655/134886117-fcd69fc9-8c3b-4bc5-93bd-02e9a6f9ca4c.png)
            * https://www.unrealengine.com/marketplace/en-US/product/bbcb90a03f844edbb20c8b89ee16ea32?sessionInvalidated=true
    * 2021.10.02:
        * Kocsi kinézet cseréje és kamerabeállítások
        * ![1002kamera](https://user-images.githubusercontent.com/71563655/135724911-d813830b-1614-47fe-9c19-33fd7d851246.png)
        * A kocsinak nincsen fizikája -> belépek a világba vele és nem esik le a földre (lebeg).
        * 1 óra után megtaláltam a probléma okát ( segített ez a videó: https://www.youtube.com/watch?v=T6vvnLRzjvY&t=301s )
        * Mozog a kocsi, már csak az animáció kell hozzá.
    * 2021.10.03:
        * Animációt megcsináltam hozzá. Idáig nem vettem észre vele kapcsolatban hibát. Ha a kézi féket használjuk akkor megállnak, kanyarodásnál mozdulnak, úgy ahogy kell.
        * Kameramozgást tettem bele, amit az egérrel tudjuk kezelni. -> Kamera bug: be lehet vinni a föld alá.
        ![1003foldalatt](https://user-images.githubusercontent.com/71563655/135762745-da501ea0-f870-492c-8736-a2fda1c4df94.png)
        
