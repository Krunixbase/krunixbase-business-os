# Moduł Baza Danych — Krunixbase Business OS

Warstwa danych Krunixbase Business OS jest fundamentem całego systemu. Zapewnia spójność, integralność, bezpieczeństwo oraz wysoką wydajność operacji. Struktura została zaprojektowana modułowo, aby wspierać CRM, projekty, budżety, KSeF, płatności, BI, automatyzacje oraz moduły premium.

---

## 1. Cele warstwy danych

- zapewnienie integralności danych,
- modularna struktura tabel,
- wysoka wydajność zapytań,
- pełna zgodność z modułami systemu,
- bezpieczeństwo i izolacja danych,
- łatwość integracji z API i BI.

---

## 2. Standardy projektowe

### **Model danych**
- relacyjny (PostgreSQL),
- modularny podział tabel,
- klucze obce między modułami,
- indeksy na polach krytycznych.

### **Konwencje nazewnictwa**
- snake_case,
- prefiksy modułów (crm_, proj_, bud_, ksef_, pay_, auto_),
- klucze główne: id (UUID).

### **Typy danych**
- UUID,
- TEXT,
- JSONB,
- TIMESTAMP,
- BOOLEAN,
- NUMERIC(12,2).

---

## 3. Struktura tabel — CRM

### **crm_clients**
- id (UUID),
- name,
- email,
- phone,
- status,
- created_at,
- updated_at.

### **crm_history**
- id,
- client_id,
- type,
- description,
- created_at.

---

## 4. Struktura tabel — Projekty

### **proj_projects**
- id,
- name,
- description,
- status,
- start_date,
- end_date,
- budget_id.

### **proj_tasks**
- id,
- project_id,
- title,
- description,
- status,
- due_date,
- assigned_to.

### **proj_stages**
- id,
- project_id,
- name,
- start_date,
- end_date,
- status.

---

## 5. Struktura tabel — Budżety

### **bud_budgets**
- id,
- project_id,
- total_cost,
- total_income,
- margin,
- updated_at.

### **bud_items**
- id,
- budget_id,
- type (cost/income),
- amount,
- description,
- related_invoice_id.

---

## 6. Struktura tabel — KSeF

### **ksef_invoices**
- id,
- ksef_id,
- number,
- client_id,
- amount,
- issue_date,
- due_date,
- status.

---

## 7. Struktura tabel — Płatności

### **pay_payments**
- id,
- type (online/bank),
- amount,
- client_id,
- invoice_id,
- created_at.

### **pay_bank_transactions**
- id,
- bank_id,
- amount,
- description,
- matched_invoice_id,
- created_at.

---

## 8. Struktura tabel — Windykacja

### **wnd_debts**
- id,
- invoice_id,
- client_id,
- days_late,
- status,
- risk_level.

### **wnd_actions**
- id,
- debt_id,
- type,
- status,
- created_at.

---

## 9. Struktura tabel — Automatyzacje

### **auto_rules**
- id,
- name,
- trigger,
- action,
- status.

### **auto_logs**
- id,
- rule_id,
- result,
- created_at.

---

## 10. Struktura tabel — BI

### **bi_metrics**
- id,
- module,
- key,
- value,
- timestamp.

### **bi_reports**
- id,
- name,
- data (JSONB),
- created_at.

---

## 11. Relacje między modułami

### **CRM ↔ Projekty**
- crm_clients.id → proj_projects.client_id

### **Projekty ↔ Budżety**
- proj_projects.id → bud_budgets.project_id

### **KSeF ↔ Płatności**
- ksef_invoices.id → pay_payments.invoice_id

### **KSeF ↔ Windykacja**
- ksef_invoices.id → wnd_debts.invoice_id

### **Automatyzacje ↔ Wszystkie moduły**
- auto_rules.trigger → event_name

---

## 12. Indeksy

### **Indeksy krytyczne**
- crm_clients.email (unique),
- proj_tasks.project_id,
- ksef_invoices.ksef_id (unique),
- pay_payments.invoice_id,
- wnd_debts.client_id,
- auto_logs.rule_id.

---

## 13. Bezpieczeństwo danych

- szyfrowanie danych wrażliwych,
- izolacja danych klientów,
- role i uprawnienia,
- audyt zmian,
- logi dostępu,
- zgodność z RODO.

---

## 14. Integracja z API

Warstwa danych jest w pełni zgodna z:

- REST API,
- webhookami,
- modułem BI,
- modułem automatyzacji,
- modułem predykcji AI.

---

## 15. Roadmap warstwy danych

- indeksy adaptacyjne,
- cache danych,
- replikacja pozioma,
- sharding modułów,
- warstwa danych premium,
- integracja z Data Lake.

---

## 16. Status warstwy danych

Warstwa danych jest kompletna, modularna i gotowa do produkcyjnego użycia w Krunixbase Business OS.

