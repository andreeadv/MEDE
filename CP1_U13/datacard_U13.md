# Fișe de Date (Data Cards) - CP1


### 1. Sursa 1: Temperatura Suprafeței Terestre (Termic)
- **Nume set de date:** USGS Landsat 9 (Level 2, Collection 2, Banda ST_B10).
- **Proveniență:** United States Geological Survey (USGS) și NASA, date via Google Earth Engine.
- **Perioadă:** 1 iunie – 31 august 2026. Baza de date se axează pe sezonul estival pentru a capta fenomenul de insulă de căldură la intensitatea sa maximă.
- **Rezoluție spațială/temporală:** Rezoluție spațială nativă de 30m / rezoluție temporală de 16 zile.
- **Unități:** Grade Celsius (°C), derivate prin aplicarea factorului de scalare nativ și conversia din grade Kelvin.
- **Goluri de date (Lacune):** Date lipsă generate de mascarea zonelor cu acoperire noroasă sau a umbrelor norilor la momentul capturii satelitare.
- **Licență:** Domeniu Public (Public Domain) – acces liber și gratuit.

### 2. Sursa 2: Indicele de Vegetație (Optic)
- **Nume set de date:** Sentinel-2 MSI (Level-2A, Surface Reflectance, Harmonized).
- **Proveniență:** Programul Copernicus (ESA), date via Google Earth Engine.
- **Perioadă:** 1 iunie – 31 august 2026.
- **Rezoluție spațială/temporală:** Rezoluție nativă de 10m (benzile B8 și B4) / rezoluție temporală de 5 zile.
- **Unități:** Indicele NDVI (Normalized Difference Vegetation Index) – valoare adimensională teoretică între -1 și 1, care reflectă densitatea și sănătatea vegetației.
- **Goluri de date (Lacune):** Valori lipsă punctuale cauzate de prezența norilor, a umbrelor acestora sau a ceții.
- **Licență:** Copernicus Sentinel Data Terms and Conditions (date deschise, utilizare liberă).

### 3. Sursa 3: Înălțimea Clădirilor (Formă Urbană - Raster)
- **Nume set de date:** GHSL - Global Human Settlement Layer (GHS_BUILT_H).
- **Proveniență:** Joint Research Centre (JRC) al Comisiei Europene.
- **Perioadă:** Model de referință pentru anul 2018 (cel mai recent set de date global disponibil pentru acest parametru).
- **Rezoluție spațială/temporală:** Rezoluție nativă de 100m / set de date static reprezentativ pentru anul 2018.
- **Unități:** Metri (reprezintă înălțimea medie estimată a mediului construit).
- **Goluri de date (Lacune):** Limitare de natură temporală; clădirile și ansamblurile rezidențiale edificate după anul 2018 nu sunt prezente în acest model.
- **Licență:** Creative Commons Attribution 4.0 International (CC-BY 4.0).

### 4. Sursa 4: Amprenta la Sol și Rețeaua Stradală (Formă Urbană - Vector)
- **Nume set de date:** OpenStreetMap (OSM) - poligoane pentru clădiri și parcuri, linii pentru infrastructura rutieră.
- **Proveniență:** Comunitatea globală participativă OpenStreetMap, date extrase via Overpass API.
- **Perioadă:** Toamna anului 2026.
- **Rezoluție spațială/temporală:** Date de tip vector cu precizie sub-metrică / actualizare continuă prin crowdsourcing.
- **Unități:** Fracție (procent de acoperire per arie pentru clădiri și parcuri) și Densitate (lungime liniară a rețelei stradale raportată la arie).
- **Goluri de date (Lacune):** Lipsuri inerente mapării participative; pot exista omisiuni în cartografierea unor alei, clădiri sau curți în zonele periferice aflate în curs de mapare.
- **Licență:** Open Data Commons Open Database License (ODbL).
