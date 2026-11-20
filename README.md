
# Geländedarstellung und 3D-Datenvisualisierung | WiSe 2026



## EP02 – Geländedarstellung II

<p align="center">
  <img src="https://github.com/user-attachments/assets/9009cabc-e5a9-4a1a-bf26-1ea1e2ab771e" width="900" alt="Reliefkarte der Schweiz">
</p>

### Umsetzung der Methode

Grundlage ist ein digitales Höhenmodell (**DEM**) aus dem **ArcGIS Living Atlas**, das auf die Landesgrenzen der Schweiz zugeschnitten wurde. In **ArcGIS Pro** wurden das DEM und eine Schummerung (**Hillshade**) mit angepassten Farb- und Transparenzwerten nach den **Imhof-Farbparametern** miteinander kombiniert.

Durch die Überlagerung der Höheninformationen mit der Schummerung entsteht eine plastische Reliefdarstellung, die die Geländeformen und Höhenunterschiede der Schweiz hervorhebt.

---

## EP03 – Höhenschichten und Isolinien (Berlin)

<p align="center">
  <img src="https://github.com/user-attachments/assets/f04be1ff-f6be-4c97-955c-5be819d1b030" width="900" alt="Höhenschichten und Isolinien Berlin">
</p>

### Umsetzung der Methode

Grundlage ist das digitale Höhenmodell `Berlin_DEM_Focal_10.tif`, das das Berliner Stadtgebiet abbildet. In **ArcGIS Pro** wurden mithilfe des Werkzeugs **Konturlinien (Contour)** Höhenlinien aus dem Raster erzeugt und die Höheninformationen in abgestuften Höhenschichten visualisiert.

Die Abstufungen machen die geringen Höhenunterschiede und leichten Erhebungen im ansonsten weitgehend flachen Berliner Stadtgebiet sichtbar.

---

## EP03 – Reliefkarte Berlin/Brandenburg nach historischer Vorlage

<p align="center">
  <img src="https://github.com/user-attachments/assets/84c2c293-a4b1-480b-a290-eaf0f72da6b0" width="900" alt="Reliefkarte Berlin und Brandenburg">
</p>

### Umsetzung der Methode

Ziel der Übung war es, eine gedruckte Reliefkarte des Landes Brandenburg im Maßstab 1 : 500.000 mit **ArcGIS Pro** nachzubilden. Als Datengrundlage diente das **SRTM-Höhenmodell**, das auf die Landesgrenzen Brandenburgs zugeschnitten wurde.

Die Geländedarstellung entstand durch die Kombination aus **hypsometrischen Höhenschichten**, **Schummerung (Hillshade)** und **Isolinien** vor einer dezenten Hintergrundkarte.

Durch die Kombination dieser Darstellungsformen treten auch feinere eiszeitlich geprägte Geländeformen wie Urstromtäler, Seenplatten und der Fläming plastisch hervor.

---

## EP05 – Illuminated Choropleth Maps

<p align="center">
  <img src="https://github.com/user-attachments/assets/5fe55d80-7c2b-44fa-b259-f54d525566b1" width="900" alt="Illuminated Choropleth Map Berlin">
</p>

### Umsetzung der Methode

Grundlage sind die Berliner LOR-Daten aus dem Monitoring Soziale Stadtentwicklung (`berlin_LOR_MSS_2025`). Dargestellt wird der Indikator **Arbeitslosigkeit (S1)** vor einer dunklen Grundkarte.

In **ArcGIS Pro** wurden die Gebiete in fünf Farbklassen eingeteilt und ohne Umrisslinien dargestellt. Um einen räumlichen Effekt zu erzeugen, wurden die Attributwerte über den Ausdruck `!S1!*20` als Höheninformationen in ein 10-m-Raster übertragen. Auf dieser Grundlage wurde anschließend eine **Schummerung (Hillshade)** berechnet.

Durch die Kombination aus thematischer Farbgebung und Schummerung entsteht eine plastische Choroplethenkarte, die die räumlichen Unterschiede der Arbeitslosigkeit zwischen den Berliner Kiezen hervorhebt.

---

## EP05 – Spike Map (Berlin)

<p align="center">
  <img src="https://github.com/user-attachments/assets/d0c1c5c9-7cf2-483e-b773-f09705fbdaa5" width="900" alt="Spike Map Berlin">
</p>

### Umsetzung der Methode

Grundlage sind ebenfalls die Berliner LOR-Daten aus dem Monitoring Soziale Stadtentwicklung (`berlin_LOR_MSS_2025`). Dargestellt wird der Indikator **Arbeitslosigkeit (S1)**.

Zunächst wurden die Gebietsflächen auf 80 % Transparenz gesetzt und mithilfe des Werkzeugs **Feature in Punkt** durch ihre Mittelpunkte repräsentiert. Anschließend wurden ausgehend von einer dreieckigen Grundform und dem geladenen Style *Granitspike* über datengesteuerte Symbolisierungseffekte dreidimensionale Spitzen erzeugt.

Die Höhe der Spikes wird über den Maßstab der Y-Achse durch den jeweiligen `S1`-Wert gesteuert. Ein vertikaler Offset (Verschieben entlang der Y-Achse) sorgt dafür, dass die Basis der Spikes auf den jeweiligen Gebietspunkten bleibt. Zusätzlich erfolgt eine farbliche Abstufung anhand des Indikators `S1`.

Durch die Kombination aus Spitzenhöhe und Farbgebung lassen sich räumliche Schwerpunkte der Arbeitslosigkeit im Berliner Stadtgebiet erkennen.

---

## EP07 – Local Scenes: 3D-Gebäudemodell (Columbiahalle)

<p align="center">
  <img src="https://github.com/user-attachments/assets/6c7088fa-9cfd-4a4a-b618-4a34420de444" width="900" alt="3D-Gebäudemodell Columbiahalle">
</p>

### Umsetzung der Methode

Für das 3D-Stadtmodell rund um die **Columbiahalle** wurden Gebäudehöhen aus dem **Berliner Umweltatlas** über einen WFS-Dienst eingebunden und auf den Untersuchungsbereich eingegrenzt. Die Daten wurden anschließend in das einheitliche Koordinatensystem **EPSG:25833** überführt.

In einer lokalen 3D-Szene von **ArcGIS Pro** erfolgte die Höhenextrusion der Gebäudegrundrisse anhand des Attributs `hoehe`. Zusätzlich wurden die Gebäude entsprechend ihrer Nutzung (`funktion_t`) thematisch eingefärbt. Beleuchtung und Schattenwurf ergänzen die Darstellung vor einer topografischen Grundkarte mit 3D-Bäumen.

Durch die Kombination aus Gebäudehöhen, Nutzungsdifferenzierung und Licht- und Schatteneffekten werden die Gebäudekubaturen und Höhenunterschiede rund um den Columbiadamm räumlich sichtbar.

---

## EP07 – 3D-Prismenkarte: Soziale Stadtentwicklung (Berlin)

<p align="center">
  <img src="https://github.com/user-attachments/assets/b26cd83e-d828-4813-9929-19b44d2498fa" width="900" alt="3D-Prismenkarte soziale Stadtentwicklung Berlin">
</p>

### Umsetzung der Methode

Grundlage sind die Berliner LOR-Gebiete (`outputLayer` aus EP01), die in einer **3D-Szene** von **ArcGIS Pro** visualisiert wurden. Dabei werden zwei soziale Indikatoren miteinander kombiniert: Die Farbe der Prismen repräsentiert die **Statusklasse (SK)**, während ihre Höhe über den skalierten Indikator **Kinderarmut (S4)** gesteuert wird. Hierfür wurde der Ausdruck `$feature.S4*100` verwendet.

Im Gegensatz zu einer klassischen Geländedarstellung basieren die Höhen der Prismen somit nicht auf tatsächlichen Geländehöhen, sondern auf den jeweiligen Attributwerten.

Durch die Kombination aus Farb- und Höhenunterschieden lassen sich räumliche Zusammenhänge zwischen dem sozialen Status und der Kinderarmut in den Berliner Kiezen erkennen.



