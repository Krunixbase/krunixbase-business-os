# Stwórz własny moduł — Krunixbase Business OS

Ten dokument prowadzi krok po kroku przez proces tworzenia własnego modułu w Krunixbase Business OS: od nazwy, przez pliki, API, bazę danych, aż po dokumentację.

---

## 1. Nazwa modułu

**Krok 1:** wybierz nazwę modułu:

- krótka,
- biznesowa,
- jednoznaczna.

Przykłady:

- `lojalnosc` (program lojalnościowy)
- `magazyn` (gospodarka magazynowa)
- `subskrypcje` (abonamenty)
- `ankiety` (formularze i feedback)

---

## 2. Struktura plików

Załóż katalog w warstwie modułów:

```text
/src/modules/[nazwa_modulu]/
  index.ts
  service.ts
  controller.ts
  model.ts
  routes.ts
```

Dodaj dokumentację:

```text
/docs/system/modul_[nazwa_modulu].md
```

---

## 3. Baza danych

Zdefiniuj tabelę:

```sql
CREATE TABLE modul_[nazwa_modulu] (
  id UUID PRIMARY KEY,
  nazwa TEXT NOT NULL,
  status TEXT NOT NULL,
  created_at TIMESTAMP NOT NULL,
  updated_at TIMESTAMP NOT NULL
);
```

Jeśli potrzebujesz relacji:

```sql
ALTER TABLE modul_[nazwa_modulu]
ADD COLUMN owner_id UUID REFERENCES users(id);
```

---

## 4. API modułu

Dodaj endpointy:

```ts
// routes.ts
router.get('/api/[nazwa_modulu]/list', controller.list);
router.post('/api/[nazwa_modulu]/create', controller.create);
router.put('/api/[nazwa_modulu]/update/:id', controller.update);
router.delete('/api/[nazwa_modulu]/delete/:id', controller.remove);
```

---

## 5. Logika biznesowa

W `service.ts`:

- walidacja danych,
- reguły biznesowe,
- integracje z innymi modułami (np. CRM, Projekty, Budżety),
- obsługa statusów.

---

## 6. UI/UX

Dodaj widoki w warstwie UI:

```text
/src/ui/[nazwa_modulu]/
  ListView.tsx
  DetailView.tsx
  Form.tsx
```

Elementy:

- lista rekordów,
- formularz dodawania/edycji,
- szczegóły rekordu.

---

## 7. Automatyzacje IF→THEN

Zarejestruj wyzwalacze:

```json
{
  "trigger": "[nazwa_modulu].create",
  "action": "notifications.send",
  "params": {
    "template": "modul_[nazwa_modulu]_created"
  }
}
```

---

## 8. Dokumentacja modułu

Użyj szablonu:

```markdown
# Moduł [Nazwa Modułu] — Krunixbase Business OS

## Cele
- [Cel 1]
- [Cel 2]

## Funkcje
- [Funkcja 1]
- [Funkcja 2]

## Architektura
- UI/UX
- API
- Logika biznesowa
- Baza danych

## Powiązania
- [Moduł A] → [Nazwa Modułu]
- [Nazwa Modułu] → [Moduł B]

## Status
- opisany
- udokumentowany
- gotowy do implementacji
```

---

## 9. Rejestracja modułu w systemie

Dodaj moduł do rejestru:

```ts
// src/modules/index.ts
export const modules = [
  'crm',
  'projects',
  'budgets',
  '[nazwa_modulu]'
];
```

---

## 10. Checklist

- **Nazwa modułu** wybrana  
- **Tabela** utworzona  
- **API** dodane  
- **UI** przygotowane  
- **Automatyzacje** zarejestrowane  
- **Dokumentacja** w `/docs/system/modul_[nazwa_modulu].md`  
- **Moduł** dodany do rejestru

-
