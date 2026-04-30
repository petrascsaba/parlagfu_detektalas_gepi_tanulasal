# parlagfu_detektalas_gepi_tanulasal
Parlagfű detektálása Sentinel–2 műholdfelvételek, vegetációs indexek és gépi tanulási módszerek alkalmazásával.

# Parlagfű detektálása Sentinel–2 idősorok és gépi tanulás alapján

Ez a repository a diplomamunkámhoz kapcsolódó Python-alapú feldolgozási munkafolyamatot tartalmazza, amely az ürömlevelű parlagfű (*Ambrosia artemisiifolia L.*) Sentinel–2 műholdfelvételek alapján történő detektálását vizsgálja.

A módszertan Sentinel–2 L2A műholdképekre, vegetációs indexekre, fenológiai idősorokra és Random Forest osztályozási modellre épül.

## Téma

A kutatás célja annak vizsgálata, hogy Sentinel–2 műholdfelvételek és gépi tanulási módszerek segítségével milyen mértékben azonosíthatók a parlagfűvel fertőzött területek egy Fejér vármegyei mintaterületen.

A feldolgozás során több időpontból származó Sentinel–2 felvételek alapján vegetációs indexek és idősor-alapú statisztikai jellemzők kerültek előállításra, majd ezek felhasználásával Random Forest modell készült a parlagfű jelenlétének pixelalapú becslésére.

## Főbb feldolgozási lépések

A repositoryban szereplő notebookok és scriptek az alábbi főbb lépéseket dokumentálják:
