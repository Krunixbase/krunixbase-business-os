# **Moduł Workflow — Krunixbase Business OS**

Moduł **Workflow** odpowiada za projektowanie, wykonywanie i monitorowanie procesów biznesowych w Krunixbase.  
Pozwala tworzyć sekwencje kroków, reguły, warunki, automatyzacje oraz integracje między modułami.

---

## 🔵 Cele modułu

- standaryzacja procesów biznesowych,  
- automatyzacja powtarzalnych działań,  
- eliminacja błędów operacyjnych,  
- pełna widoczność przepływu pracy,  
- integracja modułów w jedną logikę operacyjną.

---

## 🔧 Funkcje modułu

- projektowanie workflow (graficznie + JSON),  
- kroki sekwencyjne i równoległe,  
- warunki IF/ELSE,  
- akcje systemowe,  
- integracje między modułami,  
- logi wykonania,  
- retry / fallback,  
- powiadomienia.

---

## 🧩 Typy kroków

- **Akcja** — wykonanie operacji (np. utwórz zadanie).  
- **Warunek** — IF/ELSE.  
- **Webhook** — wywołanie zewnętrznego API.  
- **Opóźnienie** — delay, harmonogram.  
- **Równoległość** — wykonanie wielu ścieżek naraz.  
- **Powiadomienie** — wysłanie komunikatu.  

---

## 🧱 Architektura modułu

### Warstwa UI/UX
- kreator workflow (drag & drop),  
- edytor JSON,  
- podgląd wykonania,  
- logi kroków.

### Warstwa API
- `POST /api/workflow/create`  
- `POST /api/workflow/run`  
- `GET /api/workflow/logs/:id`  
- `PUT /api/workflow/update/:id`  
- `DELETE /api/workflow/delete/:id`

### Warstwa logiki
- silnik workflow,  
- kolejka zadań,  
- retry/fallback,  
- walidacja kroków,  
- integracja z automatyzacjami.

### Warstwa danych
- tabele workflow,  
- tabele kroków,  
- tabele logów,  
- tabele instancji wykonania.

---

## 🗄️ Schemat bazy danych

### Tabela: `workflow`
- id (UUID)  
- nazwa  
- opis  
- status  
- created_at  
- updated_at  

### Tabela: `workflow_steps`
- id  
- workflow_id  
- typ  
- konfiguracja (JSONB)  
- kolejność  

### Tabela: `workflow_logs`
- id  
- workflow_id  
- step_id  
- status  
- message  
- timestamp  

---

## 🔌 Integracje z modułami

### Workflow → CRM  
- automatyczne tworzenie leadów,  
- scoring klientów.

### Workflow → Projekty  
- tworzenie projektów na podstawie zdarzeń.

### Workflow → Zadania  
- generowanie zadań na podstawie kroków.

### Workflow → Budżety  
- automatyczne aktualizacje kosztów.

### Workflow → Automatyzacje  
Workflow jest rozszerzeniem silnika IF→THEN.

---

## 🤖 Przykład workflow (JSON)

```json
{
  "name": "Onboarding klienta",
  "steps": [
    {
      "type": "crm.create",
      "params": { "segment": "premium" }
    },
    {
      "type": "projects.create",
      "params": { "template": "onboarding" }
    },
    {
      "type": "notifications.send",
      "params": { "template": "welcome_email" }
    }
  ]
}
```

---

## 📄 Dokumentacja powiązana

- **[moduł automatyzacje](modul_automatyzacje.md)**  
- **[moduł API](modul_api.md)**  
- **[moduł BI & AI](modul_bi_ai.md)**  
- **[moduł bezpieczeństwo](modul_bezpieczenstwo.md)**  

---

## 🏁 Status modułu

Moduł Workflow jest:

- opisany,  
- udokumentowany,  
- zgodny z architekturą,  
- gotowy do implementacji.
