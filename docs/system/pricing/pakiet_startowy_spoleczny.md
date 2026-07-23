# **Pakiet Startowy Społeczny — Krunixbase Business OS**

Pakiet Startowy Społeczny jest sercem misji Krunixbase:  
**technologia dla każdego, niezależnie od sytuacji finansowej.**

To nie jest promocja.  
To nie jest marketing.  
To jest społeczny program wyrównywania szans, zgodny z:

- **Kodeksem Społecznym**  
- **Pakietami Społecznymi**  
- **Deklaracją Etyki Technologicznej**  
- **Deklaracją Odpowiedzialnego AI**  

---

## 🌍 Cel pakietu

Pakiet Startowy Społeczny powstał, aby:

- umożliwić start każdemu,  
- nie wykluczać mikrofirm, JDG, freelancerów, studentów, samotnych rodziców,  
- dać narzędzia do pracy bez kosztów,  
- chronić twórców przed przeciążeniem darmowymi kontami,  
- zapewnić uczciwą, symboliczną cenę po okresie społecznym.

---

## 🟦 Zawartość pakietu

Pakiet Startowy Społeczny zawiera:

- CRM  
- Zadania  
- Projekty  
- 1 automatyzacja  
- 1 dashboard BI  
- 1 użytkownik  
- Podstawowy workflow  
- Powiadomienia  
- Podstawowe API  

To jest zestaw, który pozwala realnie prowadzić działalność od pierwszego dnia.

---

## 💸 Model cenowy społeczny

### **0 zł przez 12 miesięcy**  
Każdy może zacząć bez barier.

### **9 zł/m‑c po roku**  
Symboliczna opłata, która:

- chroni twórców,  
- filtruje spam i masowe darmowe konta,  
- utrzymuje projekt społeczny przy życiu,  
- jest najniższą ceną w Polsce w tej kategorii.

---

## 🤖 Automatyzacje pakietu startowego

### Automatyczne przyznanie STARTER 0 zł

```json
{
  "trigger": "user.registration",
  "action": "subscriptions.assign_plan",
  "params": {
    "plan": "STARTER_SOCIAL",
    "price": 0,
    "duration_months": 12
  }
}
```

### Automatyczne przejście na STARTER 9 zł/m‑c

```json
{
  "trigger": "subscription.period_end",
  "action": "subscriptions.switch_plan",
  "params": {
    "from": "STARTER_SOCIAL",
    "to": "STARTER_SYMBOLIC",
    "price": 9
  }
}
```

### Zamrożenie ceny w trudnym okresie  
**zamrożenie ceny**

---

## 🧠 Społeczna logika pakietu

Silnik cenowy analizuje:

- aktywność,  
- sytuację finansową firmy (opcjonalnie),  
- wykorzystanie modułów,  
- historię płatności,  
- ryzyko nadużyć.

Jeśli firma ma trudniejszy okres:

- cena może zostać **zamrożona**,  
- okres społeczny może zostać **przedłużony**,  
- system może zaproponować **tańszy plan**.

Powiązanie z modułem:  
**Cennik dynamiczny**

---

## 🗄️ JSON pakietu startowego

```json
{
  "name": "STARTER_SOCIAL",
  "price_free_period_months": 12,
  "price_after": 9,
  "modules": ["crm", "tasks", "projects"],
  "limits": {
    "users": 1,
    "automations": 1,
    "dashboards": 1
  }
}
```

---

## 🔥 Manifest pakietu startowego

> „Każdy zasługuje na narzędzia do pracy.  
> Pieniądze nie mogą decydować o tym, kto może rozwijać firmę.  
> STARTER Społeczny jest dla ludzi — nie dla zysku.”

---

## 🏁 Status dokumentu

Pakiet Startowy Społeczny jest:

- kompletny,  
- zgodny z misją,  
- gotowy do publikacji,  
- fundamentem całego ekosystemu Krunixbase.
