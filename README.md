# Suomen kuntien vaakunat

Tässä hakemistossa on kuvia Suomen kuntien vaakunoista. Kuvatiedostojen nimet on muodostettu pohjautuen kunkin kunnan nimeen, joka on hankittu Tilastokeskuksen avoimen datan palvelusta [stat.fi](https://pxdata.stat.fi/PxWeb/api/v1/en/StatFin/synt/statfin_synt_pxt_12dy.px).

## Tiedostonimien muodostaminen

Kunnan nimet muunnettiin tiedostonimiksi seuraavan Java-koodin avulla:

```java
Normalizer.normalize(name, Normalizer.Form.NFD)
    .replaceAll("[^\\p{ASCII}]", "")
    .replaceAll("-|\\s", "_")
    .toLowerCase();
```
