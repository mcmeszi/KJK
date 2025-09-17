# StoryBuilder

Egy egyfájlos, offline használható történet-építő alkalmazás található ebben a repóban. A `storybuilder.html` tartalmaz minden szükséges HTML, CSS és JavaScript kódot a jelenetek szerkesztéséhez, a gráf vizualizálásához, a lejátszáshoz és az exportáláshoz.

## Megnyitás

1. Töltsd le vagy klónozd a repót a saját gépedre.
2. Dupla kattintással nyisd meg a `storybuilder.html` fájlt a kedvenc böngésződben (Chrome, Edge, Firefox vagy Safari). Nem szükséges semmilyen szerver vagy internetkapcsolat.
3. A projekt adatai automatikusan a böngésző `localStorage` tárában tárolódnak, így a következő megnyitáskor visszatöltődnek.

## Szerkesztés

- A `storybuilder.html` egyetlen fájl. Nyisd meg Visual Studio Code-ban vagy bármelyik szövegszerkesztőben.
- A stílus és a logika is ebben a fájlban található, így bővítéskor érdemes szekciók szerint (CSS, HTML, JavaScript) navigálni.
- Verziókezeléshez a repó már tartalmaz egy Git környezetet, így commitokkal követheted a módosításokat.

## Funkciók röviden

- Jelenetek létrehozása, szerkesztése, törlése.
- Kötelező címke mező vizuális jelzéssel.
- Elágazások kezelése, új céljelenet gyors létrehozása.
- Kezdő jelenet kijelölése és lejátszás mód.
- Vászon: zoom, pan (középső/jobb gomb), doboz húzás, élcímkék, törött linkek kiemelése, kezdő jelenet jelzése.
- Diagnosztika: árva csomópontok, nem elérhető jelenetek, törött linkek listája.
- Export: JSON, TXT, DOCX (OpenXML formátumban, a `docx` könyvtár segítségével).
- Import JSON-ból, automatikus mentés `localStorage`-ba.

## Ismert korlátok és bővíthetőség

- A jelenlegi automatikus elrendezés egy egyszerű körkiosztás; nagy projektekhez egy erősebb force-directed algoritmus javíthatná az átláthatóságot.
- Az élcímkék canvas-on jelennek meg, de jelenleg nem szerkeszthetők közvetlenül a térképen.
- Nincs külön undo/redo verem; fejlesztéshez érdemes verziókat exportálni JSON formátumban.
- A DOCX export a `docx` CDN-t használja, ezért teljesen offline módban a fájl első megnyitásakor internetkapcsolat szükséges a könyvtár betöltéséhez. Alternatívaként a könyvtár fájlját be is ágyazhatod a projektbe.
- A teljesítmény 100+ jelenetnél is stabil, de további optimalizálás (pl. web workeres számítások, virtuális lista) későbbi fejlesztési lehetőség.

## Licenc

A projekt tartalma alapértelmezés szerint minden jog fenntartva. Saját célra szabadon módosíthatod.
