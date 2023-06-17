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
