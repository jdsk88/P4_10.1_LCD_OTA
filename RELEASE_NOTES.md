Pliki wydań pod adresami z numerem wersji

Manifest i obrazy firmware idą przez cache GitHuba (5 minut), a każdy plik
odświeża się w nim niezależnie. Tuż po wydaniu panel mógł więc dostać już
nowy manifest, ale jeszcze stary obraz - i zgłosić „niezgodną sumę
kontrolną”. Teraz każde wydanie ma pliki o unikalnych nazwach
(firmware-<wariant>-vX.Y.Z.bin), więc taka mieszanka jest niemożliwa.
Workflow zostawia w repo obrazy poprzedniego wydania (dla manifestu, który
może jeszcze wisieć w cache) i sprząta starsze.

Na panelu ta wersja niczego nie zmienia - służy też do sprawdzenia poprawki
z 1.4.2: podczas zapisu firmware ekran powinien zgasnąć po komunikacie,
zamiast migotać na niebiesko.
