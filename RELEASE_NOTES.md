v1.8.0: obsługa wideodomofonu (ESP-NOW)

Nowości:
- nowy widżet urządzenia typu „doorbell”: przycisk otwarcia drzwi (komenda
  „open”), stan rygla, licznik dzwonków z toastem przy nowym dzwonku
- wiersz WiFi urządzenia: połączone z siłą sygnału albo ostrzeżenie
  z przyciskiem „Połącz z WiFi” — z dotyku podpowiada SSID sieci panelu,
  pyta o hasło i wysyła komendę „wifi” szyfrowanym łączem ESP-NOW;
  panel WWW robi to samo przez istniejące API
- lista urządzeń grupowana po kategorii (audio-wideo, czujniki, inne);
  nagłówki pojawiają się dopiero, gdy kategorii jest więcej niż jedna
- device_meta zna typ „doorbell”: ikona dzwonka, tłumaczenia, etykiety
  komend open/wifi; stan łącza (wifi, wifi_rssi, lock_open, ring_age)
  nie dubluje się w pomiarach
- rejestr widżetów przyjmuje listę komend obsługiwanych przez widżet
