# Rendszerterv
## 1. A rendszer célja

A rendszer célja, hogy az üzeneteinket biztonságosabbá tegyük azzal, hogy különböző
titkosítási módszereket alkalmazunk. Ezeket a módszereket vegyíteni is lehet, mellyel
csökkenthetjük a szöveg visszafejtésének esélyét idegen fejtők által. Fontos, hogy a
felhasználó könnyen el tudjon igazodni a felületeken ezért minimalista felhasználói felületet
kap a program. A titkosításhoz meg kell adni bizonyos paramétereket a beállításokban 
(például mekkora legyen a Caesar-féle titkosításnál az eltolás mértéke), majd ugyanezeket
a paramétereket használva a felhasználó vissza is tudja fejteni a titkosított szöveget. 
A program titkosítani/visszafejteni kívánt szöveget fájlból vagy egy szövegdobozból tudja be,- 
és a titkosított/visszafejtet szöveget fájlba menteni tudja vagy egy szövegdobozon keresztül
kiírja a felhasználónak. Ha a felhasználó vissza szeretné fejteni a kívánt titkosított üzenetet,
akkor tudnia kell a használt módszert és a módszerhez szükséges paramétert is.

## 2. Projektterv

### 2.1 Projektszerepkörök, felelőségek:
   * Scrum masters:
     - Bódi Maja
     - Cserneczky Bálint
   * Product owner: Dr. Tajti Tibor Gábor
   * Üzleti szereplő:
     - Megrendelő: Dr. Tajti Tibor Gábor
     
### 2.2 Projektmunkások és felelőségek:
   * Frontend: Bagoly Gábor
   * Backend:
     - Boda Viktor
     - Fejes Bence
     - Matuch Richárd
   * Tesztelés:
     * Bagoly Gábor
     * Boda Viktor 
     * Fejes Bence
     * Matuch Richárd
     
### 2.3 Ütemterv:

|Funkció                  | Feladat                                | Prioritás | Becslés (nap) | Aktuális becslés (nap) | Eltelt idő (nap) | Becsült idő (nap) |
|-------------------------|----------------------------------------|-----------|---------------|------------------------|------------------|---------------------|
|Követelmény specifikáció |Megírás                                 |         1 |             1 |                      1 |                1 |                   1 |             
|Funkcionális specifikáció|Megírás                                 |         1 |             1 |                      1 |                1 |                   1 |
|Rendszerterv             |Megírás                                 |         1 |             1 |                      1 |                1 |                   1 |
|Program                  |Képernyőtervek elkészítése              |         2 |             1 |                      1 |                1 |                   1 |
|Program                  |Prototípus elkészítése                  |         3 |             8 |                      8 |                8 |                   8 |
|Program                  |Alapfunkciók elkészítése                |         3 |             8 |                      8 |                8 |                   8 |
|Program                  |Titkosítási funkciók elkészítése        |         3 |             8 |                      8 |                8 |                   8 |
|Program                  |Fájlbaírás / Fájlból olvasás elkészítése|         3 |             8 |                      8 |                8 |                   8 |
|Program                  |Tesztelés                               |         4 |             2 |                      2 |                2 |                   2 |

### 2.4 Mérföldkövek:
   * Prototípus átadása

## 3. Üzleti folyamatok modellje

### 3.1 Üzleti szereplők

A rendszer regisztrálás nélkül használható. Akármelyik felhasználó, akinek
az eszközén megtalálható a szoftver mindenféle korlátozás nélkül használhatja.
Annak eldöntése, hogy a szoftvert kinek az eszközére települ és ki használhatja
azt a megrendelő vállalat döntésére van bízva.

### 3.2 Üzleti folyamatok

A felhasználó a szoftver elindítása után kedve használhatja a titkosítást és visszafejtést,
kiválaszthatja, hogy ha szövegből szeretne olvasni vagy írni,
valamint a szoftver korlátozásain belül testre szabhatja a beállításokat is.
A beállításokon belül kiválaszthatja a használni kívánt titkosítást és annak
bonyolultságát is.

* **Fájl kiválasztása:** A felhasználó ezen menüpont segítségével kiválaszthatja
a beolvasni kívánt fájlt.
* **Művelet indítása:** Ezen funkció használatával titkosításkor a szoftver elvégzi a titkosítást
és az felhasználó által kívánt módon vagy a szövegdobozban, vagy pedig külön fájlban
megjeleníti azt.
* **Beállítások:** A funkción keresztül elérheti a felhasználó
a szoftver beállításait.

## 4. Követelmények

### Funkcionális követelmények

| ID | Megnevezés | Leírás |
| --- | --- | --- |
| K1 | Titkosítás beállítása | A kívánt titkosításokat és paramétereket a felhasználó be tudja állítani. |
| K2 | Forrás beállítása | A felhasználó kiválaszthatja a kívánt szöveg forrását. Ez vagy egy fájl, vagy egy szövegdoboz a programon belül. |
| K3 | Cselekmény kiválasztása | A felhasználó miután kiválaszthatja, hogy titkosítani vagy visszafejteni szeretné a szöveget. |

### Nemfunkcionális követelmények

| ID | Megnevezés | Leírás |
| --- | --- | --- |
| K4 | Letisztult design | A program ablakainak a designja legyen letisztult, átlátható, könnyen használható. Törekszünk a lehető legkényelmesebb megjelenésre.

### Támogatott eszközök
.NET Framework használata miatt platformfüggő.
Csak olyan Windows rendszeren használható, melyen telepítve van a .NET Framework is.

## 5. Funkcionális terv

### 5.1 Rendszerszereplők

A rendszer, mivel lokálisan a felhasználók számítógépén,
internetre kapcsolódás nélkül működik.
Egyetlen egy jogosultsági kör van, 
ezért a felhasználók között nem teszünk különbséget.

### 5.2 Menühierarchiák

A szoftver egy nagyon egyszerű menürendszert tartalmaz.
Az indításkor a felhasználót a főoldal menü fogadja, ahol
megtalálja az input mezőt, valamint innen átléphet a
beállításokat tartalmazó menüpontba, ahol testre szabhatja
milyen konfigurációt szeretne használni.

## 6. Fizikai környezet

### Vásárolt softwarekomponensek és külső rendszerek
Nincsenek vásárolt szoftverkomponensek.
### Hardver topológia
Az alkalmazás 32 bites Windows rendszerre készült, így a 64 bites verzión is működik.
### Fizikai alrendszerek
Kliens gépek: A követelményeknek megfelelő, Windows-t futtatatására alkalmas PC-k, amik rendelkeznek a .Net keretrendszerrel.
### Fejlesztő eszközök
Visual Studio 2019

## 8. Architekturális terv

### Webszerver
A program nem kapcsolódik az internethez, ezért nem kell webszervert használni

### Adatbázis rendszer
A program nem kapcsolódik adatbázis rendszerhez, ezért nem kell adatbázis rendszert alkalmazni

### A program elérése, kezelése
A programot Windows operációs rendszert futtató és .NET keretrendszerrel rendelkező számítógép
futtathatja. A futtatás egyszerű, csak kétszer kell rákattintani a futtatható állományra, vagy
az állománynak a parancsikonjára.

## 9. Adatbázis terv

Adatbázis használatának hiányában nem szükséges az adatbázis terv,
de a program beállításokat egy fájlba menti el és olvassa be a könnyebb felhasználhatóság
érdekében. Egy felhasználó több ilyen beállítás fájlt is hordozhat magával, a különböző
tartalmú fájlok/üzenetek titkosításához.

## 10. Implementációs terv

 * C# program, ami a .NET keretrendszer alkalmazásával fut.
 * A felhasználói felület - windows form alkalmazás.
 * A programok objektum orientált programozási paradigma használatával.

## 11. Tesztterv

A tesztelések célja a rendszer és komponensei funkcionalitásának teljes vizsgálata,
ellenőrzése a rendszer által megvalósított üzleti szolgáltatások verifikálása.
A teszteléseket a fejlesztői csapat minden tagja elvégzi.
Egy teszt eredményeit a tagok dokumentálják külön fájlokba.

### Tesztesetek

 | Teszteset | Elvárt eredmény | 
 |-----------|-----------------| 
 | Helytelen titkosítási beállítások megadása | A titkosítás nem hajtódik végre. Üzenetben jelezni a felhasználónak, hogy miért és milyen adatok megadásával történhet. |
 | Helyes titkosítási beállítások megadása | Megtörténik a titkosítás. A felhasználó kap egy kulcsot. | 
 | Helytelen fejtési beállítások megadása helytelen kulccsal | A fejtés nem történhet meg. Jelezni a felhasználónak, hogy helytelenek az adatok. | 
  | Helytelen fejtési beállítások megadása helyes kulccsal | A fejtés nem történhet meg. Jelezni a felhasználónak, hogy helytelenek az adatok. | 
  | Helyes fejtési beállítások megadása helytelen kulccsal | A fejtés nem történhet meg. Jelezni a felhasználónak, hogy helytelen a kulcs. | 
 | Helyes fejtési beállítások megadása helyes kulccsal | A fejtés végbemegy. A felhasználó megkapja az üzenetet. | 

### A tesztelési jegyzőkönyv kitöltésére egy sablon:

**Tesztelő:** Vezetéknév Keresztnév

**Tesztelés dátuma:** Év.Hónap.Nap

Tesztszám | Rövid leírás | Várt eredmény | Eredmény | Megjegyzés
----------|--------------|---------------|----------|-----------
például. Teszt #01 | Regisztráció | A felhasználó az adatok megadásával sikeresen regisztrálni tud  | A felhasználó sikeresen regisztrált | Nem találtam problémát.
... | ... | ... | ... | ...

## 12. Telepítési terv

Fizikai telepítési terv: A titkosító/visszafejtő programnak nincs szüksége adatbázis szerverre, 
se webszerverre, se internetre, csak meg kell nyitnunk a PC-n.

Szoftver telepítési terv: Szükségünk van egy 32 bites Windows operációs rendszerű PC-re, 
hogy használni tudjuk a programot.

## 13. Karbantartási terv

Fontos ellenőrizni:
*	A kódolás/visszafejtés jól működik
*	A program nem lassul be

Új kódolási típus megjelenésénél fontos, hogy implementáljuk azt a programunkba, így a felhasználok új élménnyel gazdagodhatnak és biztonságosabbá tesszük a titkosítandó szöveget, fájlt.

Figyelembe kell venni a felhasználó által jött visszajelzést is a programmal kapcsolatban.
Ha hibát talált, mielőbb orvosolni kell, lehet az:
*	Működéssel kapcsolatos
*	Kinézet, dizájnnal kapcsolatos
