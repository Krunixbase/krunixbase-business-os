# Moduły Systemu — Krunixbase Business OS
## Wersja 1.0 — 2026

Dokument przedstawia pełną listę modułów Krunixbase Business OS wraz z ich opisem, przeznaczeniem, funkcjami oraz powiązaniami.  
System składa się z modułów podstawowych, finansowych, premium oraz integracyjnych.

---

# 1. Moduły podstawowe

## 1.1 CRM
Zarządzanie klientami, kontaktami, historią aktywności i relacjami biznesowymi.

## 1.2 Kampanie
Planowanie i realizacja kampanii marketingowych oraz komunikacyjnych.

## 1.3 Zadania
Zarządzanie zadaniami, statusami, priorytetami i przypisaniami.

## 1.4 Projekty
Moduł do prowadzenia projektów, etapów, harmonogramów i zasobów.

## 1.5 Oferty
Tworzenie ofert handlowych, wycen i propozycji dla klientów.

## 1.6 Partnerzy
Zarządzanie partnerami biznesowymi, dostawcami i kontrahentami.

## 1.7 Kalendarz
Widok kalendarza, wydarzeń, spotkań i terminów.

## 1.8 Powiadomienia
System powiadomień, alertów i komunikatów systemowych.

---

# 2. Moduły finansowe

## 2.1 KSeF
Integracja z Krajowym Systemem e‑Faktur, import, statusy, dokumenty.

## 2.2 Budżety
Zarządzanie kosztami, przychodami, marżami i budżetami projektów.

## 2.3 Płatności
Obsługa płatności online, bankowych, przypisywanie do faktur.

## 2.4 Rozliczenia
Automatyczne rozliczanie faktur, płatności i dokumentów finansowych.

## 2.5 Windykacja
Monitorowanie zaległości, działania windykacyjne, statusy ryzyka.

---

# 3. Moduły premium

## 3.1 Gantt
Zaawansowany wykres Gantta dla projektów, etapów i harmonogramów.

## 3.2 Ryzyka
Analiza ryzyk projektowych, scoring, statusy i działania.

## 3.3 BI
Dashboardy, wykresy, raporty, metryki i analityka biznesowa.

## 3.4 AI Predykcja
Prognozy, modele predykcyjne, analiza danych historycznych.

## 3.5 AI Rekomendacje
Rekomendacje działań, klientów, projektów i priorytetów.

---

# 4. Moduły integracyjne

## 4.1 Integracje
Integracje z API partnerów, ERP, bankami, systemami marketingowymi.

## 4.2 Mobile
Warstwa mobilna systemu — aplikacja, API mobilne, responsywność.

## 4.3 Automatyzacje
System IF→THEN, wyzwalacze, akcje, logi automatyzacji.

---

# 5. Powiązania między modułami

### CRM → Projekty  
Klient tworzy projekt, projekt dziedziczy dane kontaktowe.

### Projekty → Budżety  
Budżet powiązany z projektem, koszty i przychody.

### KSeF → Płatności  
Faktura → płatność, automatyczne aktualizacje statusów.

### Płatności → Rozliczenia  
Płatność → rozliczenie, automatyczne przypisanie.

### Automatyzacje → Wszystkie moduły  
Wyzwalacze IF→THEN, akcje systemowe.

---

# 6. Status modułów

Wszystkie moduły Krunixbase Business OS są:
- opisane,
- udokumentowane,
- powiązane architektonicznie,
- gotowe do implementacji,
- gotowe do rozwoju open‑source.

---

# 7. Dokumenty powiązane

- **[Architektura](modul_architektura.md)**  
- **[Whitepaper](whitepaper.md)**  
- **[README premium](README_premium.md)**  
- **[Brandbook](brandbook.md)** 
- **[Moduł API](modul_api.md)**  
- **[Moduł Baza Danych](modul_baza_danych.md)**  
- **[Moduł Deployment](modul_deployment.md)**
- **[Moduł DevOps](modul_devops.md)**  
- **[Moduł Testy](modul_testy.md)**  
- **[Moduł UI/UX](modul_ui_ux.md)**

---

# 8. Podsumowanie

Dokument **moduly_systemu.md** stanowi centralny spis wszystkich modułów Krunixbase Business OS.  
Jest fundamentem dla architektury, dokumentacji, roadmapy oraz rozwoju systemu.

