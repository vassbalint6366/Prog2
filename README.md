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
        ![1002kamera](https://user-images.githubusercontent.com/71563655/135724911-d813830b-1614-47fe-9c19-33fd7d851246.png)
        * A kocsinak nincsen fizikája -> belépek a világba vele és nem esik le a földre (lebeg).
        * 1 óra után megtaláltam a probléma okát ( segített ez a videó: https://www.youtube.com/watch?v=T6vvnLRzjvY&t=301s )
        * Mozog a kocsi, már csak az animáció kell hozzá.
    * 2021.10.03:
        * Animációt megcsináltam hozzá. Idáig nem vettem észre vele kapcsolatban hibát. Ha a kézi féket használjuk akkor megállnak, kanyarodásnál mozdulnak, úgy ahogy kell.
        * Kameramozgást tettem bele, amit az egérrel tudjuk kezelni. -> Kamera bug: be lehet vinni a föld alá és szilárd tárgyak mögé.
        ![1003foldalatt](https://user-images.githubusercontent.com/71563655/135762745-da501ea0-f870-492c-8736-a2fda1c4df94.png)
        * A kocsi könnyen csúszik kanyarodás közben.
        * Kocsinak nincs hangja. Valami kicsit sportosabb hangot találtam itt: https://www.fesliyanstudios.com/royalty-free-sound-effects-download/car-driving-207
        * A hangeffekteket szerkeszteni kell még.
        ![1003hangok](https://user-images.githubusercontent.com/71563655/135768269-fc1ba828-b8ee-43b6-afd1-940ff04a3e73.png)
        * Több óra után meglett a hang, de nem úgy működik ahogyan elképzeltem. A hangja jelenleg szörnyű (vissza fogok térni erre).
    * 2021.10.04:
        * Kamera bug kijavítva. Mostmár nem megy át a falon.
        * Az assets amit letöltöttem (tárgyak) bugosak (hitbox hamarabb kezdődik mint a kinézet).
        * A kocsi hangját nem sikerült javítani.
    * 2021.10.07 - 2021.10.24:
        * Hitbox javítás elkezdése... ez hosszú lesz... ( + lassú haladás zh időszak miatt )
        ![1007hitbox](https://user-images.githubusercontent.com/71563655/136452710-f45f4765-32de-4bef-bb8d-94ae80a8b3d6.png)
        * 15+ óra hitboxjavítás után találtam egy beállítást ami megcsinálja a hitboxot magától (2021.10.18). :)
        ![1018hitboxoutplay](https://user-images.githubusercontent.com/71563655/137687403-749c6c6c-c038-47e7-8e23-de0a3bb03ecb.png)
        * hitboxok elkészültek.
    * 2021.11.01:
        *  Map készítése: Méretezések, ház alapjának elkészítése.
        ![1101map_1](https://user-images.githubusercontent.com/71563655/139710007-6384de7a-2d5b-42f8-beee-9dc5208e2a04.png)
        ![1101elhelyezes_1](https://user-images.githubusercontent.com/71563655/139720065-6b8b46fc-2477-423f-b236-836f04b83c01.png)
    * 2021.11.04:
        * Fény beállítások, fénnyel kapcsolatos hibák javítása.
        ![1104fenyek](https://user-images.githubusercontent.com/71563655/140419515-2f7574b0-151e-485f-a96d-58715c1a258f.png)
        * Lépcső elkészítése négyzetekből és hengerekből.
        ![1104lepcso](https://user-images.githubusercontent.com/71563655/140577103-3f6c157c-3295-429d-b3df-88dd79c366dc.png)
    * 2021.11.05:
        * Nappali kész.
        ![1105nappali](https://user-images.githubusercontent.com/71563655/140576388-f8cddc1a-9823-4bba-a329-9f3399086783.png)
        * Kocsi lámpáját megcsináltam, mivel sok sötét hely volt ahol nem lehetett látni + ha lehetett látni akkor zavaró a fénye, így megcsináltam, hogy ki lehessen kapcsolni a világítást ha éppen nincs rá szükségünk.
        ![1105kocsilampa](https://user-images.githubusercontent.com/71563655/140579118-4e90be31-fd7f-4447-8d47-eb6c0cc1d9b7.png)
        ![1105kocsilampaallitas](https://user-images.githubusercontent.com/71563655/140579045-ca17f2de-d5cd-4c70-b5ee-87a3cb075fec.png)
    * 2021.11.06 - 2021.11.16:
        * Alsó emelet elkészítése + kinti rész: fürdő, szoba, konyha & nappali, kinti "kondipark", folyosó.
        * Díszités kisebb elemekkel, pontos elhelyezések, bugok keresése és javítások.
        * Újabb assets-ek kerültek be --> hitboxok beállítása, javítása
        * A fény azért volt szép mivel volt köd berakva a projektbe, amit sajnos ki kellett vennem mivel nagyon laggolt már az egész.
    * 2021.11.06 - 2021.11.16:
        * A játék nagyon laggol már a gépemen. Több ram kellene ami nem megoldható.
        ![1117niceram](https://user-images.githubusercontent.com/71563655/142500125-e733cbe5-c4de-4236-9be6-4820a9b272b9.png)


        

