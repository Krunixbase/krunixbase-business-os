# **Moduł Cennik Dynamiczny — Krunixbase Business OS**

Moduł **Cennik Dynamiczny** odpowiada za inteligentne, sprawiedliwe i automatyczne ustalanie cen pakietów Krunixbase.  
Łączy misję społeczną z ochroną twórców, zapewniając **najlepszą cenę w Polsce**, ale bez ryzyka przeciążenia darmowymi kontami.

---

## 🟦 Pakiety i ceny (pełna lista)

### **1. STARTER — 0 zł przez rok → 9 zł/m‑c**
Pakiet społeczny dla mikrofirm, JDG, freelancerów.

- CRM  
- Zadania  
- Projekty  
- 1 automatyzacja  
- 1 dashboard BI  
- 1 użytkownik  

```json
{
  "name": "STARTER",
  "price_free_period_months": 12,
  "price_after": 9,
  "modules": ["crm", "tasks", "projects"],
  "limits": { "users": 1, "automations": 1, "dashboards": 1 }
}
```

---

### **2. GROW — 29 zł/m‑c**
Dla małych firm, które zaczynają rosnąć.

- CRM  
- Projekty  
- Zadania  
- Budżety  
- Płatności  
- Automatyzacje  
- BI  
- 3 użytkowników  

```json
{
  "name": "GROW",
  "price": 29,
  "modules": ["crm", "projects", "tasks", "budgets", "payments", "automations", "bi"],
  "limits": { "users": 3 }
}
```

---

### **3. PRO — 79 zł/m‑c**
Dla firm, które działają aktywnie.

- wszystkie moduły  
- workflow  
- AI predykcja  
- integracje REST  
- 10 użytkowników  

```json
{
  "name": "PRO",
  "price": 79,
  "modules": "all",
  "limits": { "users": 10 }
}
```

---

### **4. ENTERPRISE — 299 zł/m‑c**
Dla software house’ów, integratorów, dużych zespołów.

- pełny Business OS  
- moduły premium  
- automatyzacje unlimited  
- workflow unlimited  
- integracje REST  
- 50 użytkowników  

```json
{
  "name": "ENTERPRISE",
  "price": 299,
  "modules": "all_premium",
  "limits": { "users": 50 }
}
```

---

## 🧩 Logika dynamiczna

Silnik dynamiczny dobiera cenę na podstawie:

- aktywności użytkownika,  
- liczby modułów,  
- liczby użytkowników,  
- przychodów firmy (opcjonalnie),  
- historii płatności,  
- sytuacji ekonomicznej firmy,  
- czy firma dopiero startuje,  
- czy firma ma trudniejszy okres.

---

## 🤖 Reguły dynamiczne (JSON)

### 1. STARTER → SYMBOLIC (po roku)

```json
{
  "name": "Starter to Symbolic",
  "condition": { "months_since_registration": ">12" },
  "action": { "switch_plan": "STARTER_SYMBOLIC", "price": 9 }
}
```

### 2. Zamrożenie ceny w trudnym okresie

```json
{
  "name": "Freeze Price",
  "condition": { "financial_status": "critical" },
  "action": { "freeze_price": true }
}
```

### 3. Automatyczny upgrade do GROW

```json
{
  "name": "Upgrade to Grow",
  "condition": { "usage_score": ">70" },
  "action": { "switch_plan": "GROW" }
}
```

---

## 🗄️ Schemat bazy danych

### Tabela: `pricing_plans`
- id  
- nazwa  
- cena  
- moduły (JSONB)  
- limity (JSONB)  
- okresy specjalne (JSONB)

### Tabela: `dynamic_pricing_rules`
- id  
- warunek (JSONB)  
- akcja (JSONB)  
- priorytet  

### Tabela: `pricing_history`
- id  
- client_id  
- plan_before  
- plan_after  
- price_before  
- price_after  
- reason  
- timestamp  

---

## ❤️ Manifest cenowy Krunixbase

> „Cennik nie jest narzędziem do zarabiania.  
> Jest narzędziem do równowagi:  
> pomagamy ludziom, ale nie pozwalamy, żeby nasza pomoc nas niszczyła.”

---

## 🏁 Status modułu

Moduł Cennik Dynamiczny jest:

- kompletny,  
- udokumentowany,  
- zgodny z misją społeczną,  
