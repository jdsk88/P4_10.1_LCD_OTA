Poczta: nie odrzucaj haseł, których panel nie zgadł

Pole hasła aplikacji wymagało dokładnie 16 liter, bez cyfr i innych znaków.
Hasła w innym formacie panel po prostu odrzucał i nie dało się ich zapisać.
Do tego w klawiaturze brakowało czterech znaków ASCII (^ ` | ~), więc hasła
z którymkolwiek z nich nie szło nawet wpisać.

Zmiany:
- hasło jest sprawdzane tylko pod kątem tego, czy nie jest puste; format
  ocenia serwer i zgłasza to jako "Logowanie nieudane"
- limit długości podniesiony z 24 do 64 znaków
- spacje są usuwane tylko wtedy, gdy wyglądają na sposób, w jaki Google
  wyświetla hasło aplikacji (cztery grupy po cztery litery); każde inne
  hasło zapisuje się dokładnie tak, jak je wpisano
- warstwa znaków specjalnych klawiatury obejmuje teraz każdy drukowalny
  znak ASCII, w pięciu wierszach
