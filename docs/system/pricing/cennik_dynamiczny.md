# **Cennik Dynamiczny — Krunixbase Business OS**

Cennik Dynamiczny Krunixbase jest inteligentnym systemem ustalania cen, który działa w oparciu o:

- aktywność użytkownika,  
- sytuację ekonomiczną firmy,  
- historię płatności,  
- ryzyko nadużyć,  
- misję społeczną Krunixbase.

Jego celem jest **równowaga**:  
technologia dostępna dla każdego, ale bez przeciążania twórców.

Dynamiczny cennik współpracuje z:

- **Cennikiem statycznym**  
- **Pakietami społecznymi**  
- **Pakietami NGO**  
- systemem subskrypcji  
- modułem automatyzacji  

---

## 🧠 Cele dynamicznego cennika

Dynamiczny cennik powstał, aby:

- obniżać ceny w trudnych okresach,  
- zamrażać ceny dla mikrofirm,  
- chronić twórców przed nadużyciami,  
- automatycznie dobierać najlepszy pakiet,  
- wspierać rozwój użytkownika,  
- zapobiegać masowym darmowym kontom,  
- utrzymać równowagę społeczną.

---

## 🔍 Jak działa dynamiczny cennik?

Silnik analizuje:

- aktywność użytkownika,  
- liczbę modułów,  
- liczbę użytkowników,  
- przychody firmy (opcjonalnie),  
- historię płatności,  
- ryzyko nadużyć,  
- status NGO lub społeczny,  
- okres działania firmy.

Na tej podstawie podejmuje decyzje:

- obniżenie ceny,  
- zamrożenie ceny,  
- automatyczny upgrade,  
- automatyczny downgrade,  
- przedłużenie okresu społecznego,  
- blokada nadużyć.

---

## ⚙️ Reguły dynamiczne (pełna lista)

### 🟦 1. Przedłużenie STARTER 0 zł

```json
{
  "name": "Extend Starter Free",
  "condition": {
    "financial_status": "critical",
    "usage_score": "<40"
  },
  "action": {
    "extend_free_period_months": 6
  }
}
```

---

### 🟩 2. Automatyczne przejście STARTER → STARTER SYMBOLIC (9 zł)

```json
{
  "name": "Starter to Symbolic",
  "condition": {
    "months_since_registration": ">12"
  },
  "action": {
    "switch_plan": "STARTER_SYMBOLIC",
    "price": 9
  }
}
```

---

### 🟧 3. Automatyczny upgrade do GROW

```json
{
  "name": "Upgrade to Grow",
  "condition": {
    "usage_score": ">70",
    "projects_active": ">5"
  },
  "action": {
    "switch_plan": "GROW"
  }
}
```

---

### 🟥 4. Zamrożenie ceny w trudnym okresie

```json
{
  "name": "Freeze Price",
  "condition": {
    "financial_status": "critical"
  },
  "action": {
    "freeze_price": true
  }
}
```

---

### 🟪 5. Obniżenie ceny dla NGO

```json
{
  "name": "NGO Discount",
  "condition": {
    "organization_type": "NGO"
  },
  "action": {
    "reduce_price_percent": 70
  }
}
```

---

### 🟫 6. Blokada nadużyć (masowe darmowe konta)

```json
{
  "name": "Abuse Protection",
  "condition": {
    "accounts_created_last_24h": ">3"
  },
  "action": {
    "require_verification": true
  }
}
```

---

## 🗄️ Struktura bazy danych

### Tabela: `dynamic_pricing_rules`
- id  
- nazwa  
- warunek (JSONB)  
- akcja (JSONB)  
- priorytet  
- aktywna (bool)  

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

## 📊 Przykład pełnej reguły (upgrade społeczny)

```json
{
  "name": "Social Upgrade",
  "condition": {
    "usage_score": ">60",
    "financial_status": "stable"
  },
  "action": {
    "switch_plan": "GROW",
    "notify_user": true
  }
}
```

---

## 🔗 Powiązania z innymi modułami

- **Cennik statyczny**  
- **Pakiety społeczne**  
- **Pakiety NGO**  
- **Porównywarka pakietów**  
- **Subskrypcje**  

---

## 🔥 Manifest dynamicznego cennika

> „Cena nie jest karą.  
> Cena nie jest barierą.  
> Cena jest narzędziem równowagi społecznej.  
> Krunixbase dostosowuje się do człowieka — nie odwrotnie.”

---

## 🏁 Status dokumentu

Cennik Dynamiczny jest:

- kompletny,  
- gotowy do repo,  
- zgodny z misją społeczną,  
- fundamentem automatyzacji cenowych.
