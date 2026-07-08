# Desktop Power Supply (LM317)

![3D Render](Documentation/Images/3d_render_2.jpg)

## O projekcie

**Desktop Power Supply** to kompaktowy, biurkowy zasilacz warsztatowy oparty na popularnym i niezawodnym stabilizatorze liniowym LM317. 

Projekt ten powstał z myślą o stworzeniu prostego, taniego i wygodnego źródła zasilania o regulowanym napięciu, idealnego do prototypowania na płytkach stykowych i testowania mniejszych układów elektronicznych. Całość została zaprojektowana tak, aby zajmowała jak najmniej miejsca na biurku, a jednocześnie oferowała wszystko, co niezbędne do codziennej pracy hobbysty i inżyniera.

## Główne cechy (Features)

* **Płynna regulacja napięcia:** Wykorzystanie układu LM317 oraz precyzyjnego potencjometru pozwala na łatwe dostosowanie napięcia wyjściowego do potrzeb testowanego układu.
* **Wbudowany woltomierz (Mini Digital LCD):** Zintegrowany wyświetlacz pozwala na bieżący, wygodny odczyt ustawionego napięcia bez konieczności podłączania zewnętrznego multimetru.
  * *Uwaga projektowa:* Footprint (obrys) modułu woltomierza LCD został przygotowany na podstawie ogólnodostępnej dokumentacji. Przed docelową produkcją PCB i montażem elementu, zalecam zakupienie fizycznego modułu i ostateczną weryfikację rozstawu otworów montażowych oraz padów.
* **Wygodny interfejs:** Standardowe gniazdo zasilania DC Jack na wejściu, główny włącznik zasilania (Power ON/OFF) z czerwoną diodą LED sygnalizującą status pracy oraz wielokrotne wyprowadzenia wyjściowe na złączach szpilkowych (goldpin).
* **Zarządzanie termiczne:** Liniowe stabilizatory napięcia wydzielają ciepło przy dużych różnicach napięć. W projekcie świadomie przewidziano odpowiednią ilość miejsca na montaż aluminiowego radiatora dla układu LM317, co jest mocno zalecane dla stabilnej pracy pod obciążeniem.

## Specyfikacja techniczna i układ PCB

Podczas projektowania płytki w programie KiCad, skupiłem się na optymalizacji ścieżek prądowych oraz odpowiednim rozprowadzaniu ciepła.

* **Wymiary płytki:** Bardzo kompaktowy format – 55 mm x 36 mm.
* **Ścieżki zasilające (0,8 mm):** Zważywszy na to, że jest to moduł zasilacza, zdecydowana większość ścieżek przewodzi główne zasilanie. Ich szerokość została znacznie zwiększona (0,8 mm), aby bezpiecznie przewodzić prądy wymagane przez zasilane układy i zminimalizować spadki napięć.
* **Ścieżki sygnałowe (0,25 mm):** Węższe ścieżki zastosowane wyłącznie dla mniej obciążonych linii (np. sygnał pomiarowy dla woltomierza).
* **Wylewki masy (Ground Planes):** Zastosowałem solidne wylanie masy (poligony GND) na obu warstwach (Top i Bottom). Zapewnia to dobrą płaszczyznę powrotu dla prądu, redukuje szumy, a także pełni rolę dodatkowego radiatora rozpraszającego ciepło z komponentów.

## Schemat ideowy

![Schematic](Documentation/Images/schematic_2.png)

## Projekt PCB (Pcbnew)

Poniżej znajduje się podgląd gotowego projektu obwodu drukowanego, obrazujący optymalizację ścieżek prądowych.

![PCB View](Documentation/Images/PCB_2.PNG)

**Górna warstwa (Top Layer):**
![PCB Top Layer](Documentation/Images/PCB_r_2.PNG)

**Dolna warstwa (Bottom Layer):**
![PCB Bottom Layer](Documentation/Images/PCB_b_2.PNG)

## Wykaz elementów (BOM)

Aby ułatwić proces zamawiania części i lutowania, przygotowałem interaktywny wykaz elementów (BOM).

👉 **[Kliknij tutaj, aby otworzyć interaktywny BOM](TUTAJ_WKLEJ_SWOJ_LINK_Z_GITHUB_PAGES)**

---
*Projekt wykonany w programie KiCad.*