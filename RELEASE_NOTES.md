v1.17.3: strona WWW z pełnym menu na telefonie (ustawienia Wi-Fi w trybie hotspotu), świeży manifest aktualizacji

Poprawki:
- Na telefonie strona WWW miała w dolnym pasku tylko pięć pozycji i nie dało
  się dojść do Sieci, Oprogramowania, Fotowoltaiki ani Audio – w trybie
  hotspotu (AP / AP+STA) nie było więc jak ustawić sieci Wi-Fi. Teraz przycisk
  menu w górnym pasku otwiera pełną listę stron jak na komputerze, a strona
  System ma skróty do nich. Gdy panel pracuje tylko jako hotspot, Pulpit od
  razu podpowiada ustawienie sieci.
- „Sprawdź aktualizację” pobiera manifest przez API GitHuba zamiast z CDN,
  który przez 5 minut po wydaniu pokazywał poprzednią wersję; stary adres
  zostaje jako awaryjny.
