# parlagfu_detektalas_gepi_tanulasal
Parlagfű detektálása Sentinel–2 műholdfelvételek, vegetációs indexek és gépi tanulási módszerek alkalmazásával.

# Parlagfű detektálása Sentinel–2 idősorok és gépi tanulás alapján

Ez a repository a diplomamunkámhoz kapcsolódó Python-alapú feldolgozási munkafolyamatot tartalmazza, amely az ürömlevelű parlagfű (*Ambrosia artemisiifolia L.*) Sentinel–2 műholdfelvételek alapján történő detektálhatóságát vizsgálja.

A módszertan Sentinel–2 L2A műholdképekre, vegetációs indexekre, fenológiai idősorokra és Random Forest osztályozási modellre épül.

## Téma

A kutatás célja annak vizsgálata, hogy Sentinel–2 műholdfelvételek és gépi tanulási módszerek segítségével milyen mértékben azonosíthatók a parlagfűvel fertőzött területek egy Fejér vármegyei mintaterületen.

A feldolgozás során több időpontból származó Sentinel–2 felvételek alapján vegetációs indexek és idősor-alapú statisztikai jellemzők kerültek előállításra, majd ezek felhasználásával Random Forest modell készült a parlagfű jelenlétének pixelalapú becslésére.

## Főbb feldolgozási lépések

A repositoryban szereplő notebookok és scriptek az alábbi főbb lépéseket dokumentálják:
1. Sentinel–2 L2A képek lekérdezése és letöltése a Copernicus Data Space Ecosystem API-n keresztül.
2. T33TYM és T33TYN MGRS csempék mozaikolása.
3. Fejér vármegyei mintaterület kivágása.
4. A sávok 10 méteres rácsra illesztése.
5. SCL-alapú felhőmaszkolás és 10 napos medián kompozitok készítése.
6. Jellemzők előállítása a tanítóadatokhoz
7. Random Forest modell tanítása és kiértékelése.
8. Klasszifikált parlagfű-raszter előállítása.

## Használt adatok
A feldolgozás főbb bemeneti adatai:
- Sentinel–2 L2A műholdfelvételek
- Sentinel–2 Scene Classification Layer / SCL felhőmaszkoláshoz
- Fejér vármegye határa
- parlagfűvel fertőzött területeket tartalmazó tanítópoligonok
- CLCplus backbone felszínborítási adatok a nem releváns területek maszkolásához
A nagy méretű műholdképek és térbeli bemeneti adatok nem minden esetben részei a repositorynak.

## Használt módszerek
A feldolgozás során több vegetációs index került kiszámításra, többek között:
- NDVI
- GNDVI
- EVI
- MSAVI2
- NDRE
- CIRE
- PSRI
- NDWI
A modellalkotás Random Forest osztályozóval történt. A tanítás során a spektrális idősorok, vegetációs indexek és ezekből képzett statisztikai jellemzők szolgáltak bemeneti változóként.

## Technológiai környezet
A kódok Python nyelven készültek. A fontosabb használt csomagok:
- rasterio
- geopandas
- numpy
- pandas
- scikit-learn
- imbalanced-learn
- matplotlib
- joblib
