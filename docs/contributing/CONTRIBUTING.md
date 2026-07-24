# **KRUNIXBASE Business OS — Contribution Guidelines**

---

## 🧩 1. Wprowadzenie  
Dziękujemy za zainteresowanie kontrybucją do **KRUNIXBASE Business OS** — deterministycznego systemu operacyjnego dla biznesu.  
Ten dokument opisuje zasady współpracy, standardy techniczne oraz procesy, które zapewniają:

- spójność kodu,  
- bezpieczeństwo,  
- deterministyczne działanie,  
- pełną audytowalność,  
- zgodność z licencjami open‑source.

KRUNIXBASE jest projektem modularnym, deterministycznym i w pełni transparentnym.

---

## 📁 2. Struktura repozytorium  
Repozytorium KRUNIXBASE jest podzielone na logiczne sekcje:

- `docs/architecture/` — **Architecture**  
- `docs/modules/` — **Modules**  
- `docs/security/` — **Security**  
- `docs/workflow/` — **Deterministic Workflow**  
- `docs/contributing/` — **CONTRIBUTING.md**  
- `docs/roadmap/` — **Roadmap**  
- `docs/branding/` — **Branding Package**  
- `system/` — Core, API, Events, Modules  
- `src/` — implementacje modułów  

Każdy kontrybutor powinien zapoznać się z dokumentacją przed rozpoczęciem pracy.

---

## 🔄 3. Zasady kontrybucji  
Kontrybucje muszą być:

- deterministyczne,  
- modularne,  
- zgodne z API Core,  
- w pełni logowane,  
- zgodne z licencjami,  
- testowalne,  
- audytowalne.

KRUNIXBASE nie akceptuje:

- kodu losowego,  
- ukrytych stanów,  
- niejawnych efektów ubocznych,  
- nieudokumentowanych zmian.

---

## 🧱 4. Jak zgłosić zmianę (PR Workflow)

### **4.1 Fork repozytorium**  
Utwórz własny fork projektu.

### **4.2 Utwórz branch**  
Nazewnictwo:

```
feature/<nazwa>
fix/<nazwa>
docs/<nazwa>
refactor/<nazwa>
```

### **4.3 Wprowadź zmiany**  
Zmiany muszą być:

- deterministyczne,  
- zgodne z modułem,  
- zgodne z dokumentacją,  
- zgodne z API Core.

### **4.4 Dodaj testy**  
Każda zmiana musi posiadać testy deterministyczne.

### **4.5 Utwórz Pull Request**  
PR musi zawierać:

- opis zmiany,  
- powód zmiany,  
- moduł, którego dotyczy,  
- wpływ na workflow,  
- wpływ na bezpieczeństwo,  
- linki do dokumentacji.

---

## 🔍 5. Zgłaszanie błędów  
Błędy zgłaszamy przez Issues.

Każdy zgłoszony błąd musi zawierać:

- moduł,  
- opis,  
- kroki reprodukcji,  
- oczekiwany wynik,  
- rzeczywisty wynik,  
- wpływ na deterministyczność.

---

## 🔐 6. Standardy bezpieczeństwa  
Kontrybucje muszą być zgodne z:

- deterministycznym modelem bezpieczeństwa,  
- zasadami walidacji danych,  
- zasadami izolacji modułów,  
- zasadami audytowalności.

Nie wolno:

- dodawać losowości,  
- dodawać ukrytych stanów,  
- modyfikować danych innych modułów bez API.

---

## 📜 7. Licencjonowanie  
KRUNIXBASE używa:

- **GPL‑3.0** — kod źródłowy,  
- **AGPL‑3.0** — komponenty sieciowe,  
- **CC‑BY‑4.0** — dokumentacja i branding.

Kontrybucje muszą być zgodne z tymi licencjami.

---

## 🧭 8. Roadmap kontrybucji  
Obszary, w których kontrybutorzy są szczególnie mile widziani:

- moduły rozszerzeń,  
- integracje partnerów,  
- automatyzacje,  
- workflow designer,  
- deterministic webhooks,  
- partner API v2,  
- dokumentacja techniczna.

---

## 💬 9. Kontakt  
Wszelkie pytania dotyczące kontrybucji można kierować przez Issues lub PR.
