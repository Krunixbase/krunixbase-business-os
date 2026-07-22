# Moduł KSeF Business — Krunixbase Business OS

Moduł KSeF Business umożliwia pełną integrację z Krajowym Systemem e-Faktur (KSeF). Odpowiada za pobieranie, wystawianie, analizę oraz przypisywanie faktur do klientów i zadań. Jest w pełni zintegrowany z CRM, zadaniami, automatyzacjami IF→THEN oraz raportami.

---

## 1. Cele modułu KSeF

- automatyzacja procesów księgowych,
- pobieranie faktur z KSeF,
- wystawianie faktur,
- przypisywanie faktur do klientów,
- tworzenie zadań księgowych,
- integracja z workflow operacyjnym,
- pełna audytowalność działań.

---

## 2. Funkcje modułu KSeF

### **Pobieranie faktur**
- pobieranie faktur z KSeF,
- pobieranie faktur cykliczne,
- pobieranie faktur automatyczne (IF→THEN),
- filtrowanie faktur.

### **Wystawianie faktur**
- wystawianie faktur sprzedażowych,
- wystawianie faktur korekt,
- integracja z CRM,
- integracja z projektami.

### **Przypisywanie faktur**
- przypisanie faktury do klienta,
- przypisanie faktury do projektu,
- przypisanie faktury do zadania.

### **Statusy faktur**
- pobrana,
- wystawiona,
- oczekująca,
- odrzucona,
- przetworzona.

### **Analiza faktur**
- podsumowania,
- statystyki,
- raporty,
- integracja z modułem raportów.

---

## 3. Przepływ danych KSeF

### **Przykładowy przepływ**
1. system pobiera faktury z KSeF,  
2. faktury trafiają do modułu KSeF Business,  
3. automatyzacja przypisuje fakturę do klienta,  
4. automatyzacja tworzy zadanie księgowe,  
5. operator wykonuje zadanie,  
6. raport generuje statystyki.

---

## 4. Automatyzacje KSeF

Moduł KSeF współpracuje z silnikiem automatyzacji IF→THEN.

### **Przykłady automatyzacji**
- IF faktura pobrana → THEN przypisz zadanie „sprawdź fakturę”,
- IF faktura wystawiona → THEN wyślij e-mail do klienta,
- IF faktura zmieni status → THEN utwórz aktywność w CRM,
- IF faktura przypisana → THEN dodaj ją do projektu.

---

## 5. Integracje KSeF

### **Integracje systemowe**
- CRM,
- zadania,
- automatyzacje IF→THEN,
- raporty,
- projekty.

### **Integracje zewnętrzne**
- API KSeF,
- systemy księgowe,
- banki (planowane).

---

## 6. Bezpieczeństwo KSeF

- szyfrowanie danych faktur,
- szyfrowanie tokenów KSeF,
- izolacja środowisk,
- role i uprawnienia,
- logi działań,
- audyt zmian,
- monitoring API KSeF.

---

## 7. Raporty KSeF

- liczba faktur,
- statusy faktur,
- faktury przypisane,
- faktury nieprzypisane,
- statystyki księgowe,
- raporty cykliczne.

---

## 8. Wymagania mobilne modułu KSeF

Moduł KSeF Business wymaga dedykowanej aplikacji mobilnej na Android oraz iOS. Aplikacja mobilna zapewnia:

- powiadomienia push o nowych fakturach,
- szybkie zatwierdzanie i przypisywanie faktur,
- skanowanie dokumentów papierowych,
- mobilny workflow księgowy,
- dostęp zabezpieczony FaceID/TouchID,
- integrację z modułem zadań i automatyzacjami.

Aplikacja mobilna jest kluczowym elementem pakietu KSeF Business i stanowi rozszerzenie funkcjonalności panelu webowego.

---

## 9. Roadmap modułu KSeF

- automatyczne przypisania faktur,
- integracje z systemami księgowymi,
- integracje bankowe,
- moduł płatności,
- moduł rozliczeń,
- zaawansowane raporty finansowe.

---

## 10. Status modułu KSeF

Moduł KSeF Business jest w pełni gotowy do wdrożenia i stanowi kluczowy element finansowy systemu Krunixbase Business OS.

