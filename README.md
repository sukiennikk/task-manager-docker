##### PODZIAŁ ZADANIA NA ETAPY


# 1
Stworzenie prostej aplikacji Flask.

Aplikacja powinna:
- wyświetlać stronę główną;
- pokazywać przykładową listę zadań;
- umożliwiać dodanie zadania;
- działać w kontenerze Dockera.

Cel: uruchomienie prostej aplikacji w jednym koneterze (wymaganie na 3.0).

Podział na osoby:

###### #1 KT
- stworzyć app.py
- implementacja prostej aplikacji Flask (w app.py)
- przygotować requirements.txt
- stworzyć Dockerfile backendu

###### #2 KS
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

#

# 2

Rozdzielenie aplikacji na frontend i backend. Uruchomienie w dwóch kontererach (wymaganie na ocenę 4.0).

Co ulega zmianie?
Frontend:
- HTML — struktura strony;
- CSS — wygląd;
- JavaScript — obsługa formularzy i komunikacja z API;
- Nginx — serwowanie strony i przekazywanie żądań API.
Backend:
- Flask — API;
- obsługa zadań;
- zwracanie danych w formacie JSON.


Podział na osoby:

###### #1 KT
- rozbudowa Flask o REST API.
- stworzenie endpoint GET /api/tasks.
- stworzenie endpoint POST /api/tasks.
- przygotowanie odpowiedzi JSON.
- aktualizacja Dockerfile backendu.

###### #2 KS
- rozbudowa html i css
- JavaScript korzystający z fetch()
- konfiguracja Nginx
- stworzenie Dockerfile frontendu

#

# 3

Dodanie PostgreSQL (bazy danych, uruchamiana w Dockerze, bez instalacji lokalnej). Wymaganie na ocenę 4.5.

Podział na osoby: 

###### #1 KT
- konfiguracja połączenia Flask z PostgreSQL
- stworzenie funkcji pobierania zadań z bazy
- implementacja dodawania, aktualizowania i usuwania rekordów
- przygotowuje konfigurację zmiennych środowiskowych

###### #2 KS
- stworzenie database/init.sql
- projekt tabeli i test zapytań SQL
- dodanie usługi PostgreSQL do Compose
- konfuguracja wolumenu na dane
- sprawdzenie, czy zadania pozostają w bazie po restarcie kontenerów

#

# 4

Dodanie Apache Kafka. Wymaganie na ocenę 5.0.

Zastosowanie prostego scenariusza:

Użytkownik dodaje nowe zadanie.
1. Frontend wysyła żądanie do backendu.
2. Backend zapisuje zadanie w PostgreSQL.
3. Backend wysyła komunikat do Kafki.
4. Konsument odbiera komunikat.
5. Konsument zapisuje informację w logach.

Podział na osoby:

###### #1 KT
- dodanie producenta Kafka do backendu
- implementacja wysyłania zdarzeń
- konfiguracja połączenia backendu z brokerem
- testowanie publikowania komunikatów

###### #2 KS
- dodanie usługi Kafka do Docker Compose
- konfiguracja brokera w trybie KRaft
- przygotowanie kodu konsumenta
- implementacja odbierania komunikatów
- sprawdzanie komunikatów w logach





