v1.17.1: aktualizacja OTA znów działa; wybór dostawcy klimatyzacji: ConnectLife, Smart Life (chmura) lub Smart Life (lokalnie)

Poprawki:
- Aktualizacja OTA nie zawiesza się już na 0–5 % i nie zrywa Wi-Fi: obraz jest
  pobierany w porcjach po 32 KB na jednym połączeniu, więc pamięć wewnętrzna
  panelu nie kończy się w trakcie pobierania. Na czas instalacji amplituner,
  falownik i kamera czekają, a przy zbyt małej ilości wolnej pamięci panel
  prosi o restart zamiast tracić sieć.

Nowości:
- Ustawienia → Klimatyzacja → Dostawca (API): obok ConnectLife można wybrać
  Smart Life / Tuya Smart – przez chmurę (klucze projektu z iot.tuya.com,
  centrum danych) albo lokalnie po sieci domowej (protokół Tuya 3.3/3.4/3.5,
  bez żadnej chmury; wystarczy id urządzenia i klucz lokalny z konta aplikacji,
  które wypisuje tools/smartlife/local_keys.sh po zeskanowaniu kodu QR
  w aplikacji Smart Life).
- Jednostki Smart Life konfiguruje się na stronie WWW panelu i w aplikacji
  (lista jednostek, klucze, pokój, numery DP dla nietypowych produktów);
  panel pokazuje stan i liczbę dostępnych jednostek.
- Przyciski, których dany klimatyzator nie ma (np. Turbo, Cichy), są ukrywane
  na panelu, w WWW i w aplikacji.
- Opis obu wariantów Smart Life w docs/smartlife.md.
