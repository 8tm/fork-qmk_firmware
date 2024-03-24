* Poradnik
  * [Wstęp](pl/newbs.md)
  * [Konfiguracja](pl/newbs_getting_started.md)
  * [Budowanie Pierwszego Firmware](pl/newbs_building_firmware.md)
  * [Wgrywanie Firmware'u](pl/newbs_flashing.md)
  * [Uzyskiwanie Pomocy/Wsparcia](pl/support.md)
  * [Zewnętrzna przestrzeń użytkownika](pl/newbs_external_userspace.md)
  * [Pozostałe zasoby](pl/newbs_learn_more_resources.md)
  * [Sylabus](pl/syllabus.md)

* Najczęściej zadawane pytania (FAQ)
  * [Ogólne](pl/faq_general.md)
  * [Budowanie / Kompilowanie QMK](pl/faq_build.md)
  * [Rozwiązywanie problemów z QMK](pl/faq_misc.md)
  * [Debugowanie QMK](pl/faq_debug.md)
  * [Mapa klawiszy](pl/faq_keymap.md)
  * [Optymalizacja pamięci AVR](pl/squeezing_avr.md)
  * [Słownik](pl/reference_glossary.md)

* Konfigurator
  * [Przegląd](pl/newbs_building_firmware_configurator.md)
  * [Krok po kroku](pl/configurator_step_by_step.md)
  * [Rozwiązywanie problemów](pl/configurator_troubleshooting.md)
  * [Architektura](pl/configurator_architecture.md)
  * QMK API
    * [Przegląd](pl/api_overview.md)
    * [Dokumentacja](pl/api_docs.md)
    * [Obsługiwane klawiatury](pl/reference_configurator_support.md)
    * [Dodawanie domyślnych map klawiszy](pl/configurator_default_keymaps.md)

* CLI
    * [Przegląd](pl/cli.md)
    * [Konfiguracja](pl/cli_configuration.md)
    * [Polecenia](pl/cli_commands.md)
    * [Uzupełnianie tabulatora](pl/cli_tab_complete.md)

* Korzystanie z QMK
  * Przewodniki
    * [Personalizacja funkcji](pl/custom_quantum_functions.md)
    * [Instalacja sterowników za pomocą Zadig](pl/driver_installation_zadig.md)
    * [Przegląd Map klawiszy](pl/keymap.md)
    * Środowiska deweloperskie
      * [Przewodnik po Dockerze](pl/getting_started_docker.md)
    * Wgrywanie oprogramowania
      * [Wgrywanie firmware](pl/flashing.md)
      * [Wgrywanie firmware dla ATmega32A (ps2avrgb)](pl/flashing_bootloadhid.md)
    * Środowiska programistyczne (IDE)
      * [QMK w Eclipse](pl/other_eclipse.md)
      * [QMK w VSCode](pl/other_vscode.md)
    * Git - Najlepsze praktyki
      * [Wprowadzenie](pl/newbs_git_best_practices.md)
      * [Twoja kopia (Fork)](pl/newbs_git_using_your_master_branch.md)
      * [Konflikty scalania](pl/newbs_git_resolving_merge_conflicts.md)
      * [Naprawianie gałęzi](pl/newbs_git_resynchronize_a_branch.md)

  * Proste kody klawiszy
    * [Pełna lista](pl/keycodes.md)
    * [Podstawowe kody klawiszy](pl/keycodes_basic.md)
    * [Kody klawiszy specyficzne dla języka](pl/reference_keymap_extras.md)
    * [Klawisze modyfikujące](pl/feature_advanced_keycodes.md)
    * [Kody klawiszy Quantum](pl/quantum_keycodes.md)
    * [Magiczne kody klawiszy](pl/keycodes_magic.md)

  * Zaawansowane kody klawiszy
    * [Polecenie](pl/feature_command.md)
    * [Dynamiczne makra](pl/feature_dynamic_macros.md)
    * [Funkcja Grave Escape](pl/feature_grave_esc.md)
    * [Funkcja Leader Key](pl/feature_leader_key.md)
    * [Funkcja Mod-Tap](pl/mod_tap.md)
    * [Makra](pl/feature_macros.md)
    * [Klawisze myszy](pl/feature_mouse_keys.md)
    * [Programowalny przycisk](pl/feature_programmable_button.md)
    * [Funkcja Repeat Key](pl/feature_repeat_key.md)
    * [Funkcja Space Cadet Shift](pl/feature_space_cadet.md)
    * [Funkcja US ANSI Shifted Keys](pl/keycodes_us_ansi_shifted.md)

  * Funkcje oprogramowania
    * [Auto Shift](pl/feature_auto_shift.md)
    * [Autokorekta](pl/feature_autocorrect.md)
    * [Funkcja Caps Word](pl/feature_caps_word.md)
    * [Kombinacje](pl/feature_combo.md)
    * [Debounce API](pl/feature_debounce_type.md)
    * [Digitizer](pl/feature_digitizer.md)
    * [EEPROM](pl/feature_eeprom.md)
    * [Key Lock](pl/feature_key_lock.md)
    * [Key Overrides](pl/feature_key_overrides.md)
    * [Warstwy](pl/feature_layers.md)
    * [One Shot Keys](pl/one_shot_keys.md)
    * [OS Detection](pl/feature_os_detection.md)
    * [Raw HID](pl/feature_rawhid.md)
    * [Secure](pl/feature_secure.md)
    * [Send String](pl/feature_send_string.md)
    * [Sequencer](pl/feature_sequencer.md)
    * [Swap Hands](pl/feature_swap_hands.md)
    * [Tap Dance](pl/feature_tap_dance.md)
    * [Konfiguracja Tap-Hold](pl/tap_hold.md)
    * [Tri Layer](pl/feature_tri_layer.md)
    * [Unicode](pl/feature_unicode.md)
    * [Userspace](pl/feature_userspace.md)
    * [Obliczanie WPM](pl/feature_wpm.md)

  * Funkcje sprzętowe
    * Wyświetlacze
      * [Quantum Painter](pl/quantum_painter.md)
        * [Quantum Painter LVGL Integration](pl/quantum_painter_lvgl.md)
      * [Sterownik LCD HD44780](pl/feature_hd44780.md)
      * [Sterownik LCD ST7565](pl/feature_st7565.md)
      * [Sterownik OLED](pl/feature_oled_driver.md)
    * Oświetlenie
      * [Podświetlenie](pl/feature_backlight.md)
      * [Matryca LED](pl/feature_led_matrix.md)
      * [Oświetlenie RGB](pl/feature_rgblight.md)
      * [Matryca RGB](pl/feature_rgb_matrix.md)
    * [Audio](pl/feature_audio.md)
    * [Bluetooth](pl/feature_bluetooth.md)
    * [Bootmagic Lite](pl/feature_bootmagic.md)
    * [Konwertery](pl/feature_converters.md)
    * [Niestandardowa matryca](pl/custom_matrix.md)
    * [Przełącznik DIP](pl/feature_dip_switch.md)
    * [Kodery](pl/feature_encoders.md)
    * [Haptic Feedback](pl/feature_haptic_feedback.md)
    * [Dżojstik](pl/feature_joystick.md)
    * [Wskaźniki LED](pl/feature_led_indicators.md)
    * [MIDI](pl/feature_midi.md)
    * [Urządzenie wskazujące](pl/feature_pointing_device.md)
    * [Mysz PS/2](pl/feature_ps2_mouse.md)
    * [Podzielona klawiatura](pl/feature_split_keyboard.md)
    * [Stenografia](pl/feature_stenography.md)

  * Budowanie klawiatury
    * [Easy Maker for One Offs](pl/easy_maker.md)
    * [Portowanie klawiatur](pl/porting_your_keyboard_to_qmk.md)
    * [Przewodnik po ręcznym montażu](pl/hand_wire.md)
    * [Przewodnik po wgrywaniu ISP](pl/isp_flashing_guide.md)

* Rozwijanie QMK
  * [Lista kontrolna PR](pl/pr_checklist.md)
  * Niebezpieczne zmiany
    * [Przegląd](pl/breaking_changes.md)
    * [Mój pull request został oflagowany](pl/breaking_changes_instructions.md)
    * [Najnowszy ChangeLog](pl/ChangeLog/20240225.md "QMK v0.24.0 - 2024 Feb 25")
    * [Historia niebezpiecznych zmian](pl/breaking_changes_history.md)

  * Rozwój w języku C
    * [Przewodnik po debugowaniu ARM](pl/arm_debugging.md)
    * [Konwencje kodowania](pl/coding_conventions_c.md)
    * [Kompatybilne mikrokontrolery](pl/compatible_microcontrollers.md)
    * [Sterowniki](pl/hardware_drivers.md)
      * [ADC](pl/adc_driver.md)
      * [APA102](pl/apa102_driver.md)
      * [Audio](pl/audio_driver.md)
      * [I2C](pl/i2c_driver.md)
      * [SPI](pl/spi_driver.md)
      * [WS2812](pl/ws2812_driver.md)
      * [EEPROM](pl/eeprom_driver.md)
      * [Flash](pl/flash_driver.md)
      * ['serial'](pl/serial_driver.md)
      * [UART](pl/uart_driver.md)
    * [Sterowanie GPIO](pl/gpio_control.md)
    * [Wytyczne dotyczące tworzenia klawiatury](pl/hardware_keyboard_guidelines.md)

  * Rozwój w języku Python
    * [Konwencje kodowania](pl/coding_conventions_python.md)
    * [Rozwój QMK CLI](pl/cli_development.md)

  * Rozwój konfiguratora
    * QMK API
      * [Środowisko programistyczne](pl/api_development_environment.md)
      * [Przegląd architektury](pl/api_development_overview.md)

  * Rozwój platformy sprzętowej
    * Arm/ChibiOS
      * [Wybór mikrokontrolera](pl/platformdev_selecting_arm_mcu.md)
      * [Wczesna inicjalizacja](pl/platformdev_chibios_earlyinit.md)
      * [Raspberry Pi RP2040](pl/platformdev_rp2040.md)
      * [Proton C](pl/platformdev_proton_c.md)
      * [WeAct Blackpill F4x1](pl/platformdev_blackpill_f4x1.md)

  * Odnośniki QMK
    * [Współtworzenie QMK](pl/contributing.md)
    * [Tłumaczenie dokumentacji QMK](pl/translating.md)
    * [Opcje konfiguracji](pl/config_options.md)
    * [Konfiguracja oparta na danych](pl/data_driven_config.md)
    * [Dokumentacja Make](pl/getting_started_make_guide.md)
    * [Najlepsze praktyki dokumentacji](pl/documentation_best_practices.md)
    * [Szablony dokumentacji](pl/documentation_templates.md)
    * [Układy społecznościowe](pl/feature_layouts.md)
    * [Testowanie jednostkowe](pl/unit_testing.md)
    * [Przydatne funkcje](pl/ref_functions.md)
    * [Format info.json](pl/reference_info_json.md)

  * Dla lepszego zrozumienia
    * [Jak działają klawiatury](pl/how_keyboards_work.md)
    * [Jak działa macierz](pl/how_a_matrix_works.md)
    * [Zrozumienie QMK](pl/understanding_qmk.md)

  * Wbudowane w QMK (W trakcie tworzenia)
    * [Definicje](pl/internals/defines.md)
    * [Rejestr zwrotny wejścia](pl/internals/input_callback_reg.md)
    * [Urządzenie MIDI](pl/internals/midi_device.md)
    * [Proces konfiguracji urządzenia MIDI](pl/internals/midi_device_setup_process.md)
    * [Narzędzia dla urządzeń MIDI](pl/internals/midi_util.md)
    * [Funkcja Wyślij](pl/internals/send_functions.md)
    * [Narzędzia Sysex](pl/internals/sysex_tools.md)
