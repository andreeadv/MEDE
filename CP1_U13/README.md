# Fișe de Date (Data Cards) - CP1
**Proiect:** Analiza Insulei de Căldură Urbane (București)
**Unitatea de analiză:** Grid spațial de 500m x 500m

---

### 1. Sursa 1: Temperatura Suprafeței Terestre (Termic)
* **Nume:** USGS Landsat 9 (Level 2, Collection 2, Banda ST_B10)
* **Proveniență:** USGS și NASA (date descărcate prin Google Earth Engine)
* **Perioadă:** 1 iunie – 31 august 2026 (medie estivală)
* **Rezoluție spațială/temporală:** 30m rezoluție spațială nativă / 16 zile rezoluție temporală (datele au fost agregate la gridul de 500m)
* **Unități:** Grade Celsius (°C)
* **Goluri:** Pixeli cu date lipsă din cauza acoperirii noroase sau a umbrelor norilor.
* **Licență:** Domeniu Public (Public Domain - date deschise și gratuite).

### 2. Sursa 2: Indicele de Vegetație (Optic)
* **Nume:** Sentinel-2 MSI (Level-2A, Surface Reflectance)
* **Proveniență:** Programul Copernicus, Agenția Spațială Europeană (date descărcate prin Google Earth Engine)
* **Perioadă:** 1 iunie – 31 august 2026 (medie estivală)
* **Rezoluție spațială/temporală:** 10m rezoluție spațială nativă / 5 zile rezoluție temporală (datele au fost agregate la gridul de 500m)
* **Unități:** NDVI (Normalized Difference Vegetation Index) - valoare adimensională cuprinsă între -1 și 1.
* **Goluri:** Valori lipsă izolate provocate de nebulozitate sau ceață la momentul trecerii satelitului.
* **Licență:** Copernicus Sentinel Data Terms and Conditions (utilizare liberă).

### 3. Sursa 3: Înălțimea Clădirilor (Formă Urbană)
* **Nume:** GHSL - Global Human Settlement Layer (GHS_BUILT_H)
* **Proveniență:** Joint Research Centre (JRC) al Comisiei Europene (prin Google Earth Engine)
* **Perioadă:** Anul de referință 2018 (cel mai recent dataset global disponibil)
* **Rezoluție spațială/temporală:** 100m rezoluție spațială / model static pentru 2018 (agregat la gridul de 500m)
* **Unități:** Metri (înălțimea medie a structurilor construite)
* **Goluri:** Inexistența datelor pentru clădirile și cartierele rezidențiale construite după anul 2018.
* **Licență:** CC-BY 4.0 (Creative Commons Attribution 4.0 International).

### 4. Sursa 4: Amprenta la Sol (Formă Urbană Vectorială)
* **Nume:** OpenStreetMap (OSM) - clădiri, parcuri și rețea stradală
* **Proveniență:** Comunitatea OpenStreetMap (date extrase via Overpass API)
* **Perioadă:** Toamna anului 2026 (extracție la zi)
* **Rezoluție spațială/temporală:** Precizie vectorială sub-metrică / actualizare temporală continuă (crowdsourcing). Poligoanele au fost intersectate pe gridul de 500m.
* **Unități:** Fracție (procentaj de acoperire per celulă pentru clădiri și parcuri) și Densitate (lungime liniară per arie pentru drumuri).
* **Goluri:** Lipsa datelor în zonele periferice necartografiate complet de către voluntari.
* **Licență:** ODbL (Open Data Commons Open Database License).
