PODZIAŁ ZADANIA NA ETAPY


#1
Stworzenie prostej aplikacji Flask.

Aplikacja powinna:
- wyświetlać stronę główną;
- pokazywać przykładową listę zadań;
- umożliwiać dodanie zadania;
- działać w kontenerze Dockera.

Cel: uruchomienie prostej aplikacji w jednym koneterze (wymaganie na 3.0).

Podział na osoby: 
##1 KT
- stworzyć app.py
- implementacja prostej aplikacji Flask (w app.py)
- przygotować requirements.txt
- stworzyć Dockerfile backendu

##2 KS
- zaprojektowanie wyglądu prostej strony HTML
- CSS
- dodanie formularza dodawania zadania
- pomoc w przygotowaniu pierwszego docker-compose.yml
- testowanie działania strony


Na początek, to pliki, których będziemy używać:
task-manager-docker/
│
├── backend/
│   ├── app.py
│   ├── requirements.txt
│   └── Dockerfile
│
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── app.js
│
└── docker-compose.yml

Pozostałe pliki pozostają nieużyte, potrzebne jednak do dalszej rozbudowy/podziału aplikacji o kontenery.
