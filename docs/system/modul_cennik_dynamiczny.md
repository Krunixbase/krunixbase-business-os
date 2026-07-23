# **Moduł Cennik Dynamiczny — Krunixbase Business OS**

Moduł **Cennik Dynamiczny** odpowiada za inteligentne, sprawiedliwe i automatyczne ustalanie cen pakietów Krunixbase.  
Jego celem jest **zrównoważenie misji społecznej z ochroną twórców**, tak aby:

- każdy mógł zacząć,  
- nikt nie był wykluczony,  
- a my nie byliśmy przeciążeni darmową obsługą tysięcy kont.

---

## 🎯 Cele modułu

- zapewnić najniższe ceny w Polsce,  
- chronić twórców przed nadmiernym obciążeniem,  
- dostosować cenę do sytuacji firmy,  
- automatycznie dobierać najlepszy plan,  
- wspierać mikrofirmy i osoby zaczynające od zera,  
- utrzymać równowagę między misją społeczną a realiami operacyjnymi.

---

## 🔧 Funkcje modułu

- dynamiczne ustalanie ceny,  
- analiza aktywności użytkownika,  
- analiza przychodów firmy (opcjonalnie),  
- analiza wykorzystania modułów,  
- automatyczne przełączanie planów,  
- zamrażanie ceny w trudnych okresach,  
- obniżki społeczne,  
- rekomendacje planów,  
- logika anty‑wyzyskowa.

---

## 🟦 Model STARTER (0 zł → 9 zł/m‑c)

### **0 zł przez 12 miesięcy**
Każdy może zacząć bez barier.

### **9 zł/m‑c po roku**
Symboliczna opłata, aby:

- nie mieć tysięcy darmowych kont,  
- nie pracować za darmo ponad siły,  
- nie utrzymywać infrastruktury z własnej kieszeni.

To jest **ochrona twórców**, nie komercja.

---

## 🧠 Logika dynamiczna

Silnik analizuje:

- liczbę użytkowników,  
- aktywność,  
- moduły,  
- historię płatności,  
- czy firma jest w trudnej sytuacji,  
- czy firma rośnie,  
- czy firma korzysta z modułów premium.

Na tej podstawie dobiera **najbardziej sprawiedliwą cenę**.

---

## 🤖 Automatyzacje cenowe

### 1. IF firma dopiero startuje → THEN STARTER 0 zł

**pakiet startowy**

### 2. IF minęło 12 miesięcy → THEN 9 zł/m‑c

```json
{
  "trigger": "subscription.period_end",
  "action": "subscriptions.switch_plan",
  "params": {
    "from": "STARTER_FREE",
    "to": "STARTER_SYMBOLIC",
    "price": 9
  }
}
```

### 3. IF firma ma trudniejszy okres → THEN zamroź cenę

**zamrożenie ceny**

### 4. IF firma rośnie → THEN zaproponuj GROW

**upgrade społeczny**

---

## 🗄️ Schemat bazy danych

### Tabela: `dynamic_pricing_rules`
- id  
- nazwa  
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

## 📊 Przykład reguły (JSON)

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

## ❤️ Manifest modułu

> „Cennik Krunixbase nie jest narzędziem do zarabiania.  
> Jest narzędziem do równowagi:  
> pomagamy ludziom, ale nie pozwalamy, żeby nasza pomoc nas niszczyła.”

---

## 🏁 Status modułu

Moduł Cennik Dynamiczny jest:

- opisany,  
- udokumentowany,  
- zgodny z misją społeczną,  
- gotowy do implementacji.
