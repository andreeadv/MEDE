# Fișe de Date (Data Cards) - CP1

În cadrul acestei etape, am extras, procesat și aliniat spațial date provenite din patru surse independente. Pentru a asigura compatibilitatea în vederea analizei, toate seturile de date au fost reproiectate și agregate pe un grid comun de 500m x 500m (Sistem de coordonate: EPSG:32635). 

---

### 1. Sursa 1: Temperatura Suprafeței Terestre (Termic)
* **Nume set de date:** USGS Landsat 9 (Level 2, Collection 2, Banda ST_B10).
* **Proveniență:** United States Geological Survey (USGS) și NASA, date extrase și procesate prin Google Earth Engine.
* **Perioadă:** 1 iunie – 31 august 2026. Am ales calcularea unei medii pe sezonul estival pentru a surprinde fenomenul de insulă de căldură la intensitatea sa maximă.
* **Rezoluție spațială/temporală:** Rezoluție spațială nativă de 30m / rezoluție temporală de 16 zile. În script, valorile pixelilor au fost agregate (prin medie) pe celulele de 500m.
* **Unități:** Grade Celsius (°C), obținute prin aplicarea factorului de scalare nativ și conversia din grade Kelvin.
* **Goluri de date (Lacune):** Pixeli lipsă (`NaN`) generați de mascarea zonelor cu acoperire noroasă sau umbre ale norilor (s-a utilizat un filtru pentru imagini cu sub 10% nebulozitate).
* **Licență:** Domeniu Public (Public Domain) – acces liber și gratuit.

### 2. Sursa 2: Indicele de Vegetație (Optic)
* **Nume set de date:** Sentinel-2 MSI (Level-2A, Surface Reflectance, Harmonized).
* **Proveniență:** Programul Copernicus (ESA), date extrase prin Google Earth Engine.
* **Perioadă:** 1 iunie – 31 august 2026 (perioadă aliniată strict cu datele termice pentru coerența analizei).
* **Rezoluție spațială/temporală:** Rezoluție nativă de 10m (benzile B8 și B4) / rezoluție temporală de 5 zile. Datele au fost mediate pe gridul de 500m.
* **Unități:** Indicele NDVI (Normalized Difference Vegetation Index) – valoare adimensională teoretică între -1 și 1, care reflectă densitatea și sănătatea vegetației.
* **Goluri de date (Lacune):** Similar cu datele Landsat, pot exista valori lipsă punctuale cauzate de filtrarea pixelilor cu nori.
* **Licență:** Copernicus Sentinel Data Terms and Conditions (date deschise, utilizare liberă).

### 3. Sursa 3: Înălțimea Clădirilor (Formă Urbană - Raster)
* **Nume set de date:** GHSL - Global Human Settlement Layer (GHS_BUILT_H).
* **Proveniență:** Joint Research Centre (JRC) al Comisiei Europene, via Google Earth Engine.
* **Perioadă:** Model de referință pentru anul 2018 (cel mai recent set de date global disponibil pentru acest parametru).
* **Rezoluție spațială/temporală:** Rezoluție nativă de 100m / set de date static pentru epoca 2018. Valorile au fost agregate (medie) la 500m.
* **Unități:** Metri (reprezintă înălțimea medie estimată a mediului construit din respectiva celulă).
* **Goluri de date (Lacune):** Limitarea principală este de natură temporală; clădirile și ansamblurile rezidențiale edificate în București după anul 2018 nu sunt captate în acest model.
* **Licență:** Creative Commons Attribution 4.0 International (CC-BY 4.0).

### 4. Sursa 4: Amprenta la Sol și Rețeaua Stradală (Formă Urbană - Vector)
* **Nume set de date:** OpenStreetMap (OSM) - poligoane pentru clădiri și parcuri, linii pentru infrastructura rutieră.
* **Proveniență:** Comunitatea globală participativă OpenStreetMap, date descărcate prin Overpass API utilizând biblioteca Python `OSMnx`.
* **Perioadă:** Date actualizate la zi (extracție realizată în toamna anului 2026).
* **Rezoluție spațială/temporală:** Date de tip vector cu precizie sub-metrică / actualizare continuă prin crowdsourcing. Geometriile au fost intersectate și decupate exact pe granițele celulelor de 500m.
* **Unități:** Pentru clădiri și parcuri s-a calculat o **fracție** (procent din aria celulei, cu valori între 0 și 1). Pentru drumuri s-a calculat **densitatea** (lungimea liniară a rețelei raportată la suprafața celulei).
* **Goluri de date (Lacune):** Lipsuri inerente mapării participative; pot exista omisiuni în cartografierea unor alei, clădiri sau curți în zonele periferice mai puțin active ale orașului.
* **Licență:** Open Data Commons Open Database License (ODbL).
