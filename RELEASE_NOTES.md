Suwak nie cofa już widoku do poprzedniej strony

Przesunięcie suwaka w prawo (np. jasności albo prędkości wentylatora)
i puszczenie go przenosiło widok do poprzedniej strony. LVGL wysyła gest
„machnięcie w prawo” jeszcze w trakcie przeciągania, a panel traktuje taki
gest jako „wstecz” - ruch suwakiem wyglądał więc jak nawigacja.

Zmiany:
- gest powrotu jest ignorowany, gdy palec operuje widżetem przyjmującym
  poziome przeciąganie: suwakiem, przełącznikiem, pierścieniem oczyszczacza
  lub kursorem wykresu
- machnięcie w prawo poza takimi widżetami dalej cofa jak dotąd
- test w symulatorze odtwarza błąd na suwaku jasności (bez poprawki
  faktycznie wychodzi ze strony) i pilnuje obu zachowań
