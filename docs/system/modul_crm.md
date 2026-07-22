# Moduł CRM — Krunixbase Business OS

Moduł CRM jest centralnym elementem systemu Krunixbase Business OS. Odpowiada za zarządzanie klientami, kontaktami, historią działań, segmentacją oraz integracją z pozostałymi modułami systemu.

---

## 1. Cele modułu CRM

- pełna kontrola nad klientami,
- zarządzanie relacjami,
- segmentacja klientów,
- historia kontaktu,
- automatyzacje operacyjne,
- integracja z kampaniami, zadaniami i raportami.

---

## 2. Funkcje modułu CRM

### **Zarządzanie klientami**
- dodawanie klientów,
- edycja danych,
- statusy klientów,
- etapy procesu,
- tagi i segmenty.

### **Historia kontaktu**
- notatki,
- aktywności,
- wiadomości e-mail,
- zadania powiązane,
- kampanie powiązane.

### **Segmentacja**
- segmenty ręczne,
- segmenty automatyczne,
- filtry dynamiczne,
- grupowanie klientów.

### **Statusy i etapy**
- statusy klientów (np. nowy, aktywny, nieaktywny),
- etapy procesu (np. kontakt, oferta, decyzja),
- automatyczne przejścia między etapami.

### **Powiązania**
- powiązane zadania,
- powiązane kampanie,
- powiązane automatyzacje,
- powiązane faktury (KSeF).

---

## 3. Struktura danych

### **Klient**
- ID klienta,
- imię i nazwisko / nazwa firmy,
- dane kontaktowe,
- status,
- etap,
- tagi,
- segmenty,
- historia kontaktu,
- powiązane zadania,
- powiązane kampanie,
- powiązane faktury.

### **Aktywność**
- typ aktywności,
- data,
- użytkownik,
- opis,
- powiązany klient.

### **Segment**
- nazwa segmentu,
- typ segmentu (ręczny / automatyczny),
- warunki segmentacji.

---

## 4. Workflow CRM

### **Przykładowy workflow klienta**
1. klient dodany do CRM,  
2. przypisany status „nowy”,  
3. automatyzacja tworzy zadanie „kontakt”,  
4. operator wykonuje kontakt,  
5. status zmienia się na „w trakcie”,  
6. kampania wysyła e-mail powitalny,  
7. klient przechodzi do etapu „oferta”,  
8. automatyzacja tworzy zadanie „przygotuj ofertę”,  
9. klient przechodzi do etapu „decyzja”.

---

## 5. Automatyzacje CRM

Moduł CRM współpracuje z silnikiem automatyzacji IF→THEN.

### **Przykłady automatyzacji**
- IF klient zmieni status → THEN wyślij e-mail,
- IF klient przejdzie do etapu „oferta” → THEN utwórz zadanie,
- IF klient doda aktywność → THEN przypisz operatora,
- IF klient nieaktywny 30 dni → THEN wyślij kampanię reaktywacyjną.

---

## 6. Integracje CRM

### **Integracje systemowe**
- kampanie marketingowe,
- zadania i workflow,
- automatyzacje IF→THEN,
- raporty,
- KSeF Business.

### **Integracje zewnętrzne**
- e-mail,
- kalendarz,
- social media,
- API partnerskie.

---

## 7. Bezpieczeństwo CRM

- role i uprawnienia,
- logi działań,
- audyt zmian,
- izolacja danych,
- szyfrowanie danych kontaktowych,
- kontrola dostępu do klientów.

---

## 8. Raporty CRM

- liczba klientów,
- statusy klientów,
- etapy procesu,
- aktywności,
- segmenty,
- skuteczność kampanii,
- skuteczność automatyzacji.

---

## 9. Roadmap modułu CRM

- tagi klientów,
- scoring klientów,
- segmenty automatyczne,
- automatyczne przypisania operatorów,
- integracje social media,
- moduł leadów,
- moduł partnerów.

---

## 10. Status modułu CRM

Moduł CRM jest w pełni gotowy do wdrożenia i stanowi centralny element systemu Krunixbase Business OS.

