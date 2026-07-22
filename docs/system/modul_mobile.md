# Moduł Mobile — Krunixbase Business OS (Android + iOS)

Moduł Mobile zapewnia dostęp do systemu Krunixbase Business OS z urządzeń mobilnych. Aplikacja mobilna jest kluczowym elementem pakietu KSeF Business oraz modułów operacyjnych, umożliwiając szybkie działania, powiadomienia push, skanowanie dokumentów oraz mobilny workflow.

---

## 1. Cele aplikacji mobilnej

- zapewnienie dostępu do systemu z dowolnego miejsca,
- obsługa procesów księgowych (KSeF) w czasie rzeczywistym,
- szybkie reagowanie na zadania i automatyzacje,
- skanowanie dokumentów papierowych,
- powiadomienia push o zdarzeniach systemowych,
- zwiększenie efektywności pracy zespołu.

---

## 2. Funkcje aplikacji mobilnej

### **Dashboard mobilny**
- podsumowanie dnia,
- powiadomienia,
- zadania,
- faktury KSeF,
- aktywności CRM.

### **Moduł KSeF Mobile**
- powiadomienia push o nowych fakturach,
- przegląd faktur,
- przypisywanie faktur do klientów,
- przypisywanie faktur do projektów,
- skanowanie dokumentów,
- zatwierdzanie faktur.

### **Moduł CRM Mobile**
- lista klientów,
- wyszukiwanie,
- statusy i etapy,
- aktywności,
- szybkie notatki.

### **Moduł Zadań Mobile**
- lista zadań,
- statusy,
- terminy,
- przypisania,
- komentarze.

### **Moduł Kampanii Mobile**
- podgląd kampanii,
- statystyki,
- aktywność klientów.

### **Powiadomienia push**
- nowe faktury,
- nowe zadania,
- zmiany statusów,
- automatyzacje IF→THEN,
- kampanie.

---

## 3. Architektura aplikacji mobilnej

### **Technologia**
- Android: Kotlin / Flutter / React Native,
- iOS: Swift / Flutter / React Native.

### **Warstwy**
- UI (interfejs mobilny),
- API (komunikacja z backendem),
- moduł offline (cache danych),
- moduł bezpieczeństwa (FaceID/TouchID),
- moduł skanowania dokumentów.

### **Komunikacja**
- HTTPS,
- tokeny dostępu,
- klucze API,
- szyfrowanie danych.

---

## 4. Integracje aplikacji mobilnej

### **Integracje systemowe**
- CRM,
- zadania,
- kampanie,
- automatyzacje IF→THEN,
- KSeF Business,
- raporty.

### **Integracje urządzenia**
- aparat (skanowanie dokumentów),
- galeria,
- FaceID / TouchID,
- powiadomienia push.

---

## 5. Workflow mobilny

### **Przykładowy workflow KSeF Mobile**
1. system pobiera fakturę z KSeF,  
2. aplikacja mobilna wysyła powiadomienie push,  
3. użytkownik otwiera fakturę,  
4. przypisuje ją do klienta,  
5. automatyzacja tworzy zadanie księgowe,  
6. użytkownik wykonuje zadanie w aplikacji mobilnej.

### **Przykładowy workflow operacyjny**
1. automatyzacja tworzy zadanie,  
2. użytkownik dostaje powiadomienie,  
3. wykonuje zadanie,  
4. zmienia status,  
5. CRM zapisuje aktywność.

---

## 6. Bezpieczeństwo aplikacji mobilnej

- FaceID / TouchID,
- szyfrowanie danych,
- szyfrowanie tokenów,
- izolacja środowisk,
- role i uprawnienia,
- logi działań,
- audyt zmian,
- monitoring API.

---

## 7. Raporty mobilne

- aktywność użytkowników,
- liczba wykonanych zadań,
- liczba przetworzonych faktur,
- statystyki modułów,
- raporty cykliczne.

---

## 8. Roadmap modułu Mobile

- tryb offline,
- skanowanie OCR faktur,
- integracje bankowe,
- moduł płatności,
- moduł rozliczeń,
- moduł partnerów,
- zaawansowane powiadomienia,
- moduł projektów mobilnych.

---

## 9. Status modułu Mobile

Moduł Mobile jest kluczowym elementem pakietu KSeF Business i stanowi rozszerzenie funkcjonalności panelu webowego. Aplikacja mobilna jest gotowa do wdrożenia w środowiskach produkcyjnych.

