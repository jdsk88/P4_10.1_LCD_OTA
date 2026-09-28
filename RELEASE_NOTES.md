Naprawa OTA: pobieranie do PSRAM przed zapisem flasha

Aktualizacja przez OTA kończyła się błędem „pobieranie przerwane (stalled)”
i zrywała łączność Wi-Fi aż do restartu panelu.

Przyczyna: biblioteka Update kasuje flash blokami po 64 KB dopiero w trakcie
zapisu, a dotychczasowy kod zapisywał obraz na bieżąco, w pętli pobierania.
Każde kasowanie blokuje pamięć podręczną na setki milisekund, więc host nie
obsługuje przerwań SDIO i łącze ESP-Hosted do ESP32-C6 rozpada się na dobre.

Zmiany:
- instalacja w dwóch etapach: cały obraz trafia najpierw do PSRAM, a flash
  jest zapisywany dopiero po zamknięciu połączenia HTTPS
- suma SHA-256 sprawdzana przed dotknięciem flasha
- zapis porcjami przez bufor w RAM wewnętrznym, żeby esp_flash_write nie
  musiał kopiować z PSRAM i nie mógł polec na braku pamięci
- osobne komunikaty postępu: „Pobieranie %” oraz „Instalowanie % - nie wyłączaj”
- notatki wydania pokazywane na panelu bez technicznych stopek commita

Uwaga: wersje starsze niż 1.4.1 nie zainstalują tej poprawki przez OTA,
pierwsze wgranie musi pójść przez USB.
