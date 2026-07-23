 **Cennik Statyczny — Krunixbase Business OS**

Cennik Statyczny Krunixbase definiuje oficjalne, stałe ceny pakietów Business OS.  
Jest fundamentem dla:

- **Cennika dynamicznego**  
- **Pakietów społecznych**  
- **Pakietów NGO**  
- systemu subskrypcji  
- automatyzacji cenowych  

Cennik Statyczny jest prosty, przejrzysty i zgodny z misją społeczną Krunixbase.

---

## 📦 **Lista pakietów i cen (wersja statyczna)**

### 🟦 **STARTER**  
Pakiet społeczny dla mikrofirm i osób zaczynających od zera.

- **0 zł przez 12 miesięcy**  
- **9 zł/m‑c po okresie społecznym**  
- 1 użytkownik  
- CRM, Zadania, Projekty  
- 1 automatyzacja  
- 1 dashboard BI  

---

### 🟩 **GROW**  
Pakiet rozwojowy dla małych firm.

- **29 zł/m‑c**  
- 3 użytkowników  
- CRM, Projekty, Zadania, Budżety, Płatności  
- Pełne automatyzacje  
- BI  

---

### 🟧 **PRO**  
Pakiet operacyjny dla firm działających aktywnie.

- **79 zł/m‑c**  
- 10 użytkowników  
- Wszystkie moduły operacyjne  
- Workflow  
- Automatyzacje pełne  
- Integracje REST + Webhook  
- BI + AI predykcja  

---

### 🟥 **ENTERPRISE**  
Pakiet dla software house’ów, integratorów i dużych zespołów.

- **299 zł/m‑c**  
- 50 użytkowników  
- Wszystkie moduły premium  
- Workflow unlimited  
- Automatyzacje unlimited  
- Integracje unlimited  
- Zaawansowane BI + AI  

---

## 🧩 **Struktura danych (statyczna)**

### Tabela: `pricing_plans`

- id  
- nazwa  
- cena  
- opis  
- moduły (JSONB)  
- limity (JSONB)  
- typ (standard / social / NGO)  

### Tabela: `pricing_features`

- id  
- plan_id  
- funkcja  

### Tabela: `pricing_limits`

- id  
- plan_id  
- limit_nazwa  
- limit_wartosc  

---

## 📊 **Przykład pakietu w JSON (STARTER)**

```json
{
  "name": "STARTER",
  "price": {
    "free_period_months": 12,
    "after": 9
  },
  "modules": ["crm", "tasks", "projects"],
  "limits": {
    "users": 1,
    "automations": 1,
    "dashboards": 1
  }
}
```

---

## 🔗 **Powiązania z innymi modułami**

- **Cennik dynamiczny**  
- **Pakiety społeczne**  
- **Pakiety NGO**  
- **Porównywarka pakietów**  

---

## 🔥 Manifest cenowy Krunixbase

> „Cennik nie jest narzędziem do zarabiania.  
> Jest narzędziem do równowagi społecznej.  
> Technologia ma być dostępna dla każdego.”

---

## 🏁 Status dokumentu

Cennik Statyczny jest:

- kompletny,  
- gotowy do repo,  
- zgodny z misją społeczną,  
- fundamentem systemu subskrypcji.
