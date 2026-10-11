v1.17.5: /api/ac przyjmuje dowolną właściwość z flagą raw (testy funkcji klimatyzatora)

Poprawki:
- POST /api/ac z "raw": true wysyła do chmury klimatyzacji dowolną
  właściwość t_* / f_* bez listy dozwolonych – do sprawdzania, które
  polecenia jednostka naprawdę wykonuje (bramka ConnectLife przyjmuje każdą
  nazwę bez błędu).
