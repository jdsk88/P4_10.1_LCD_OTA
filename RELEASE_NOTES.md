v1.17.0: amplituner Yamaha w panelu, na WWW i w aplikacji; radio FM; zrzut ekranu panelu

Nowości:
- Amplituner Yamaha MusicCast (RX-V4A) sterowany bezpośrednio z panelu po sieci
  domowej (Yamaha Extended Control po HTTP, bez chmury). Ustawienia → Audio:
  adres i pokój; amplituner staje się urządzeniem w tym pokoju z kafelkiem na
  Start i w pokoju, a „Wychodzę” i „Wyłącz pokój” przełączają go w czuwanie.
- Widok amplitunera w stylu Crestron Home Media: kafelki źródeł z ikonami
  (HDMI, TV, AUDIO1–5, Bluetooth, tuner, USB, AirPlay, Spotify, radio
  internetowe; przytrzymanie nadaje własną nazwę, np. CD lub AUX), suwak
  głośności z wyciszeniem, osobny poziom startowy każdego źródła, karta „teraz
  gra” z przewijaniem, powtarzaniem i presetami, a dalej zakładki Dźwięk
  (program, dekoder surround, bas/soprany/dialog/subwoofer, Pure Direct,
  Enhancer, Extra Bass, Adaptive DRC), Wyjścia (głośniki strefy B z własną
  głośnością, HDMI OUT), Radio, Pilot (kursor i menu ekranowe, sceny, timer
  snu) i Więcej (Bluetooth, wyświetlacz, łącze MusicCast, opóźnienie audio).
  W poziomie źródła zajmują lewą kolumnę.
- Radio FM: lista stacji z nazwami i logotypami na panelu. Skanowanie pasma
  przez amplituner z nazwami z RDS, import jego presetów, dodawanie ręczne po
  częstotliwości; logotypy po nazwie stacji (radio-browser.info + miniatura
  JPEG przez images.weserv.nl). Wymaga anteny FM w amplitunerze.
- Całe API amplitunera przez panel: GET/POST /api/audio (ponad 30 akcji),
  /api/audio/yxc (dowolne wywołanie YXC, także zdalnie przez relay),
  /api/radio, /api/radio/logo. Strona WWW ma zakładkę Audio z konsolą API.
- GET /api/screen.bmp: zrzut tego, co jest na ekranie panelu.

Poprawki:
- Klimatyzacja: akcje „Wychodzę”/„Wyłącz pokój” obejmują amplituner.
- Odczyt list z amplitunera (wejścia, programy, presety) był pusty: parser
  z filtrem odrzucał odpowiedź bez pola response_code, a strumień TCP był
  czytany po kawałkach. Oba błędy usunięte.
