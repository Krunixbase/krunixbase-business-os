# **Get Started — Krunixbase Business OS**

Krunixbase Business OS to modularny system operacyjny dla biznesu.  
Ta strona przeprowadzi Cię przez pierwsze kroki: instalację, strukturę repozytorium, uruchomienie środowiska oraz podstawowe moduły.

---

## 🚀 1. Wymagania

- Node.js (LTS)  
- PostgreSQL  
- Docker (opcjonalnie)  
- Git  
- dowolny edytor (VS Code polecany)

---

## 📦 2. Pobranie projektu

```bash
git clone https://github.com/Krunixbase/krunixbase-business-os
cd krunixbase-business-os
```

---

## 🧱 3. Struktura repozytorium

```
/src
  /api
  /modules
  /database
  /ui
  /automation

/docs
  /system
    modul_architektura.md
    moduly_systemu.md
    brandbook.md
    whitepaper.md
    ...
```

Pełna lista modułów:  
**[moduły systemu](moduly_systemu.md)**

---

## ⚙️ 4. Instalacja zależności

```bash
npm install
```

---

## 🗄️ 5. Konfiguracja bazy danych

Utwórz bazę PostgreSQL:

```sql
CREATE DATABASE krunixbase;
```

Skonfiguruj `.env`:

```
DB_HOST=localhost
DB_PORT=5432
DB_USER=postgres
DB_PASS=twoje_haslo
DB_NAME=krunixbase
```

---

## ▶️ 6. Uruchomienie systemu

```bash
npm run dev
```

System uruchomi się na:

```
http://localhost:3000
```

---

## 🧩 7. Pierwsze moduły

### CRM
Zarządzanie klientami i kontaktami.

### Projekty
Tworzenie projektów, etapów, harmonogramów.

### Zadania
Zarządzanie zadaniami i priorytetami.

### Budżety
Koszty, przychody, marże.

Pełna dokumentacja modułów:  
**[moduły systemu](moduly_systemu.md)**

---

## 🔌 8. API — pierwsze zapytania

### Lista klientów

```bash
GET /api/crm/list
```

### Tworzenie projektu

```bash
POST /api/projects/create
```

### Lista zadań

```bash
GET /api/tasks/list
```

Pełna dokumentacja API:  
**[moduł API](moduly_api.md)**

---

## 🤖 9. Pierwsza automatyzacja IF→THEN

Przykład:

**IF** klient zostanie dodany  
**THEN** utwórz projekt startowy

```json
{
  "trigger": "crm.create",
  "action": "projects.create",
  "params": {
    "template": "default"
  }
}
```

Dokumentacja automatyzacji:  
**[moduł automatyzacje](modul_automatyzacje.md)**

---

## 📊 10. BI & AI — pierwsze kroki

### BI
- dashboardy  
- wykresy  
- metryki  

### AI
- predykcja danych  
- rekomendacje działań  

Dokumentacja:  
**[BI & AI](modul_bi_ai.md)**

---

## 🔐 11. Bezpieczeństwo

System implementuje:

- TLS 1.3  
- role i uprawnienia  
- audyt działań  
- zgodność z RODO  

Dokumentacja:  
**[moduł bezpieczeństwo](modul_bezpieczenstwo.md)**

---

## 📄 12. Dokumentacja

Krunixbase posiada pełny zestaw dokumentów:

- **[Whitepaper](whitepaper.md)**  
- **[README premium](README_premium.md)**  
- **[Brandbook](brandbook.md)**  
- **[Pitch Deck](pitch_deck.md)**  
- **[Press Kit](press_kit.md)**  
- **[About](about.md)**  

---

## 🤝 13. Współpraca

Krunixbase jest projektem open‑source.  
Możesz:

- tworzyć moduły,  
- zgłaszać pomysły,  
- rozwijać dokumentację,  
- budować integracje.

Repozytorium:  
github.com/Krunixbase/krunixbase-business-os
