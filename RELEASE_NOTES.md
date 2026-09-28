v1.5.0: motywy kolorystyczne i naprawa przycisku wentylatora

Nowości:
- Ustawienia -> Wyświetlacz: wybór motywu kolorów obok trybu ciemny/jasny.
  Sześć schematów: Domyślny, Zielony, Niebieski, Fioletowy, Lekko niebieski
  i Lekko biały - każdy z osobną paletą ciemną i jasną, więc łączy się
  z przełącznikiem trybu. Wybiera się je kolorowymi kółkami, zmiana działa
  natychmiast. Odcienie dobrane pod RGB565, żeby nic nie prążkowało.

Poprawki:
- przycisk zasilania oczyszczacza reaguje natychmiast po dotknięciu;
  wcześniej odświeżał się dopiero po pół sekundy, a szybkie drugie
  stuknięcie wysyłało tę samą komendę zamiast przełączyć z powrotem -
  przycisk sprawiał wrażenie zawieszonego. Wybór trybu pracy także
  podświetla się od razu.
