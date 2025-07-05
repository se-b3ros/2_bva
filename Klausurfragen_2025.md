# BVA Klausurfragen 2025

## 0.Overview [5]

0.1 Wie kann man ein überbestimmtes Gleichungssystem lösen. Erläutern Sie die erforderlichen Schritte. Formen Sie die Gleichungen für ein konkretes BSP um, sodass via Matrix + Falk-Schema lösbar. Welche Vor- und Nachteile besitzt diese Strategie des Gleichungslösens?

0.2 Geben Sie eine (eigene) Definition für Computer Vision. Welche Disziplinen sind mit welchen Konzepten/Algorithmen involviert?

0.3 Was sind klassische Anwendungsgebiete der Computer Vision?

0.4 Welche Bildeigenschaften sind für die menschliche Wahrnehmung relevant?

0.5 Skizzieren Sie Computer Vision mit den relevantesten Verfahren grob als Wissenslandkarte.


---
## 1.Linear Imaging Systems [9]

1.1 Rotation in 2D: welche zwei Möglichkeiten gibt es hierfür? Fertigen Sie eine Skizze an. 

1.2: Wie viele Rotationswinkel gibt es in 3D. Wie groß Matrix für Translation, Rotation, Skalierung in 3D. Warum 4x4. Wo kommt fehlende 4-te Koordinate in 3D her? Sind affine Transformationen kommutativ? Zeigen Sie anhand eines 2D Beispiels mit Rot/Trans, dass NICHT kommutativ.

1.3 Intrinsische vs. Extrinsische Rotation, d.h. Objekt- bzw. Koordinatensystem-bezogen. Vgl. Vor und Nachteile. Welche Eigenheit gibt es bei der Überführung von extrinsisch nach intrinsisch (Rot-Reihenfolge dreht sich um)

1.4 Was bedeutet Kamera-Kalibrierung? Wo liegen die Anwendungsgebiete und welche generellen Einschränkungen können Abbildungssystemen anhaften (distortion, keine echten Farben, usw.)

1.5 Warum kommt es bei der Camera Obscura zu Unschärfe? Fertigen Sie eine Skizze an und diskutieren Sie wovon es abhängt, dass ein Bild mittels Camera Obscura vergrößert oder verkleinert wird. Konnex zu adaptiven Filtern zwecks Korrektur

1.6 Welche intrinsischen und extrinsischen Parameter als Matrizeninhalte sind bei der Kamera-Kalibrierung zu lösen? Beschreiben Sie jeden der Parameter. Warum gibt es 2 Parameter für die Fokuslänge (x,y)? Durch welche weiteren Parameter kann eine Verzerrungskorrektur erfolgen?

1.7 Welche grundlegenden 3 geometrischen Probleme können mittels Kamera Kalibrierung gelöst werden? Erläutern Sie ev. mit Skizze.

1.8 Beschreiben Sie den Verfahrensablauf bei der Kalibrierung einer Kamera (Schachbrett-Muster).

1.9 Erläutern sie grob, wie die Gleichungen zur Kalibrierung einer Kamera definiert und gelöst werden können. Ev. mit Skizze.


---
## 2. Segmentation and Classification [8]

2.1 Differenzieren Sie die Begriffe Klassifikation, Segmentierung und Lokalisierung für ein BSP mit 1-N Objekten.

2.2 Wie kann man mittels MeanShift eine Vorsegmentierung bewirken, wie mittels KMeans Clustering + Quantisierung/Region Labelling, wie mittels Anisotroper Diffusion + Quantisierung/Region Labelling? Vergleichen Sie und erläutern Sie kurz.

2.3 Erläutern Sie kurz Graph Cut / Grab Cut. BG und FG-Wurzeln im Graph, Kantengewichte und Schnitt. Wie kann mittels Benutzerinteraktion ein verbessertes Ergebnis bewirkt werden?

2.4 Diskutieren Sie bei der OCR die technischen Hürden für a) die Erkennung von Text-Passagen und b) für die eigentliche Analyse der Buchstaben. Nennen Sie die dafür jeweils notwendigen verfahren.

2.5 Nennen Sie einige relevante Features aus dem Bereich Textur, Geometrie und Transformation. Welche dieser Features können auch im Bereich OCR zur Analyse von binären Buchstaben innerhalb einer region of interest (ROI) verwendet werden? Inwieweit beinhalten klassische Segmentierungsverfahren wie Interval-Threshold oder Region-Growing ebenfalls Features?

2.6 Erläutern Sie das Vorgehen, wenn man OCR „von 0 weg“ eigenständig umsetzen möchte auf Basis von vorsegmentierten Regionen und Featureanalyse für die Klassifikation (vgl. Übung).

2.7 Was sind Haar Cascades? Wie werden sie trainiert und angewandt? Inwieweit ist das Konzept skalierungsinvariant? Führen Sie über die Bedeutung der Haar Cascade im Bereich der

2.8. Nennen und Diskutieren Sie alternative Ansätze zur Gesichtserkennung (historische Verfahren bis hin zu aktuellen Strategien) und charakterisieren Sie dabei jeweils die Vor- und Nachteile.

 
---
## 3. Image Restauration [5]

3.1 Erläutern Sie die Idee der Anisotropen Diffusion mit eigenen Worten. Was bedeutet die lokale Diffusionszahl ? Was bedeutet K? Wird c für jedes Pixel individuell berechnet?  Wird K für jedes Pixel individuell berechnet?  Wie viele Gradientenrichtungen sind für jedes Pixel zu betrachten?

3.2 Was bedeutet „image degradation“. Filterung im Ortsraum vs. Frequenzraum. Sehen Frequenz-Spektren von natürlichen Bildern ähnlich aus? Wie kann man das nun zur Beseitigung von Störsignalen nützen? Warum muss bei der „deconvolution“ im Falle von Rauschen der hohe Frequenzbereich abgeschwächt werden (Skizze).

3.3 Die Wiener-Deconvolution kann mittels Wiener-Filterkern erfolgen, wobei K welche Bedeutung zukommt? ( Abschätzung des Signal-Rausch-Verhältnis). Wie kommt man zu K? Wie vereinfacht sich die Wiener-Deconvolution, wenn kein Rauschen im Bild vorhanden ist.

3.4 Muss bei der Richardson-Lucy-Deconvolution der Faltungskernel bekannt sein, der das Störsignal verursacht? Erläutern Sie in eigenen Konzepten grob, wie mittels RLD ein verzerrtes Bild wieder rekonstruiert werden kann.

3.5 Was bedeutet Image Superresolution? Nennen Sie unterschiedliche Strategien und erläutern Sie das Grundprinzip sehr vereinfacht mit eigenen Worten. Wo liegen die Grenzen der Image Superresolution?


---
## 4. Localization [10]

**4.1 Erörtern Sie die Kernidee von VSLAM anhand einer eigenen Skizze und führen Sie in diesem Zusammenhang über die loop closure aus. In welchen Anwendungsdomänen spielt der VSLAM Algorithmus eine zentrale Rolle?**

Visual SLAM verwendet hauptsächlich visuelle Informationen, also Kameradaten, zur simultanen Lokalisierung und Kartierung. Kameras erfassen visuelle Merkmale der Umgebung, und der Algorithmus berechnet daraus die Position des Geräts.

- Ziel: Lokalisierung des Roboters und simultane Erstellung einer Karte der Umgebung.
- Input: Visuelle Sensordaten (monokular/stereo), oft kombiniert mit interner Odometrie.
- Herausforderung: Henne-Ei-Problem — Für die Lokalisierung wird eine Karte benötigt; für die Kartierung wird eine präzise Lokalisierung vorausgesetzt.

**Ablauf und Konzept**
<p float="center">
    <img src="./img/vslam_1.png" width="100" />
    <img src="./img/vslam_2.png" width="100" />
</p>

1. Start: Roboter beginnt bei Pose (0,0); Umgebung ist unbekannt.
2. Bewegung gemäß interner Odometrie (Positionsschätzung), erste Unsicherheiten entstehen.
3. Beobachtung erster Merkmale (z.B. durch SIFT); Position dieser Features ist nur ungenau bekannt.
4. Weitere Bewegung: Fehler in Pose-Schätzung akkumulieren.
5. **Loop Closure:** Ein zuvor gesehenes Merkmal wird erneut erkannt. Dies erlaubt Korrektur von Pfad und Karte durch Optimierung.
    - Führt zu signifikanter Reduktion kumulierter Fehler.
    - Erhöht Vertrauen in die Lokalisierung und die Kartengenauigkeit.
    - Ist entscheidend für globale Konsistenz der Karte.


**Anwendungsdomänen von VSLAM**
- Autonome Fahrzeuge – Navigation ohne GPS, z.B. in Tunneln oder Städten.
- Rettungsroboter – Kartierung unbekannter Gebiete (z.B. Höhlen, eingestürzte Gebäude).
- Haushaltsroboter – Staubsauger, Rasenmäher: systematische Umgebungserfassung.
- Augmented Reality / Virtual Reality – Echtzeitlokalisierung von mobilen Kameras.
- Drohnen / UAVs – Umgebungserkennung für autonome Flugnavigation.

---

**4.2 Hough-Transformation von Linien (konventionelle Geradengleichung – keine Polarkoordinaten): Linie im Ortsraum wird zu Punkt im Parameterraum. Geradengleichung + Skizze. Wie kann nun damit eine Linie als lokales Max. im Parameterraum detektiert werden (Skizze)**

Ein Punkt im Ortsraum $(x_0, y_0)$ entspricht einer Geraden im Parameterraum $(m, b)$, gemäß:

  $$
  b = -x_0 \cdot m + y_0
  $$

* Für jedes Pixel im Bild (Ortsraum) wird diese Gleichung genutzt, um alle möglichen Geraden zu berechnen, die durch diesen Punkt verlaufen könnten -> **je ein Linienzug im Parameterraum**.

* **Im Parameterraum**:
  * Wenn sich viele dieser Linien in einem Punkt schneiden, bedeutet das, dass mehrere Pixel im Bild auf derselben Linie im Ortsraum liegen.
  * Der Schnittpunkt ist ein lokales Maximum im Akkumulator, das eine detektierte Linie repräsentiert.

<p float="center">
    <img src="./img/hough_line_detection.png" width="600" />
</p>

---

**4.3 Welche Parameter sind bei der Darstellung von Kreisen im Parameterraum sinnvoll.**

Ein Kreis im Ortsraum wird durch folgende Parameter beschrieben:
* $a, b$: Mittelpunkt des Kreises
* $r$: Radius


**Wie manifestiert sich ein Punkt dabei im Parameterraum?**

Punkt im Ortsraum -> Kreis im Parameterraum:

* Ein einzelner Bildpunkt $(x_0, y_0)$ könnte auf vielen möglichen Kreisen liegen.
* Für jeden möglichen Radius $r$ ergibt sich eine Kreislinie im Parameterraum (a, b), auf der der Mittelpunkt (des Kreises aus dem Ortsraum) liegen müsste.
* Das heißt: **Ein Punkt im Ortsraum wird zu einer Kreislinie im Parameterraum**.

**Wie sind dadurch Kreise zu detektieren? Ev. BSP**

* Für viele Punkte im Bild (z. B. Kantenpunkte): Berechne alle möglichen Kreismittelpunkte für feste Radien.
* Im **dreidimensionalen Parameterraum $(a, b, r)$**:

  * Viele Punkte erzeugen viele Kreislinien.
  * Wo sich viele dieser Linien schneiden, liegt ein lokales Maximum -> ein echter Kreis ist erkannt.

<p float="center">
    <img src="./img/hough_circle_detection.png" width="600" />
</p>

---

**4.4 Warum wird die Generalized Hough Transformation benötigt?**

Die normale Hough-Transformation funktioniert nur bei einfachen Formen (Linien, Kreise). Für beliebige Formen (z. B. komplizierte Konturen) braucht man die generalizierte Hough Transformation.

**Wie wird die R-Tabelle errechnet? Hat die R-Tabelle die Bedeutung eines „Form-Modelles“?**

* Ein **Referenzpunkt** $P_c = (X_c, Y_c)$ wird gewählt (z. B. Mittelpunkt).
* Für jeden **Konturpunkt** $P_i = (X_i, Y_i)$:

  * Berechne den Abstand $r_i$ zum Referenzpunkt.
  * Bestimme die Kantenrichtung $\phi$ (z. B. mit Sobel-Operator).
  * Berechne den Winkel $\alpha_i$ zwischen $P_i$ und $P_c$.
* Die Werte $(r_i, \alpha_i)$ werden in der R-Tabelle nach Winkel $\phi$ sortiert gespeichert.

Ja, die R-Tabelle ist das Modell der Form.

<p float="center">
    <img src="./img/hough_general_1.png" width="200" />
    <img src="./img/hough_general_2.png" width="400" />
</p>


**Erhöht sich die Genauigkeit des Modells, wenn mehr Punkte entlang der Kontur in die R-Tabelle verspeichert werden?**

Ja, mehr Punkte in der R-Tabelle = genaueres Modell.


**Was ist die Bedeutung vom Index phi und wie kann man die lokale Steigung der Kontur berechnen.**

φ ist der Winkel der Kante am Konturpunkt (lokale Richtung), berechnet aus dem **Gradienten** ($g_x, g_y$). Damit sucht man passende Vektoren in der R-Tabelle.


**Wie berechnet man die lokale Steigung der Kontur?**
Mit den **x- und y-Gradienten**, z. B. aus dem **Sobel-Filter**:

$$
\phi = \arctan\left(\frac{g_y}{g_x}\right)
$$

**Erlaubt die R-Tabelle das Rekonstruieren von Mittelpunkten ($P_c$) der Form?**
Ja, durch Rückrechnung mit den gespeicherten Werten $(r_i, \alpha_i)$ und dem Winkel $\phi$.

---

**4.5 Was sind gute lokale Features in Bildern und warum?**

Gute lokale Features sind Ecken oder Kanten, also Bildbereiche mit starken Änderungen in mehreren Richtungen. Homogene Flächen sind ungeeignet, da sie keine markanten Merkmale enthalten.

<p float="center">
    <img src="./img/image_features.png" width="400" />
</p>

**Motivieren Sie die Bedeutung von lokalen Features für unterschiedliche Anwendungsdomänen (Panoramafotos, 3D Rekonstruktion, Tracking, Objekterkennung,…).**

Sie helfen, markante Punkte wiederzuerkennen, z. B. für:
- Panoramafotos: Bilder zusammensetzen
- 3D-Rekonstruktion: gleiche Punkte aus verschiedenen Blickwinkeln (mehrere Kameras)
- Tracking: Objektverfolgung über Zeit
- Objekterkennung: bekannte Formen wiederfinden
- Robotik (z. B. visuelle Navigation)


**Welche Anforderungen und Qualitätsindikatoren werden an lokale Features gestellt?**

- Repetitivität: gleiche Punkte zuverlässig finden, auch in mehreren Bildern
- Affine Invarianz: robust gegen Translation, Rotation, Skalierung
- Robustheit: stabil trotz Rauschen, Unschärfe, Helligkeitsänderung
- Unverwechselbarkeit (Distinctiveness): sollte einzigartige Strukturen zeigen
- Ausgewogene Anzahl: genug, um das Bild gut zu beschreiben, aber nicht zu viele
- Effizienz: schnell genug für Echtzeitanwendungen (z. B. Tracking)

---

**4.6 Welche Features werden beim Hessian/Harris Corner Detector erkannt und wie?** 
Beide Verfahren erkennen Ecken, also Punkte mit starkem Intensitätswechsel in mehreren Richtungen.

- Hessian-Detektor: Schaut sich an, wie stark sich Helligkeit in x- und y-Richtung ändert (mit 2. Ableitungen). Wenn sich in beiden Richtungen viel verändert, erkennt er eine Ecke.
- Harris-Detektor: Nutzt 1. Ableitungen (also wie schnell Helligkeit sich ändert) und baut daraus eine Matrix. Wenn sich die Helligkeit in mehreren Richtungen gleichzeitig stark ändert, sind beide Eigenwerte groß, das ist eine Ecke. Die Ecke wird erkannt, wenn ein gewisser Schwellwert überschritten wird.


**Welche Bedeutung haben in diesem Zusammenhang Gradienten, die Hesse Matrix sowie Eigenwerte?**
- Gradienten: Zeigen, wie stark und in welcher Richtung sich die Helligkeit im Bild ändert (1. Ableitungen in x- und y-Richtung). Grundlage für die Eckenerkennung, da Ecken starke Helligkeitswechsel in mehreren Richtungen zeigen.

- Hesse-Matrix (Hessian): Verwendet die 2. Ableitungen der Helligkeit (also wie stark sich der Gradient selbst ändert). Gibt Auskunft darüber, ob die Änderung stark genug ist und in welchen Richtungen Struktur im Bild vorhanden ist. Eine große Determinante der Hesse-Matrix bedeutet, dass sich die Helligkeit in x- und y-Richtung stark ändert -> mögliche Ecke.

- Eigenwerte (bei Harris & Hessian): Zeigen die Stärke der Änderungen in den Hauptachsen (Richtungen) der Matrix.
    - Beide Eigenwerte groß: starke Änderung in zwei Richtungen -> Ecke
    - Ein Eigenwert groß, der andere klein: Kante
    - Beide klein: Fläche ohne Struktur


**Welche Anwendungsdomänen gibt es, bei denen Feature-Detektion essentiell ist?**

- Panoramafotos: Bilder zusammensetzen
- 3D-Rekonstruktion: gleiche Punkte aus verschiedenen Blickwinkeln (mehrere Kameras)
- Tracking: Objektverfolgung über Zeit
- Objekterkennung: bekannte Formen wiederfinden
- Robotik (z. B. visuelle Navigation)


---

**4.7 Was bedeutet scale invariance?**

Scale Invariance (Skalierungsunabhängigkeit) bedeutet, dass ein Feature-Detektor Merkmale erkennt, egal wie groß oder klein das Objekt im Bild erscheint (z.B. durch Entfernung oder Zoom).

Klassische Detektoren wie Harris/Hessian sind nicht scale-invariant. Ein Objekt, das bei kleiner Skalierung ein scharfes Detail zeigt, kann bei größerer Skalierung glatt und unauffällig wirken -> wird dann nicht mehr als Feature erkannt.


**Wie kann man Skalierungsunabhängigkeit erzielen, vgl. Filterpyramide, SIFT etc.**

Lösung: Verwendung von Scale Spaces
-> Bilder werden in verschiedenen Auflösungen (Skalen) betrachtet.

<p float="center">
    <img src="./img/scale_invariance_scale_spaces.png" width="400" />
</p>

1. Filterpyramide: 
- Das Bild wird mehrfach geglättet (durch Gaussian-Filter mit verschiedenen σ) und runterskaliert.
- Feature-Detektion wird auf allen Ebenen wiederholt. So kann man Features in verschiedenen Größen finden.

2. SIFT (Scale-Invariant Feature Transform): Baut einen skalierbaren Bildraum auf, indem das Bild mit verschiedenen Gaussian-Filtern bearbeitet wird. Aus den gefilterten Bildern werden dann Differenzbilder (Difference of Gaussian, DoG) gebildet.


**Erläutern Sie Difference of Gaussian und wie dadurch Skalierungsunabhängigkeit erzielt werden kann.**

DoG ist die **Differenz zweier geglätteter Bilder**, die mit zwei leicht unterschiedlichen Sigma-Werten gefiltert wurden. Man zieht das stärker geglättete Bild vom weniger geglätteten ab.

<p float="center">
    <img src="./img/dog_1.png" width="400" />
</p>

**Warum macht man das?**: Diese Differenz hebt Bereiche hervor, in denen sich die Helligkeit im Bild stark ändert, das sind Kanten oder Ecken.

**Skalierungsunabhängigkeit**:
* Indem man DoG auf verschiedenen Skalen (also für viele verschiedene σ) berechnet, betrachtet man das Bild aus mehreren "Entfernungen".
* Auf kleinen Skalen sieht man feine Details, auf großen Skalen sieht man grobe Strukturen.
* Sucht man nun lokale Maxima oder Minima im Raum aus (x, y, σ), findet man Punkte, die auf allen Skalen gut erkennbar sind. Diese Punkte sind skalierungsinvariant, weil sie nicht von der Größe des Objekts abhängen, sondern von seiner Struktur über Skalen hinweg.

In SIFT nutzt man genau diese DoG-Extrema als stabile Merkmale, die man auch dann wiederfindet, wenn ein Objekt im Bild größer oder kleiner erscheint. So ist der Algorithmus robust gegenüber Zoom oder Entfernung.

---

**4.8 Wie wird bei SIFT der 128-Element Feature-Vektor errechnet.**

1. **Vorbereitung (Steps 1-3):**
SIFT detektiert zunächst stabile Keypoints über mehrere Skalen (DoG-Pyramide), lokalisiert sie präzise und weist jedem Keypoint eine dominante Orientierung zu, um Rotationsinvarianz zu gewährleisten.

2. **Step 4 – Keypoint Description:**
* Um jeden Keypoint wird ein 16x16 Pixel großes lokales Umfeld betrachtet.
* Dieses Umfeld wird in 16 kleine Regionen (4x4 Pixel) aufgeteilt.
* In jeder Region wird ein Histogramm der lokalen Gradientenorientierungen mit 8 Bins erstellt.
* Die Gradientenwerte werden mit einer Gauß-Gewichtung und der Gradientenstärke gewichtet.
* Die 16 Histogramme mit je 8 Werten werden aneinandergereiht -> ergibt den 128-dimensionalen Feature-Vektor (16 x 8 = 128).
* Abschließend wird der Vektor normalisiert, um Beleuchtungsänderungen robust zu begegnen.
    <p float="center">
        <img src="./img/sift_step_4.png" width="300" />
    </p>


**Was bedeutet in diesem Zusammenhang Feature-Trajektorie und wie werden Features diesbezüglich „gematched“?**

Feature-Trajektorie: Die Verbindung eines SIFT-Features aus Bild A mit dem korrespondierenden Feature aus Bild B, also die Zuordnung von Merkmalen zwischen zwei Bildern.

Matching:
* Beim Matching sucht man für jeden Feature-Vektor aus Bild A den ähnlichsten Feature-Vektor aus Bild B (meist mit der euklidischen Distanz).
* Um sicherzugehen, dass die Zuordnung zuverlässig ist, wird der Ratio-Test angewendet: Nur wenn der beste Match deutlich besser ist als der zweitbeste (z.B. mindestens 20% besser), wird die Verbindung akzeptiert.
* So entstehen stabile Feature-Trajektorien zwischen Bildern.



**Angenommen es werden zwei Mengen an SIFT-Features mittels Feature-Trajektorie in Verbindung gesetzt – wie kann die Ergebnisqualität zusätzlich verbessert werden?**

Clusterbildung und Hough-Transform:
* Features, die zusammen ähnliche Bewegungen oder Transformationsparameter (z.B. affine Transformation) aufweisen, werden zu Clustern zusammengefasst.
* Mittels Hough-Transform stimmen die Keypoints über mögliche Objektpositionen und -orientierungen ab.
* Der Cluster mit den meisten "Votes" repräsentiert die wahrscheinlichste Übereinstimmung, was die Zuverlässigkeit gegenüber Ausreißern und falschen Matches deutlich erhöht.

---

**4.9 Erläutern Sie das Histogram of Oriented Gradients (HOG).**

HOG ist ein Verfahren zur Beschreibung von Bildern, das vor allem für die Erkennung von Objekten (z.B. Personen) eingesetzt wird. Es analysiert die Verteilung von Kantenrichtungen in kleinen Bereichen eines Bildes.

**Welche zentralen Features werden hierbei zur Berechnung des L2-normalisierten 36-bin Feature-Vektors herangezogen?**

1. **Gradientenberechnung:**

* Zuerst werden horizontale und vertikale Gradienten mit Sobel-Filtern berechnet.
* Daraus ergeben sich für jeden Pixel die Gradientenstärke (Magnitude) und die Gradientenrichtung.
    <p float="center">
        <img src="./img/hog_1.png" width="200" />
    </p>


2. **Histogramme pro Pixelzelle:**

* Das Bild wird in kleine Zellen von z.B. 8×8 Pixeln unterteilt.
* Für jede Zelle wird ein Histogramm der Gradientenrichtungen berechnet, aufgeteilt in 9 Bins (also 9 Winkelbereiche von 0° bis 180°, da die Gradientenrichtung "unsigned" ist).
    <img src="./img/hog_2.png" width="600" />
* Die Gradienten werden gewichtet nach ihrer Stärke und auf die beiden nächsten Bins verteilt (Interpolation).
    <img src="./img/hog_3.png" width="600" />
    

3. **Block-Normalisierung:**

* Vier benachbarte Zellen (also 2x2 Zellen = 16×16 Pixel) werden zusammengefasst zu einem Block.
* Die 4 Histogramme (je 9 Bins) ergeben einen Vektor mit 36 Werten (4×9).
* Dieser Vektor wird L2-normalisiert (auf die Länge 1 skaliert), um Beleuchtungsunterschiede auszugleichen (beschreibt nur die relative Verteilung der Kantenrichtungen, nicht die absolute Stärke).
    <img src="./img/hog_4.png" width="600" />

4. **Endergebnis:**

* Das Bild wird von vielen solchen Blöcken abgedeckt, und die 36-Element-Vektoren dieser Blöcke werden aneinandergereiht, um den endgültigen HOG-Feature-Vektor zu bilden.


**Wie wird HOG invariant bzgl. affiner Transformationen wie etwa Skalierung, Translation oder Rotation?**

* **Skalierung:**
    Durch Vorverarbeitung wird das Bild auf eine standardisierte Größe skaliert, sodass die Größe der Zellen und Blöcke relativ zum Bild konstant bleibt.

* **Translation (Verschiebung):**
    HOG arbeitet lokal in kleinen Zellen und Blöcken, deshalb verschieben sich die lokalen Histogramme mit dem Bildinhalt mit und bleiben konsistent.

* **Rotation:**
    HOG verwendet „unsigned“ Gradienten (0° bis 180°), wodurch eine 180°-Rotation oder Spiegelung weniger Einfluss auf den Histogrammverlauf hat.


---

**4.10 Erläutern Sie die Bedeutung von Bild-Charakteristika zur Segmentierung/Klassifikation. Warum muss dabei i.d.R. ein Feature-Vektor verwendet werden, um mehrere Klassen in robuster Weise voneinander trennen zu können.**

Man nutzt mehrere Bild-Charakteristika gleichzeitig in einem Feature-Vektor, um verschiedene Klassen zuverlässig voneinander zu trennen, da einzelne Merkmale oft zu ungenau oder irreführend sind. Mehr Merkmale = bessere Unterscheidungskraft.

* **Bild-Charakteristika** sind Merkmale oder Eigenschaften eines Bildes (z.B. Farbe, Textur, Kanten, Form), die helfen, verschiedene Bildbereiche oder Objekte zu unterscheiden.
* Bei der **Segmentierung** werden Bildbereiche in sinnvolle Teile (z.B. Himmel, Boden, Objekte) getrennt.
* Bei der **Klassifikation** wird jedem Bild oder Bildteil eine Kategorie (Klasse) zugewiesen, z.B. „Auto“, „Mensch“ oder „Hintergrund“.

Warum ein Feature-Vektor:
* Ein einzelnes Merkmal (z.B. nur Farbe) ist oft nicht ausreichend, weil verschiedene Klassen sich in einem Merkmal überlappen können.
* Ein Feature-Vektor fasst viele verschiedene Merkmale zusammen (z.B. Farbe, Textur, Form, Kantenmuster). Dadurch kann man besser Unterschiede erkennen.




---

---
## 5. 3D Rekonstruktion [6]

5.1 Nennen Sie Verfahren, um mit einzelnen monokularen Bildern bzw. mehrerer monokularer Bilder Objekte 3D zu rekonstruieren. Vergleichen Sie die Ansätze.

5.2 Nennen Sie Anwendungsgebiete der 3D Rekonstruktion. Geben Sie eine Definition für "3D Rekonstruktion" in eigenen Worten. Erläutern Sie, warum in 2D Bildern die Größe von Objekten nicht ableitbar ist

5.3 Führen Sie über die Größenbestimmung in Bildern via Referenzobjekte aus. Erläutern Sie Shape from Shading.

5.4 Erläutern Sie Deep Depth from Focus. Erläutern Sie Shape from texture / structured light

5.5 Führen Sie über den Einsatz von Deep Learning zur Bestimmung der Tiefe / 3D Form aus.

5.6 Erläutern Sie Stereo Matching und Structure from Motion. Welche Bilder sind dafür gut geeignet? Erläutern Sie die Silhouette Reconstruction.


---
## 6. Computer Vision and Machine Learning [9]

**6.1 Wofür werden Bilddatenbanken als „ground-truth“ benötigt.**

Ground-truth bedeutet die exakte Referenz, also eine genaue, verlässliche "Wahrheit" über Bildinhalte (z.B. korrekte Segmentierung, Klassifikation).

Bilddatenbanken mit Ground-truth werden gebraucht, um:
  * Algorithmen in der Computer Vision zu trainieren und zu testen.
  * Ergebnisse verschiedener Verfahren objektiv zu vergleichen.
  * Zu überprüfen, wie gut eine Methode wirklich arbeitet.

**Welche Daten sind dabei hilfreich (vgl. Bilddaten, Depth-from-Focus, 3D Rekonstruktion).**

* Bilddaten mit genauen Labels (z.B. was ist Objekt, Hintergrund, welche Klasse).
* Depth-from-Focus Daten: zusätzliche Tiefeninformationen, um Objekte besser zu unterscheiden.
* 3D Rekonstruktion: 3D-Modelle oder Volumen helfen, räumliche Strukturen exakt zu erfassen.

---

**6.2 Was sind die Fallstricke bei der Verwendung von Bilddatenbanken?**

* **Begrenzte Realitätsnähe:** Bilddatenbanken zeigen nur einen kleinen Ausschnitt der realen Welt, viele Situationen fehlen.
* **Qualität der Daten:** Ground-truth ist nicht immer korrekt oder vollständig, es gibt Fehler, Lücken und Verzerrungen.
* **Bias:** Bilder können z.B. bevorzugte Blickwinkel (Autos nur von der Seite) oder typische Posen enthalten, was das Training einseitig macht.
* **Redundanz:** Viele Daten enthalten sehr ähnliche oder gleiche Motive, was die Vielfalt einschränkt und Modelle überoptimiert auf diese speziellen Beispiele.
* **Visuelle Herausforderungen:** Probleme wie Schatten, Blendungen, Reflexionen, schlechte Beleuchtung oder Verdeckungen werden oft nicht oder nur unzureichend abgebildet.
* **Unterschiedliche Test- und Realitätsszenarien:** Algorithmen, die in Benchmarks gut abschneiden, können im echten Einsatz stark schlechter sein.

---

**6.3 Wie kann man Datenbanken „anreichern“, wenn nicht genügend Testdaten verfügbar sind?**

1. Datenaugmentation durch Transformationen:

* Bilder spiegeln (horizontal/vertikal)
* Helligkeit, Kontrast oder Farben verändern (z.B. Gamma-Korrektur)
* Affine Transformationen: drehen, verschieben, skalieren, verzerren
* Künstliches Hinzufügen von Rauschen oder Objekten
* Sub-Bilder (Ausschnitte) von wichtigen Bildteilen erstellen
* Ersetzen von Bildteilen, z.B. Gesichter in Videos austauschen
* Einfügen von computergenerierten Bildern (CGI) in bestehende Szenen

2. Automatisches Hinzufügen ähnlicher Bilder aus dem Internet:

* Bilder von Suchmaschinen (Google, Flickr) abrufen
* Automatische Annotation (Labeln) mit wenig manuellem Aufwand durch Ähnlichkeitssuche
* Schrittweise Erweiterung des Datensatzes basierend auf Ähnlichkeit (Feedback-Loop)

3. Transfer Learning mit vortrainierten Deep CNNs:

* Vortrainierte Netzwerke (z.B. auf ImageNet) als Ausgangspunkt nehmen
* Auf kleinere, domänenspezifische Datensätze (z.B. Blumenarten) weitertrainieren (Feinabstimmung)
* Vorteil: Gute Grundkenntnisse werden erweitert, es braucht weniger neue Daten

4. Nutzung von 3D-Modellen zur Generierung von Bildern:

* 3D-Objekte digital rendern (realistische Bilder erzeugen)
* Verschiedene Perspektiven und Posen simulieren (z.B. für Menschen, Fahrzeuge)
* Dadurch kann der Datensatz gezielt und vielfältig erweitert werden

**Was ist diesbezüglich der Vorteil/Nachteil von simulierten [Bild]daten?**

Vorteile von simulierten Bilddaten (z.B. aus 3D-Modellen)

* Kontrollierte Vielfalt: Man kann gezielt verschiedene Ansichten, Posen, Beleuchtungen erzeugen.
* Unbegrenzte Datenmenge: Es können beliebig viele Bilder generiert werden.
* Exakte Annotation: Da alles simuliert ist, sind Labels und Tiefeninformationen perfekt verfügbar.
* Geringerer Aufwand für manuelles Labeln.

Nachteile von simulierten Bilddaten

* Realitätslücke: Simulierte Bilder können von echten Bildern abweichen (Domänenunterschiede).
* Weniger natürliche Variationen: Manche Bildfehler oder Störungen fehlen (z.B. Kamerarauschen, Reflexionen).
* Aufwendige Erstellung: Hochrealistische 3D-Modelle und Rendering benötigen viel Aufwand und Rechenleistung.

---

**6.4 Führen Sie detailliert über Datenaugmentierung sowie Tools zur semi-automatischen Annotation von Bildern aus.**

Datenaugmentierung ist eine Methode, um vorhandene Bilddaten künstlich zu erweitern, indem Variationen der Originalbilder erzeugt werden. Ziel ist es, die Datenmenge zu erhöhen und gleichzeitig die Robustheit von Modellen gegen unterschiedliche Bildvariationen zu verbessern.
* Methoden: Spiegeln, Drehen, Skalieren, Farb- und Kontraständerungen, Rauschen hinzufügen, Zufallsausschnitte.

Semi-automatisch bedeutet:
Der Computer schlägt automatische Annotationen vor, die der Mensch dann korrigiert oder bestätigt.
* Tools: Polygon- oder Bounding-Box-Annotation (LabelMe, LabelImg), Superpixel-Segmentierung, Deep-Learning-Modelle für Vorschläge (Mask R-CNN, CVAT).

---

**6.5 Was ist ein U-NET? Wie würden Sie dabei den Datenfluss mit RNNs bzw. LSTM vergleichen? Welche Vorverarbeitungsschritte sind notwendig, bevor das Eingangssignal (z.B. Bild) dem Input-Layer übergeben werden kann? Welche Auswirkung hat die Wahl der Vorverarbeitung auf das trainierte CNN?**



**6.6 Nennen Sie Anwendungsgebiete für Deep Learning. Differenzieren Sie dabei zwischen Klassifikation und Segmentierung – was sind die Auswirkungen auf die Netzwerkarchitektur (input/output Layer)? Was ist die Schwierigkeit bei der Verarbeitung von Eingangsdaten dynamischer Größe?**



**6.7 Erläutern Sie das Prinzip von GANs und deren Einsatzgebiete.**



**6.8 Diskutieren Sie die Bedeutung und Anwendungsgebiete von Yolo.**



**6.9 Diskutieren Sie die Bedeutung der Vorverarbeitung, wenn Bilddaten in den Eingangstensor überführt werden. Was könnte dabei schiefgehen?**

