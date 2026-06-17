graph TD
    A([Uruchomienie systemu skrzyżowania]) --> B[Odczyt danych z czujników]
    B --> C{Pojazd uprzywilejowany?}
    
    C -- Tak --> D[Wymuś ZIELONE dla pojazdu]
    D --> E[Czekaj na przejazd karetki]
    E --> B
    
    C -- Nie --> F{Piesi / Duży ruch?}
    F -- Tak --> G[Zmiana strategii: Wydłuż ZIELONE]
    G --> H[Standardowy cykl zmiany świateł]
    
    F -- Nie --> H
    H --> I{Wykryto awarię?}
    
    I -- Tak --> J[Tryb Awaryjny: Migające ŻÓŁTE]
    J --> K([Powiadomienie Centrum Sterowania])
    
    I -- Nie --> B
