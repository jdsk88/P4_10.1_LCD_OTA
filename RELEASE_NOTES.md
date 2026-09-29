v1.7.1: ekran powitalny przy starcie i wyłączaniu, odporniejsza aktualizacja

Ekran powitalny:
- pokazuje się teraz także przy wyłączaniu: restart z ustawień, restart po
  aktualizacji OTA i restart z panelu WWW zaczynają się od tego samego
  ekranu, zamiast gasnąć na niebiesko
- podczas startu animacja była szarpana, bo uruchamianie ESP32-C6 po SDIO
  blokuje procesor na ponad sekundę; radio startuje teraz dopiero po
  zniknięciu powitania, więc animacja jest płynna
- działa w obu orientacjach ekranu

Wyłączanie i restart:
- przed resetem wyświetlacz jest gaszony i zasilanie toru MIPI zwalniane;
  wcześniej kontroler obrazu nagle tracił zasilanie i malował niebieski ekran
- brak zasilania toru MIPI po restarcie programowym nie przerywa już startu
  firmware: panel loguje ostrzeżenie i próbuje dalej, zamiast wpadać
  w pętlę restartów z ciemnym ekranem (wtedy nie dawało się zrobić nic,
  nawet zaktualizować panelu)

Aktualizacja OTA:
- przerwane pobieranie jest wznawiane od miejsca zatrzymania (żądanie Range),
  do czterech prób; wcześniej jedno zacięcie unieważniało całe pobieranie
  i trzeba było zaczynać od zera
