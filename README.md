# Elméleti háttér

## Mi is az a Map?
A Map egy kulcs-érték párokat tároló adatszerkezet, ahol a kulcsok és az értékek bármilyen típusúak lehetnek.

A kulcsok egyedinek kell lenniük a Map-ben, mivel egy kulcshoz csak egy érték tartozhat.

Az különböző kulcsokhoz tartozó értékek lehetnek azonosak.
## A HashMap példa használata:
```
import java.util.HashMap;
import java.util.Map;

public class HashMapExample {
    public static void main(String[] args) {
        // HashMap létrehozása
        Map<String, Integer> hashMap = new HashMap<>();

        // Elemek hozzáadása
        hashMap.put("kulcs1", 10);
        hashMap.put("kulcs2", 20);
        hashMap.put("kulcs3", 30);

        // Elemek lekérdezése
        int ertek1 = hashMap.get("kulcs1"); // 10
        int ertek2 = hashMap.get("kulcs2"); // 20

        // Elem eltávolítása
        hashMap.remove("kulcs3");

        // Elemek száma
        int meret = hashMap.size(); // 2

        // Kulcsok lekérdezése
        Set<String> kulcsok = hashMap.keySet(); // ["kulcs1", "kulcs2"]

        // Értékek lekérdezése
        Collection<Integer> ertekek = hashMap.values(); // [10, 20]

        // Tartalmaz-e kulcsot?
        boolean tartalmazzaKulcsot = hashMap.containsKey("kulcs1"); // true

        // Tartalmaz-e értéket?
        boolean tartalmazzaErteket = hashMap.containsValue(20); // true
    }
}
```

***
#Feladat

Írj egy programot, amely egy személyeket nyilvántartó rendszert valósít meg. Készíts két osztályt: egyet a személyek (Person) tárolására és egyet a nyilvántartó rendszer (Registry) kezelésére.

A Person osztálynak a következő adatait kell tárolnia:

- Név (name)
- Kor (age)
- Telefonszám (phone)
A Registry osztálynak a következő funkciókat kell megvalósítania:

- Személy hozzáadása a nyilvántartó rendszerhez
- Személy eltávolítása a nyilvántartó rendszerből
- Személy keresése a nyilvántartó rendszerben név alapján
- Összes személy kiírása a nyilvántartó rendszerből
A feladatod a következők:

Hozz létre egy Person osztályt a megadott adattagokkal és egy konstruktorral, amely inicializálja ezeket az adattagokat.
Hozz létre egy Registry osztályt, amelyben egy mapben tárolod a Person objektumokat. Implementáld a szükséges funkciókat: addPerson(), removePerson(), findPerson(), displayAll().
Írj egy főprogramot (main), ahol példányosítasz egy Registry objektumot és kipróbálod a különböző funkciókat. Például, hozzáadhatsz személyeket, eltávolíthatsz személyeket, keresel személyeket név alapján és kiírod az összes személyt a nyilvántartóból.
