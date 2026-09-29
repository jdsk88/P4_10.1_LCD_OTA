1.6.0: panel WWW - pełna funkcjonalność w przeglądarce

Nowości:
- wbudowany serwer WWW: strona pod http://<adres-panelu>/ (albo
  http://jc8012-panel.local/), logowanie: admin + hasło hotspotu
- zakładki: status systemu, urządzenia ESP-NOW (parowanie, sterowanie
  oczyszczaczem, pomiary, wykresy z historii, zmiana nazwy, ping, usuwanie),
  poczta (skrzynka, odczyt, odpowiedź), ustawienia wyświetlacza i języka,
  konto Gmail, sieć Wi-Fi (skanowanie, statyczne IP, hotspot) oraz
  aktualizacje OTA, restart i reset fabryczny
- REST API pod /api/* (JSON, HTTP Basic auth)
- strona jest wbudowana w firmware, więc zawsze pasuje do działającej
  wersji i aktualizuje się razem z nią przez OTA


v1.7.0: ekran powitalny przy starcie

Nowości:
- po włączeniu panel pokazuje przez 4 s ekran powitalny: pulsująca ramka,
  świecąca ikona domku i napis „iSter electronics” na czarnym tle
- to ten sam projekt graficzny co w Piecyk_PID, przeskalowany 2,5x
  z 320x480 na 800x1280 (koło 250 px, poświata 300-400 px, ikona 96 px,
  napis 48 px); kolory, czasy i sposób pulsowania bez zmian
- w trakcie powitania dotyk jest ignorowany, a wygaszanie ekranu wstrzymane
- działa w obu orientacjach ekranu (pionowej i poziomej)
