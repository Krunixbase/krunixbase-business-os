# **Moduł Cennik Statyczny — Krunixbase Business OS**

Moduł **Cennik Statyczny** definiuje oficjalne pakiety i ceny Krunixbase Business OS.  
Jest podstawą dla modułu dynamicznego, automatyzacji cenowych oraz systemu subskrypcji.

---

## 🟦 Pakiet STARTER — 0 zł przez 12 miesięcy → 9 zł/m‑c

Pakiet społeczny dla mikrofirm, JDG, freelancerów.

- CRM  
- Zadania  
- Projekty  
- 1 automatyzacja  
- 1 dashboard BI  
- 1 użytkownik  

**Cena:**

- 0 zł przez 12 miesięcy  
- 9 zł/m‑c po okresie startowym  

**Pakiet STARTER**

---

## 🟩 Pakiet GROW — 29 zł/m‑c

Dla małych firm, które zaczynają rosnąć.

- CRM  
- Projekty  
- Zadania  
- Budżety  
- Płatności  
- Automatyzacje  
- BI  
- 3 użytkowników  

**Cena: 29 zł/m‑c**

**Pakiet GROW**

---

## 🟧 Pakiet PRO — 79 zł/m‑c

Dla firm działających aktywnie.

- wszystkie moduły  
- workflow  
- AI predykcja  
- integracje REST  
- 10 użytkowników  

**Cena: 79 zł/m‑c**

**Pakiet PRO**

---

## 🟥 Pakiet ENTERPRISE — 299 zł/m‑c

Dla software house’ów, integratorów i dużych zespołów.

- pełny Business OS  
- moduły premium  
- automatyzacje unlimited  
- workflow unlimited  
- integracje REST  
- 50 użytkowników  

**Cena: 299 zł/m‑c**

**Pakiet ENTERPRISE**

---

## 🧱 Architektura modułu

### Warstwa danych
- tabela `pricing_plans`  
- tabela `pricing_features`  
- tabela `pricing_limits`  

### Warstwa API
- `/api/pricing/plans`  
- `/api/pricing/plan/:id`  

### Warstwa UI
- tabela pakietów  
- porównywarka pakietów  
- widok szczegółów pakietu  

---

## 🗄️ Schemat bazy danych

### Tabela: `pricing_plans`
- id  
- nazwa  
- cena  
- opis  
- okres_specjalny (JSONB)  

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

## 📊 Przykład pakietu (JSON)

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

## 🔗 Powiązania z innymi modułami

- **[Cennik dynamiczny**  
- **Subskrypcje**  
- **Pakiety społeczne**  

---

## 🏁 Status modułu

Moduł Cennik Statyczny jest:

- kompletny,  
- udokumentowany,  
- gotowy do wdrożenia,  
- zgodny z misją społeczną Krunixbase.
