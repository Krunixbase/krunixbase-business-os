# Moduł API — Krunixbase Business OS

API Krunixbase Business OS umożliwia integrację z systemami zewnętrznymi, automatyzację procesów, synchronizację danych oraz budowę aplikacji partnerskich. API jest zgodne z REST, wykorzystuje JSON, autoryzację tokenową oraz standardy bezpieczeństwa enterprise.

---

## 1. Cele API

- integracja z systemami zewnętrznymi,
- dostęp do danych CRM, projektów, budżetów, KSeF, płatności i kampanii,
- automatyzacja procesów,
- budowa aplikacji partnerskich,
- synchronizacja danych mobilnych,
- obsługa webhooków.

---

## 2. Standardy API

### **Format danych**
- JSON (UTF‑8)
- struktury zgodne z modułami systemu

### **Protokół**
- REST (HTTPS)
- Webhooks (POST)

### **Autoryzacja**
- Bearer Token
- Tokeny partnerskie
- Tokeny aplikacji mobilnej

### **Bezpieczeństwo**
- TLS 1.3
- rate limiting
- audyt działań
- logi API
- izolacja danych

---

## 3. Endpoints — CRM

### **GET /api/crm/clients**
Zwraca listę klientów.

### **POST /api/crm/clients**
Tworzy nowego klienta.

### **GET /api/crm/clients/{id}**
Zwraca szczegóły klienta.

### **PATCH /api/crm/clients/{id}**
Aktualizuje klienta.

### **DELETE /api/crm/clients/{id}**
Usuwa klienta.

---

## 4. Endpoints — Projekty

### **GET /api/projects**
Lista projektów.

### **POST /api/projects**
Tworzenie projektu.

### **GET /api/projects/{id}**
Szczegóły projektu.

### **PATCH /api/projects/{id}**
Aktualizacja projektu.

### **GET /api/projects/{id}/tasks**
Zadania projektu.

### **GET /api/projects/{id}/budget**
Budżet projektu.

---

## 5. Endpoints — Zadania

### **GET /api/tasks**
Lista zadań.

### **POST /api/tasks**
Tworzenie zadania.

### **PATCH /api/tasks/{id}**
Aktualizacja zadania.

### **POST /api/tasks/{id}/complete**
Oznaczenie zadania jako wykonane.

---

## 6. Endpoints — Budżety

### **GET /api/budget/{projectId}**
Budżet projektu.

### **POST /api/budget/{projectId}/items**
Dodanie pozycji budżetowej.

### **PATCH /api/budget/items/{id}**
Aktualizacja pozycji budżetowej.

---

## 7. Endpoints — KSeF

### **GET /api/ksef/invoices**
Lista faktur.

### **POST /api/ksef/invoices/import**
Import faktury z KSeF.

### **GET /api/ksef/invoices/{id}**
Szczegóły faktury.

---

## 8. Endpoints — Płatności

### **GET /api/payments**
Lista płatności.

### **POST /api/payments/online**
Rejestracja płatności online.

### **POST /api/payments/bank**
Rejestracja transakcji bankowej.

---

## 9. Endpoints — Kampanie

### **GET /api/campaigns**
Lista kampanii.

### **POST /api/campaigns**
Tworzenie kampanii.

### **POST /api/campaigns/{id}/send**
Wysyłka kampanii.

---

## 10. Endpoints — Partnerzy

### **GET /api/partners**
Lista partnerów.

### **POST /api/partners**
Tworzenie partnera.

### **GET /api/partners/{id}/commissions**
Prowizje partnera.

---

## 11. Webhooki

### **Obsługiwane zdarzenia**
- crm.client.created  
- crm.client.updated  
- project.created  
- project.task.completed  
- payment.completed  
- ksef.invoice.imported  
- campaign.sent  
- risk.created  
- budget.updated  

### **Format webhooka**
```json
{
  "event": "project.task.completed",
  "timestamp": "2026-07-22T12:00:00Z",
  "data": {
    "taskId": 123,
    "projectId": 55
  }
}
```

---

## 12. Autoryzacja

### **Nagłówek**
```
Authorization: Bearer <token>
```

### **Typy tokenów**
- token użytkownika,
- token aplikacji,
- token partnera.

### **Endpoint tokenów**
```
POST /api/auth/token
```

---

## 13. Limity

- 1200 zapytań / godzinę / token  
- 60 zapytań / minutę / token  
- webhook retry: 3 próby  

---

## 14. Błędy API

### **Format błędu**
```json
{
  "error": "InvalidRequest",
  "message": "Missing required field: name"
}
```

### **Typy błędów**
- InvalidRequest  
- Unauthorized  
- Forbidden  
- NotFound  
- RateLimitExceeded  
- InternalError  

---

## 15. Przykłady użycia

### **Tworzenie klienta**
```json
POST /api/crm/clients
{
  "name": "Jan Kowalski",
  "email": "jan@example.com",
  "status": "lead"
}
```

### **Tworzenie zadania**
```json
POST /api/tasks
{
  "title": "Kontakt z klientem",
  "projectId": 55
}
```

### **Import faktury KSeF**
```json
POST /api/ksef/invoices/import
{
  "ksefId": "ABC123"
}
```

---

## 16. Roadmap API

- GraphQL API  
- API partnerów premium  
- API automatyzacji  
- API BI  
- API predykcji AI  
- API mobilne offline-first  

---

## 17. Status API

API jest stabilne, kompletne i gotowe do integracji z systemami zewnętrznymi.

```

---
