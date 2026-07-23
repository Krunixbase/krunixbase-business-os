# **Moduł Subskrypcje — Krunixbase Business OS**

Moduł **Subskrypcje** odpowiada za zarządzanie abonamentami, cyklicznymi płatnościami, planami, okresami rozliczeniowymi oraz automatycznym odnawianiem usług.  
Jest fundamentem dla produktów SaaS, usług cyklicznych, pakietów premium i modeli membership.

---

## 🔵 Cele modułu

- obsługa abonamentów i planów,  
- automatyczne cykliczne płatności,  
- przypomnienia i powiadomienia,  
- integracja z CRM, Płatnościami i Budżetami,  
- pełna historia subskrypcji,  
- obsługa statusów (aktywna, wygasła, anulowana).

---

## 🔧 Funkcje modułu

- tworzenie planów subskrypcyjnych,  
- cykliczne rozliczenia (miesięczne, roczne, custom),  
- automatyczne odnowienia,  
- integracja z modułem **Płatności**,  
- przypomnienia o kończących się subskrypcjach,  
- logi cyklicznych operacji,  
- obsługa rabatów i kuponów,  
- powiązanie z klientami (CRM).

---

## 🧩 Typy subskrypcji

- **Miesięczna**  
- **Roczna**  
- **Okres niestandardowy**  
- **Jednorazowa z auto‑renew**  
- **Pakietowa**  

---

## 🧱 Architektura modułu

### Warstwa UI/UX
- lista subskrypcji,  
- szczegóły klienta,  
- historia płatności,  
- konfigurator planów,  
- statusy i timeline.

### Warstwa API
- `POST /api/subscriptions/create`  
- `POST /api/subscriptions/renew/:id`  
- `GET /api/subscriptions/list`  
- `GET /api/subscriptions/history/:id`  
- `PUT /api/subscriptions/update/:id`  
- `DELETE /api/subscriptions/cancel/:id`

### Warstwa logiki
- silnik cyklicznych płatności,  
- harmonogram odnowień,  
- integracja z płatnościami,  
- walidacja statusów,  
- retry/fallback.

### Warstwa danych
- tabele subskrypcji,  
- tabele planów,  
- tabele historii płatności,  
- tabele rabatów.

---

## 🗄️ Schemat bazy danych

### Tabela: `subscriptions`
- id (UUID)  
- client_id (CRM)  
- plan_id  
- status  
- next_payment_at  
- created_at  
- updated_at  

### Tabela: `subscription_plans`
- id  
- nazwa  
- cena  
- okres (month/year/custom)  
- opis  

### Tabela: `subscription_payments`
- id  
- subscription_id  
- kwota  
- status  
- timestamp  

---

## 🔌 Integracje z modułami

### Subskrypcje → CRM  
- przypisanie subskrypcji do klienta,  
- historia aktywności.

### Subskrypcje → Płatności  
- automatyczne generowanie płatności cyklicznych.

### Subskrypcje → Budżety  
- prognozy przychodów cyklicznych.

### Subskrypcje → Automatyzacje  
- IF subskrypcja wygasa → THEN wyślij powiadomienie.

---

## 🤖 Przykład workflow subskrypcji (JSON)

```json
{
  "name": "Odnowienie subskrypcji",
  "steps": [
    {
      "type": "subscriptions.renew",
      "params": { "subscription_id": "UUID" }
    },
    {
      "type": "payments.charge",
      "params": { "method": "card" }
    },
    {
      "type": "notifications.send",
      "params": { "template": "renew_success" }
    }
  ]
}
```

---

## 📄 Dokumentacja powiązana

- **[moduł płatności](modul_platnosci.md)**  
- **[moduł automatyzacje](modul_automatyzacje.md)**  
- **[moduł CRM](modul_crm.md)**  
- **[moduł budżety](modul_budzet.md)**  

---

## 🏁 Status modułu

Moduł Subskrypcje jest:

- opisany,  
- udokumentowany,  
- zgodny z architekturą,  
- gotowy do implementacji.
