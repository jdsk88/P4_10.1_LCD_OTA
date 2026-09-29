v1.7.3: powrót do sprawdzonej sekwencji startu z 1.6.0

Wersje 1.7.0-1.7.2 przestawiały kolejność uruchamiania wokół ekranu
powitalnego i każda z nich psuła wybudzanie po aktualizacji OTA w inny
sposób. Ta wersja wraca dokładnie do sekwencji startu z 1.6.0 - ostatniej,
która po aktualizacji wstawała sama - a powitanie dokłada w jedynym
miejscu, w którym nie może zaszkodzić.

Zmiany:
- start identyczny jak w 1.6.0: wyświetlacz, interfejs, pierwsza klatka,
  podświetlenie, dopiero potem ekran powitalny. Cokolwiek by się z nim
  działo, panel jest już zapalony i narysowany
- radio i usługi startują od razu w rozruchu, jak w 1.6.0 (bez odkładania,
  które wprowadziła 1.7.1)
- ekran pożegnalny przy restarcie zapala podświetlenie, więc jest widoczny
  także po aktualizacji, kiedy ekran był wygaszony na czas zapisu
- reszta zabezpieczeń z 1.7.2 zostaje: restart zamiast zawieszenia przy
  braku pamięci, ponawianie startu panelu, wznawianie pobierania

Weryfikacja z oficjalnych źródeł ESP-IDF 5.5.5: restart programowy nie
resetuje hosta MIPI-DSI, ale sterownik resetuje jego rejestry przy
tworzeniu magistrali - ponowna inicjalizacja po restarcie jest wspierana
i żadne dodatkowe zabiegi przy wyłączaniu nie są potrzebne.
