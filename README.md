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

Grundlage ist eine **Choroplethenkarte** für **Berlin** mit abgestuften Grün- und Beigetönen vor einer dunklen Grundkarte. In **ArcGIS Pro** wurde die Flächenklassifikation mit einer **Schummerung / Beleuchtungswirkung (Illumination / Hillshade)** kombiniert, um den teilflächenbezogenen Werten räumliche Tiefe zu verleihen.

Durch die Kombination aus Farbabstufung und Beleuchtungseffekt treten kleinräumige Unterschiede zwischen den einzelnen Gebieten Berlins plastischer hervor als bei einer klassischen flachen Choroplethenkarte.

EP06 | Spike Maps

<img width="705" height="329" alt="S1_berlin_SpikeMaps" src="https://github.com/user-attachments/assets/b9aceb1e-95e8-47c6-a668-94d6d4a49c91" />

EP07 | Local Scenes in ArcGIS Pro

<img width="3508" height="2480" alt="columbiahalle_3D" src="https://github.com/user-attachments/assets/095f71e5-0942-45ee-90e1-70e068e9db02" />



