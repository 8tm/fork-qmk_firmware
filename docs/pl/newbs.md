# Poradnik QMK :id=the-qmk-tutorial

Twoja Klawiatura komputerowa zawiera w sobie procesor podobny do tego, który znajduje się w komputerze.
Ten procesor uruchamia oprogramowanie, które odpowiada za wykrywanie naciśnięć przycisków i informowanie komputera o wciśnięciu klawiszy.
Firmware QMK pełni rolę tego oprogramowania, wykrywając naciśnięcia przycisków i przekazując tę informację do komputera.
Kiedy tworzysz własne mapowanie klawiszy, tworzysz program wykonywalny dla swojej klawiatury.

QMK stara się oddać wiele możliwości w twoje ręce ułatwiając proste zadania i umożliwiając tworzenie trudnych zadań.
Nie musisz znać się na programowaniu, aby stworzyć potężne mapowanie klawiszy - wystarczy, że będziesz przestrzegać kilku prostych reguł składniowych.

Nie jesteś pewny, czy twoja klawiatura może uruchomić QMK?
Jeśli to mechaniczna klawiatura, którą zbudowałeś sam, to są dużeszanse, że może.
Wspieramy [wiele klawiatur hobbystycznych](https://qmk.fm/keyboards/).
Jeśli Twoja obecna klawiatura nie może uruchomić QMK, istnieje wiele dostępnych opcji dla płyt, które to umożliwiają.


?> **Czy ten przewodnik jest dla mnie?**<br>
Jeśli myśl o programowaniu cię przeraża, zajrzyj proszę na naszą [stronę z GUI online](pl/newbs_building_firmware_configurator.md).

## Przegląd :id=overview

Ten przewodnik jest odpowiedni dla wszystkich, którzy chcą budować oprogramowanie klawiatury, korzystając z kodu źródłowego.
Jeśli jesteś już programistą, zauważysz, że proces będzie dla Ciebie bardzo znajomy i łatwiejszy do śledzenia.
Przewodnik ten składa się z trzech głównych sekcji:


1. [Konfiguracja środowiska](pl/newbs_getting_started.md)
2. [Tworzenie pierwszego oprogramowania układowego](pl/newbs_building_firmware.md)
3. [Wgrywanie oprogramowania układowego](pl/newbs_flashing.md)

Ten przewodnik skupia się na pomocy osobie, która nigdy wcześniej nie kompilowała oprogramowania.
Dokonuje wyborów i rekomendacji zgodnie z tym punktem widzenia.
Istnieją alternatywne metody dla wielu z tych procedur, i wspieramy większość z tych alternatyw.
Jeśli masz jakiekolwiek wątpliwości co do tego, jak wykonać jakieś zadanie, możesz [poprosić nas o wskazówki](pl/getting_started_getting_help.md).

## Dodatkowe zasoby :id=additional-resources

Poza tym przewodnikiem istnieje kilka dodatkowych zasobów, które mogą być pomocne podczas nauki QMK.
Zebraliśmy je na stronach [Sylabus](pl/syllabus.md) i [Inne zasoby](pl/newbs_learn_more_resources.md).
