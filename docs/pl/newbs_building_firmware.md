# Budowanie Twojego Pierwszego Firmware :id=building-your-first-firmware

Teraz, kiedy skonfigurowałeś swoje środowisko do budowy, jesteś gotowy, aby rozpocząć budowanie niestandardowego oprogramowania.
W tej części przewodnika będziemy się poruszać pomiędzy 3 programami - menedżerem plików, edytorem tekstu i oknem terminala.
Zachowaj wszystkie 3 otwarte, dopóki nie będziesz zadowolony z oprogramowania dla swojej klawiatury.

## Skonfiguruj domyślne ustawienia środowiska budowy (opcjonalne) :id=configure-your-build-environment-defaults-optional

Możesz skonfigurować środowisko budowy, aby ustawić domyślne wartości i ułatwić pracę z QMK.
Zróbmy to teraz!

Większość nowych użytkowników QMK posiada tylko 1 klawiaturę.
Możesz ustawić tę klawiaturę jako domyślną za pomocą polecenia `qmk config`.
Na przykład, aby ustawić domyślną klawiaturę na `clueboard/66/rev4`:

    qmk config user.keyboard=clueboard/66/rev4

?> Wybrana klawiatura to ścieżka względna do katalogu klawiatury, powyższy przykład znajduje się w `qmk_firmware/keyboards/clueboard/66/rev4`.
Jeśli nie jesteś pewien, możesz wyświetlić pełną listę obsługiwanych klawiatur za pomocą polecenia `qmk list-keyboards`.

Możesz także ustawić nazwę domyślnej mapy klawiszy.
Większość osób używa swojej nazwy użytkownika na GitHubie jako nazwy mapy klawiszy z poprzednich kroków:

    qmk config user.keymap=<github_username>

## Utwórz nową mapę klawiszy :id=create-a-new-keymap

Aby utworzyć własny układ klawiszy, utworzyć kopię mapy klawiszy `default`.
Jeśli skonfigurowałeś swoje środowisko budowania w ostatnim kroku, możesz to łatwo zrobić za pomocą interfejsu wiersza poleceń QMK CLI:

    qmk new-keymap

Jeśli nie skonfigurowałeś swojego środowiska lub masz wiele klawiatur, możesz określić nazwę klawiatury:

    qmk new-keymap -kb <keyboard_name>

Spójrz na wynik z tego polecenia, powinieneś zobaczyć coś w tym rodzaju:

    Ψ Created a new keymap called <github_username> in: /home/me/qmk_firmware/keyboards/clueboard/66/rev3/keymaps/<github_username>.

To jest lokalizacja twojego nowego pliku `keymap.c`.

## Otwórz `keymap.c` w ulubionym edytorze tekstu :id=open-keymapc-in-your-favorite-text-editor

Otwórz plik `keymap.c` w swoim edytorze tekstu.
Wewnątrz tego pliku znajdziesz strukturę kontrolującą zachowanie twojej klawiatury.
Na początku pliku `keymap.c` mogą znajdować się pewne definicje i enumeracje, które ułatwiają czytelność mapy klawiszy.
Dalej znajdziesz linię wyglądającą tak:

    const uint16_t PROGMEM keymaps[][MATRIX_ROWS][MATRIX_COLS] = {

Ta linia wskazuje, gdzie zaczyna się lista warstw (layers).
Poniżej znajdziesz linie zawierające `LAYOUT`, które wskazują początek warstwy.
Poniżej tej linii znajduje się lista klawiszy, które składają się na daną warstwę.

!> Podczas edycji pliku z mapą klawiszy uważaj, aby nie dodawać ani nie usuwać żadnych zbędnych przecinków.
Jeśli tak zrobisz, uniemożliwisz kompilację oprogramowania, a znalezienie dodatkowego lub brakującego przecinka może być trudne.

## Dostosuj LAYOUT do swoich potrzeb :id=customize-the-layout-to-your-liking

To jak zrealizujesz ten krok, zależy wyłącznie od ciebie.
Dokonaj jednej zmiany, która cię irytuje, lub całkowicie przekształć wszystko.
Możesz usuwać warstwy, jeśli nie potrzebujesz wszystkich, lub dodawać nowe warstwy, łącznie do maksymalnie 32.
W QMK jest wiele funkcji, przejrzyj pasek boczny po lewej stronie pod "Korzystanie z QMK", aby zobaczyć pełną listę.
Abyś mógł już zacząć, poniżej jest podanych kilka łatwiejszych w użyciu funkcji:

* [Podstawowe kody klawiszy](pl/keycodes_basic.md)
* [Kody klawiszy Quantum](pl/quantum_keycodes.md)
* [Funkcja Grave Escape](pl/feature_grave_esc.md)
* [Klawisze myszy](pl/feature_mouse_keys.md)

?> Podczas gdy zdobywasz doświadczenie z mapami klawiszy, wykonuj małe zmiany.
Większe zmiany sprawiają, że trudniej jest debugować ewentualne problemy.

## Zbuduj swój firmware :id=build-your-firmware

Gdy twoje zmiany w mapie klawiszy są już gotowe, będziesz musiał skompilować firmware.
Aby to zrobić, wróć do swojego okna terminala i uruchom polecenie kompilacji:

    qmk compile

Jeśli nie skonfigurowałeś domyślnych ustawień środowiska, lub masz kilka klawiatur, możesz określić klawiaturę i/lub mapę klawiszy:

    qmk compile -kb <keyboard> -km <keymap>

Podczas kompilacji zobaczysz dużo informacji wyświetlanych na ekranie, informujących, które pliki są kompilowane.
Powinno to zakończyć się wynikiem podobnym do tego:

```
Linking: .build/planck_rev5_default.elf                                                             [OK]
Creating load file for flashing: .build/planck_rev5_default.hex                                     [OK]
Copying planck_rev5_default.hex to qmk_firmware folder                                              [OK]
Checking file size of planck_rev5_default.hex                                                       [OK]
 * The firmware size is fine - 27312/28672 (95%, 1360 bytes free)
```

## Wgraj swój Firmware :id=flash-your-firmware

Przejdź do [Wgrywanie Firmware’u](pl/newbs_flashing.md), aby dowiedzieć się, jak wgrać swoje nowe oprogramowanie do klawiatury.
