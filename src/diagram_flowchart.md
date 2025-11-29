# 🔁 Diagram działania aplikacji (Flowchart)

## Opis
Diagram pokazuje główny przepływ logiki użytkownika w aplikacji monitorującej czas ekranowy.

---

## ASCII Flowchart

                +----------------------+
                |        Start         |
                +----------------------+
                           |
                           v
                +----------------------+
                | Uruchomienie aplikacji|
                +----------------------+
                           |
                           v
                +----------------------+
                | Wybór aplikacji do   |
                |    monitorowania     |
                +----------------------+
                           |
                           v
                +----------------------+
                | Monitorowanie czasu  |
                +----------------------+
                           |
           +---------------+---------------+
           |                               |
           v                               v
+------------------------+       +------------------------+
| Limit nie osiągnięty   |       | Limit osiągnięty       |
+------------------------+       +------------------------+
           |                               |
           v                               v
+------------------------+       +------------------------+
| Kontynuacja monitoringu|       | Wyświetl alert /       |
|                        |       | aktywuj blokadę        |
+------------------------+       +------------------------+
           \                               /
            \                             /
             +---------------------------+
             |       Raport dzienny      |
             +---------------------------+
                           |
                           v
                +----------------------+
                |         Koniec       |
                +----------------------+

---

## Uwagi
- „Monitorowanie czasu” działa w tle, co sekundę aktualizując liczniki.  
- Alerty i blokady są warunkowe, w zależności od ustawionych limitów.  
- Raport dzienny podsumowuje wykorzystanie wszystkich kategorii aplikacji.  
