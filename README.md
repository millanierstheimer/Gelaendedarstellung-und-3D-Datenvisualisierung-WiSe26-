# Gelaendedarstellung-und-3D-Datenvisualisierung-WiSe26

## **EP02 | Geländedarstellung II**

<img width="3508" height="2480" alt="schweiz_relief" src="https://github.com/user-attachments/assets/9009cabc-e5a9-4a1a-bf26-1ea1e2ab771e" />

### Umsetzung der Methode

Grundlage ist ein digitales Höhenmodell (**DEM**) aus dem **ArcGIS Living Atlas**, zugeschnitten auf die Landesgrenzen der Schweiz vor schwarzem Hintergrund. In **ArcGIS Pro** wurden **DEM und Schummerung (Hillshade)** mit angepassten Farb- und Transparenzwerten nach den **Imhof-Farbparametern** überlagert, um eine realistische Licht- und Schattenwirkung zu erzeugen.


## **EP03 – Höhenschichten & Isolinien (Berlin)**

<img width="3508" height="2480" alt="berlin_contour" src="https://github.com/user-attachments/assets/f04be1ff-f6be-4c97-955c-5be819d1b030" />


### Umsetzung der Methode

Grundlage ist das Raster `Berlin_DEM_Focal_10.tif` für **Berlin** vor dunklem Hintergrund. In **ArcGIS Pro** wurden daraus über das Werkzeug **Konturlinien (Contour)** Höhenlinien/Stufen erzeugt und als abgestufte Höhenschichten visualisiert.

Die Abstufungen machen die flachen Übergänge sowie die leichten Erhebungen im Berliner Stadtgebiet klar erkennbar.

## **EP03 – Reliefkarte Berlin/Brandenburg nach historischer Vorlage**

<img src="https://github.com/user-attachments/assets/84c2c293-a4b1-480b-a290-eaf0f72da6b0" alt="bb_höhenlinien" width="750" />

### Umsetzung der Methode

Ziel der Übung war es, eine gedruckte Reliefkarte des Landes Brandenburg im Maßstab 1 : 500 000 frei in **ArcGIS Pro** nachzubilden. Auf Basis des **SRTM-Höhenmodells** wurde Brandenburg auf seine Landesgrenzen zugeschnitten und über **hypsometrische Höhenschichten**, **Schummerung (Hillshade)** sowie **Isolinien** vor einer dezenten Hintergrundkarte visualisiert.

Durch die Abstufung der Höhenlagen und die Reliefschattierung treten selbst die feinen eiszeitlichen Geländeformen wie Urstromtäler, Seenplatten und der Fläming plastisch hervor.


## **EP05 – Illuminated Choropleth Maps**

<img src="https://github.com/user-attachments/assets/5fe55d80-7c2b-44fa-b259-f54d525566b1" alt="S1_berlin_schummerung" width="750" />

### Umsetzung der Methode

Grundlage sind die Berliner LOR-Daten aus dem Monitoring Soziale Stadtentwicklung (`berlin_LOR_MSS_2025`), dargestellt für die **Arbeitslosigkeit (S1)** vor einer dunklen Grundkarte[cite: 6]. In **ArcGIS Pro** wurden die Gebiete in **5 Farbklassen** ohne Umrisslinien eingeteilt. Damit die Flächen räumlich wirken, wurden die Werte als Höheninformation (`!S1!*20`) in ein `10 m`-Raster umgewandelt und daraus eine **Schummerung (Hillshade)** berechnet.

So entsteht aus einer flachen Datenkarte eine plastische Darstellung, in der man die Unterschiede bei der Arbeitslosigkeit zwischen den Berliner Kiezen deutlich erkennen kann.

## **EP05 – Spike Map (Berlin)**

<img width="705" height="329" alt="S1_berlin_SpikeMaps" src="https://github.com/user-attachments/assets/d0c1c5c9-7cf2-483e-b773-f09705fbdaa5" />

### Umsetzung der Methode

Grundlage sind die Berliner LOR-Daten aus dem Monitoring Soziale Stadtentwicklung (`berlin_LOR_MSS_2025`), dargestellt für die **Arbeitslosigkeit (S1)** vor einer dunklen Grundkarte. In **ArcGIS Pro** wurden die Gebietsflächen auf `80 %` Transparenz gesetzt und über **Feature in Punkt** durch Mittelpunkte repräsentiert. Aus einer dreieckigen Grundform  sowie dem geladenen Style *Granitspike* wurden über datengesteuerte Symbolisierungseffekte Spitzen erzeugt: Über den **Maßstab (Y-Achse)** skaliert die **Höhe der Spikes** mit dem `S1`-Wert, während ein vertikaler **Offset (Verschieben entlang Y)** dafür sorgt, dass die Basis jedes Spikes exakt auf dem jeweiligen Gebietspunkt stehen bleibt statt nach unten zu rutschen. Zusätzlich wurden die Spikes nach dem Indikator `S1` farblich abgestuft.

Durch die Kombination aus Spitzenhöhe und Farbverlauf lassen sich lokale Schwerpunkte der Arbeitslosigkeit im Berliner Stadtgebiet auf einen Blick ablesen.

## **EP07 – Local Scenes: 3D-Gebäudemodell (Columbiahalle)**

<img src="https://github.com/user-attachments/assets/DEIN-BILD-LINK" alt="columbiahalle_3D" width="750" />

### Umsetzung der Methode

Für das 3D-Stadtmodell rund um die **Columbiahalle** wurden die Gebäudehöhen aus dem **Berliner Umweltatlas** über einen **WFS-Dienst** angebunden, auf den Zielbereich eingegrenzt und im einheitlichen Koordinatensystem **EPSG:25833** aufbereitet. In einer **lokalen 3D-Szene** von **ArcGIS Pro** erfolgte anschließend die **Höhenextrusion** der Grundrisse anhand des Attributs `hoehe` sowie die thematische Einfärbung nach Gebäudenutzung (`funktion_t`) mit **Beleuchtung und Schattenwurf** vor einer topografischen Grundkarte mit 3D-Bäumen.

Durch die Verbindung von Höhenextrusion, Nutzungsdifferenzierung und Licht-/Schattenwirkung lassen sich die Gebäudekubaturen und Höhenunterschiede rund um den Columbiadamm räumlich erkennen.



