v1.7.2: ekran budzi się po aktualizacji

Od wersji 1.7.0 po aktualizacji OTA ekran potrafił nie zapalić się wcale -
pomagało dopiero odcięcie zasilania. Przyczyna leżała w kolejności startu,
którą wprowadził ekran powitalny, a 1.7.1 dołożyła do tego drugi błąd.
Oba są naprawione.

Poprawki:
- podświetlenie zapala się zaraz po uruchomieniu wyświetlacza, zanim
  cokolwiek zostanie narysowane. Wcześniej czekało na pierwszą klatkę, więc
  gdy jej rysowanie się nie powiodło, ekran zostawał czarny na zawsze
- nieudana alokacja pamięci w LVGL nie zatrzymuje już panelu w nieskończonej
  pętli, tylko go restartuje; przy powtarzalnej awarii bootloader wróci do
  poprzedniej wersji, zamiast zostawić martwe urządzenie
- ekran powitalny nie rysuje już rozmytego cienia pod ikoną - to była
  największa pojedyncza alokacja przy starcie, a świecąca poświata i tak
  daje ten sam efekt
- cofnięte zwalnianie zasilania toru MIPI przed restartem, które dodałem
  w 1.7.1: odcinało napięcie od układu obrazu dokładnie w chwili resetu
- nieudane uruchomienie panelu jest ponawiane trzy razy, zanim start
  firmware zostanie przerwany
