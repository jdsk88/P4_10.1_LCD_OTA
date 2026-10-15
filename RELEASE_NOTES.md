v1.21.0: serwer DNS w panelu dla boxa BeSMART (routery bez nadpisania DNS, np. Netgear)

Panel może być serwerem DNS domu (UDP 53): zapytania przekazuje do serwera nadrzędnego (1.1.1.1, zapasowo 8.8.8.8), a na api.besmart-home.com odpowiada własnym adresem, dopóki ogrzewanie pracuje w trybie lokalnym. W routerze wystarczy wpisać adres panelu jako główny DNS (Netgear: Internet Setup -> Domain Name Server), publiczny jako zapasowy, i zrestartować box. Włącznik w Ustawienia -> Ogrzewanie (tryb lokalny) oraz na stronie WWW, z licznikami zapytań.

Poprawki:
- /api/heat: sekcja dns; /api/heatsettings: dns_enabled, dns_upstream
- docs/besmart.md: krok po kroku dla Netgear R6400v2
