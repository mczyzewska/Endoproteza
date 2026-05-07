# 🦴 Endoproteza Kości Ramiennej — Modelowanie Implantów Układu Mięśniowo-Szkieletowego

> **Projekt akademicki · Inżynieria Biomedyczna · 2026**  
> Wizualizacja endoprotezy zastosowanej w obszarze resekcji kości ramiennej z wypełnieniem strukturą Woronoja.

---

## 📋 Opis projektu

Celem było zaprojektowanie endoprotezy dopasowanej do indywidualnego przypadku klinicznego, obejmującego zmianę nowotworową lewej kości ramiennej.

### Scenariusz kliniczny

> Pacjentka posiada **zmiany nowotworowe o średnicy 5 cm** zlokalizowane w części trzonowej **lewej kości ramiennej**, na powierzchni przednio-przyśrodkowej — w miejscu przyczepu mięśnia *kruczo-ramiennego* oraz mięśnia *ramiennego*. Zmiana nacieka na kość i ją otacza.

---

## 🔬 Metodologia

### 1. Segmentacja danych medycznych
- Wyodrębnienie **lewej kości ramiennej** z danych DICOM
- Oczyszczenie siatki, wygładzenie i wypełnienie ubytków
- Eksport do formatu `.stl` z zachowaniem skali anatomicznej
- Naniesienie wymiaru kalibrującego w wybranej płaszczyźnie

### 2. Import i weryfikacja skali (Autodesk Fusion)
- Import modelu `.stl` do nowego projektu w Autodesk Fusion
- Weryfikacja wymiarów anatomicznych na podstawie wymiarów kalibrujących
- Korekta ewentualnych błędów skalowania powstałych przy konwersji z DICOM

### 3. Planowanie resekcji onkologicznej
- Wyznaczenie obszaru zmiany nowotworowej na powierzchni przednio-przyśrodkowej trzonu
- Zastosowanie **rozszerzonego marginesu resekcyjnego** według współczynnika **×1,5**
- Wykonanie wirtualnej resekcji fragmentu kości w środowisku CAD

### 4. Projektowanie endoprotezy — wypełnienie Woronoja
- Zastosowanie odpowiednich narzędzi w celu dopasowania siatki Woronoja do geometrii obszaru resekcji
- Skalowanie i multiplikacja struktury z zachowaniem równowagi między:
  - wytrzymałością mechaniczną
  - lekkością i porowatością sprzyjającą osteointegracji
  - stabilnością i dopasowaniem do ubytku kostnego

---

## 📁 Struktura repozytorium

```
.
├── Kość_z_wypełnieniem_woronoja.stl   # Finalny model 3D — kość z endoprotezą (do druku)
├── Kość_z_wypełnieniem_woronoja.obj   # Eksport OBJ (do wizualizacji i renderingu)
├── Kość_z_wypełnieniem_woronoja.mtl   # Definicje materiałów dla pliku OBJ
└── README.md
```

---

## 🖼️ Podgląd modelu

> *Plik `.obj` można otworzyć w programach MeshLab, Blender lub dowolnej przeglądarce modeli 3D w celu inspekcji geometrii implantu.*

---


### Struktura Woronoja — uzasadnienie wyboru

Struktura Woronoja została wybrana zamiast litego wypełnienia, ponieważ:

- **Osteointegracja** — otwarta geometria porowata sprzyja wrastaniu tkanki kostnej
- **Dopasowanie sztywności** — niższa efektywna sztywność implantu zmniejsza efekt odciążenia kości
- **Efektywność materiałowa** — znacząca redukcja masy w porównaniu do litego implantu tytanowego
- **Zgodność z technologiami druku 3D** — struktura kompatybilna z selektywnym topieniem laserowym metali (SLM)


---

*Projekt stanowi część portfolio akademickiego prezentującego umiejętności z zakresu przetwarzania obrazów medycznych, projektowania implantów w środowisku CAD oraz modelowania biomechanicznego.*
