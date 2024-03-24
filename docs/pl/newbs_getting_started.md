# Konfiguracja Twojego środowiska QMK :id=setting-up-your-qmk-environment

Zanim będziesz mógł kompilować mapy klawiszy, musisz zainstalować odpowiednie oprogramowanie i skonfigurować swoje środowisko kompilacji.
Ta czynność musi zostać wykonana tylko raz, niezależnie od tego, dla ilu klawiatur chcesz skompilować oprogramowanie.

## 1. Wymagania wstępne :id=prerequisites

Aby rozpocząć, potrzebujesz kilku programów.

* [Edytor tekstu](pl/newbs_learn_more_resources.md#text-editor-resources)
  * Będziesz potrzebował programu, który umożliwia edycję i zapisywanie plików typu tekstowego.
Domyślny edytor dostarczany z wieloma systemami operacyjnymi nie zapisuje plików typu tekstowego, więc upewnij się, że wybrany przez ciebie edytor to umożliwia.
* [Toolbox (opcjonalnie)](https://github.com/qmk/qmk_toolbox)
  * Graficzny program dla systemów Windows i macOS, który umożliwia zarówno programowanie, jak i debugowanie twojej niestandardowej klawiatury.

?> Jeśli nie pracowałeś wcześniej z terminalem w Linux/Unix, istnieje kilka podstawowych pojęć i poleceń, których powinieneś się nauczyć.
[Te zasoby](pl/newbs_learn_more_resources.md#command-line-resources) nauczą cię wystarczająco, abyś mógł pracować z QMK.

## 2. Przygotuj swoje środowisko :id=set-up-your-environment

Postaraliśmy się, aby skonfigurowanie QMK było tak proste jak to możliwe.
Musisz tylko przygotować swoje środowisko Linux lub Unix, a następnie pozwolić QMK zainstalować resztę.

<!-- tabs:start -->

### ** Windows **

QMK utrzymuje zestaw narzędzi MSYS2, interfejs wiersza poleceń (CLI) oraz wszystkie niezbędne zależności.
Dostarcza również przydatny skrót terminala `QMK MSYS`, który bezpośrednio uruchamia odpowiednie środowisko.

#### Wymagania wstępne

Będziesz musiał zainstalować [QMK MSYS](https://msys.qmk.fm/).
Najnowsza wersja jest dostępna [tutaj](https://github.com/qmk/qmk_distro_msys/releases/latest).

<details>
  <summary>Zaawansowani użytkownicy</summary>

!> <b style="font-size:150%">Ten proces nie jest zalecany dla nowych użytkowników.</b>

Jeśli chcesz zainstalować MSYS2 ręcznie, poniższe sekcje przeprowadzą cię przez ten proces.

#### Wymagania wstępne

Będziesz musiał zainstalować [MSYS2](https://www.msys2.org).
Po zainstalowaniu zamknij wszystkie otwarte terminale MSYS (fioletowe ikony) i otwórz nowy 64-bitowy terminal MinGW (niebieska ikona) z menu Start.

!> **UWAGA:** 64-bitowy Terminal MinGW *nie* jest tym samym co terminal MSYS, który otwiera się po zakończeniu instalacji.
Twój wiersz poleceń powinien wyświetlać napis "MINGW64" fioletowym tekstem, a nie "MSYS".
Zobacz [tę stronę](https://www.msys2.org/wiki/MSYS2-introduction/#subsystems), aby uzyskać więcej informacji na temat różnic.

#### Instalacja

Zainstaluj QMK CLI, uruchamiając:

    pacman --needed --noconfirm --disable-download-timeout -S git mingw-w64-x86_64-python-qmk

</details>

### ** macOS **

QMK utrzymuje kran Homebrew i formułę, która automatycznie zainstaluje CLI oraz wszystkie niezbędne zależności.

#### Wymagania wstępne

Musisz zainstalować Homebrew.
Postępuj zgodnie z instrukcjami na https://brew.sh.

?> Jeśli używasz komputera z procesorem Apple Silicon, proces instalacji potrwa znacznie dłużej, ponieważ GitHub actions
nie posiadają natywnych runnerów do budowania paczek dla ARM i AVR.

#### Instalacja

Zainstaluj QMK CLI, uruchamiając:

    brew install qmk/qmk/qmk
    
### ** Linux/WSL **

?> **Uwaga dla użytkowników WSL**: Domyślnie proces instalacji sklonuje repozytorium QMK do twojego katalogu domowego 
WSL, ale jeśli sklonowałeś je ręcznie, upewnij się, że znajduje się wewnątrz instancji WSL, a nie w systemie plików 
Windows (czyli nie w `/mnt`), ponieważ dostęp do niego jest obecnie [wyjątkowo powolny](https://github.com/microsoft/WSL/issues/4197).

#### Wymagania wstępne

Będziesz musiał zainstalować Gita i Pythona.
Jest bardzo prawdopodobne, że masz już oba, ale jeśli nie, jedno z poniższych poleceń powinno je zainstalować:

* Debian / Ubuntu / Devuan: `sudo apt install -y git python3-pip`
* Fedora / Red Hat / CentOS: `sudo yum -y install git python3-pip`
* Arch / Manjaro: `sudo pacman --needed --noconfirm -S git python-pip libffi`
* Void: `sudo xbps-install -y git python3-pip`
* Solus: `sudo eopkg -y install git python3`
* Sabayon: `sudo equo install dev-vcs/git dev-python/pip`
* Gentoo: `sudo emerge dev-vcs/git dev-python/pip`

#### Instalacja

Zainstaluj QMK CLI, uruchamiając:

    python3 -m pip install --user qmk

#### Pakiety społecznościowe

Te pakiety są utrzymywane przez członków społeczności, więc mogą być nieaktualne lub niekompletnie funkcjonalne.
Jeśli napotkasz problemy, prosimy zgłosić je odpowiednim osobom utrzymującym te pakiety.

Na dystrybucjach opartych na Archu możesz zainstalować interfejs wiersza poleceń (CLI) z oficjalnych repozytoriów (UWAGA: 
w chwili pisania tego pakietu niektóre zależności są oznaczone jako opcjonalne, mimo iż nie powinny być):

    sudo pacman -S qmk

Możesz również spróbować pakietu `qmk-git` z AUR:

    yay -S qmk-git

###  ** FreeBSD **

#### Instalacja

Zainstaluj pakiet QMK CLI dla FreeBSD, wykonując:

    pkg install -g "py*-qmk"

UWAGA: pamiętaj, aby postępować zgodnie z instrukcjami wyświetlonymi na końcu instalacji (użyj `pkg info -Dg "py*-qmk"` aby ponownie wyświetlić instrukcje).

<!-- tabs:end -->

## 3. Uruchom konfigurację QMK :id=set-up-qmk

<!-- tabs:start -->

### ** Windows **

Otwórz QMK MSYS i uruchom poniższe polecenie:

    qmk setup

W większości sytuacji będziesz chciał odpowiedzieć `y` na wszystkie pytania.

### ** macOS **

Otwórz terminal i uruchom poniższe polecenie:

    qmk setup

W większości sytuacji będziesz chciał odpowiedzieć `y` na wszystkie pytania.

### ** Linux/WSL **

Otwórz swój ulubiony terminal i uruchom poniższe polecenie:

    qmk setup

W większości sytuacji będziesz chciał odpowiedzieć `y` na wszystkie pytania.

?>**Uwaga dotycząca systemów Debian, Ubuntu i ich pochodnych**:
Możliwe, że otrzymasz błąd mówiący coś w stylu: `bash: qmk: command not found`.
Jest to spowodowane [błędem](https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=839155), który wprowadził Debian wraz z 
wydaniem Bash 4.4, który usunął `$HOME/.local/bin` z PATH. Ten błąd został później naprawiony w Debianie i Ubuntu.
Niestety, Ubuntu ponownie wprowadził ten błąd i [jeszcze go nie naprawił](https://bugs.launchpad.net/ubuntu/+source/bash/+bug/1588562).
Na szczęście naprawa jest prosta. Uruchom to jako swój użytkownik: `echo 'PATH="$HOME/.local/bin:$PATH"' >> $HOME/.bashrc && source $HOME/.bashrc`

###  ** FreeBSD **

Otwórz swój ulubiony terminal i uruchom poniższe polecenie:

    qmk setup

W większości sytuacji będziesz chciał odpowiedzieć `y` na wszystkie pytania.

<!-- tabs:end -->

?> Folder domowy QMK można określić podczas konfiguracji za pomocą `qmk setup -H <path>`, a następnie zmieniać go za pomocą
[konfiguracji CLI](pl/cli_configuration.md?id=single-key-example) i zmiennej `user.qmk_home`.
Aby uzyskać listę wszystkich dostępnych opcji, uruchom `qmk setup --help`.

?> Jeśli już znasz obsługę GitHub, [zalecamy, abyś postępował zgodnie z tymi instrukcjami](pl/getting_started_github.md)
i użył `qmk setup <github_username>/qmk_firmware`, aby sklonować swoje osobiste repozytorium.
Jeśli nie wiesz, o co chodzi, możesz bezpiecznie zignorować tę wiadomość.

## 4. Przetestuj swoje środowisko :id=test-your-build-environment

Teraz, gdy masz skonfigurowane środowisko budowania QMK, możesz skompilować oprogramowanie dla swojej klawiatury.
Zacznij od próby skompilowania domyślnego układu klawiatury.
Powinieneś móc to zrobić za pomocą polecenia w następującym formacie:

    qmk compile -kb <keyboard> -km default

Na przykład, aby skompilować oprogramowanie dla klawiatury Clueboard 66%, użyjesz:

    qmk compile -kb clueboard/66/rev3 -km default

?> Opcja klawiatury jest ścieżką względną do katalogu klawiatury, powyższy przykład można znaleźć w `qmk_firmware/keyboards/clueboard/66/rev3`.
Jeśli nie jesteś pewien, możesz wyświetlić pełną listę obsługiwanych klawiatur za pomocą `qmk list-keyboards`.

Kiedy kompilacja się zakończy, powinieneś otrzymać pełno informacje, które będą kończyć się podobnie do tego:

```
Linking: .build/clueboard_66_rev3_default.elf                                                       [OK]
Creating load file for flashing: .build/clueboard_66_rev3_default.hex                               [OK]
Copying clueboard_66_rev3_default.hex to qmk_firmware folder                                        [OK]
Checking file size of clueboard_66_rev3_default.hex                                                 [OK]
 * The firmware size is fine - 26356/28672 (2316 bytes free)
```

# Tworzenie własnej mapy klawiszy :id=creating-your-keymap

Jesteś już gotowy, aby stworzyć własne mapowanie klawiszy!
W tym celu przejdź teraz do [Budowanie Pierwszego Firmware](pl/newbs_building_firmware.md).
