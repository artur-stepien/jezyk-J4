# Przygotowanie paczek

## Wymagania
- Linus w WMS

## Proces budowania
- Przejdź w terminalu do katalogu repozytorium
- Aktualizacji notacji w plikach `php build/bump.php -v 5.1.1 -l 1` (`php build/bump.php -v WERSJA_JOOMLA -l NUMER_AKTUALIZACJI_TLUMACZENIA`)
- Wykonaj Commit zmian w plikach
- Stwórz tag nowej wersji (np. v5.1.1v1)
- Stwórz paczkę instalacyjną `php build/build.php --lpackages --tagversion "v5.1.1v1"` (`php build/build.php --lpackages --tagversion "NAZWA_TAGU"`)
- Stwórz zmiany dla Crowdin `php build/build.php --crowdin --tagversion "v5.1.1v1"` (`php build/build.php --crowdin --tagversion "NAZWA_TAGU"`)
- Stwórz zmiany dla Pakietu instalacyjnego `php build/build.php --install --tagversion "v5.1.1v1"` (`php build/build.php --install --tagversion "NAZWA_TAGU"`)
