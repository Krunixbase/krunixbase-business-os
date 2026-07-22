# Moduł Projekty — Krunixbase Business OS

Moduł projektów umożliwia zarządzanie pracą projektową, harmonogramami, zadaniami, etapami oraz powiązaniami z klientami, partnerami, ofertami i fakturami KSeF. Stanowi kluczowy element operacyjny systemu Krunixbase Business OS.

---

## 1. Cele modułu projektów

- organizacja pracy projektowej,
- zarządzanie etapami i harmonogramami,
- integracja projektów z CRM, ofertami i KSeF,
- monitorowanie postępu,
- automatyzacja działań projektowych,
- raportowanie wyników projektów.

---

## 2. Funkcje modułu projektów

### **Tworzenie projektów**
- kreator projektów,
- powiązanie z klientem,
- powiązanie z partnerem (opcjonalnie),
- powiązanie z ofertą,
- status projektu,
- priorytet projektu.

### **Etapy projektu**
- dodawanie etapów,
- statusy etapów,
- terminy etapów,
- przypisania użytkowników,
- automatyzacje etapów.

### **Zadania projektowe**
- zadania w ramach projektu,
- zadania cykliczne,
- zadania automatyczne (IF→THEN),
- zadania zależne.

### **Dokumenty projektowe**
- dokumenty ofertowe,
- dokumenty partnerskie,
- dokumenty księgowe (KSeF),
- notatki projektowe.

### **Powiązania**
- CRM → klient projektu,
- Oferty → oferta powiązana,
- Partnerzy → partner projektu,
- KSeF → faktury projektu,
- Zadania → zadania projektowe,
- Kampanie → kampanie projektowe.

---

## 3. Struktura danych

### **Projekt**
- ID projektu,
- nazwa projektu,
- klient,
- partner (opcjonalnie),
- oferta,
- status,
- priorytet,
- etapy,
- zadania,
- dokumenty,
- faktury KSeF,
- historia zmian.

### **Etap projektu**
- nazwa,
- status,
- termin,
- przypisany użytkownik,
- zadania w etapie.

### **Zadanie projektowe**
- nazwa,
- status,
- termin,
- przypisanie,
- powiązania.

---

## 4. Workflow projektów

### **Przykładowy workflow operacyjny**
1. klient akceptuje ofertę,  
2. automatyzacja tworzy projekt,  
3. projekt otrzymuje etapy,  
4. automatyzacja tworzy zadania projektowe,  
5. operator wykonuje zadania,  
6. etapy zmieniają status,  
7. projekt przechodzi do „w realizacji”,  
8. faktury KSeF przypisywane są do projektu,  
9. projekt przechodzi do „zakończony”.

### **Przykładowy workflow partnerski**
1. partner tworzy ofertę,  
2. oferta powiązana z projektem,  
3. projekt przypisany do partnera,  
4. automatyzacja tworzy zadania dla partnera,  
5. raport projektu generuje wyniki partnera.

---

## 5. Automatyzacje projektów

Moduł projektów współpracuje z silnikiem automatyzacji IF→THEN.

### **Przykłady automatyzacji**
- IF oferta zaakceptowana → THEN utwórz projekt,
- IF etap zakończony → THEN utwórz zadanie kolejnego etapu,
- IF faktura przypisana → THEN dodaj ją do projektu,
- IF projekt opóźniony → THEN wyślij powiadomienie,
- IF projekt zakończony → THEN wygeneruj raport.

---

## 6. Integracje projektów

### **Integracje systemowe**
- CRM,
- Oferty,
- Partnerzy,
- Zadania,
- Kampanie,
- Automatyzacje IF→THEN,
- KSeF,
- Raporty,
- Mobile.

### **Integracje zewnętrzne**
- e-mail,
- kalendarz,
- API partnerskie,
- systemy księgowe (planowane).

---

## 7. Bezpieczeństwo projektów

- role i uprawnienia,
- kontrola dostępu do projektów,
- logi działań,
- audyt zmian,
- izolacja danych,
- szyfrowanie dokumentów.

---

## 8. Raporty projektów

- statusy projektów,
- postęp etapów,
- zadania projektowe,
- opóźnienia,
- faktury KSeF projektu,
- skuteczność operatorów,
- skuteczność partnerów,
- raporty cykliczne.

---

## 9. Roadmap modułu projektów

- moduł projektów premium,
- wykresy Gantt,
- zależności między projektami,
- automatyczne harmonogramy,
- integracje księgowe,
- integracje bankowe (rozliczenia),
- moduł budżetów projektowych,
- moduł ryzyk projektowych.

---

## 10. Status modułu projektów

Moduł projektów jest gotowy do wdrożenia i stanowi kluczowy element operacyjny systemu Krunixbase Business OS.

