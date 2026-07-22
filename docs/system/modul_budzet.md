# Moduł Budżet — Krunixbase Business OS

Moduł Budżet umożliwia zarządzanie budżetami projektów, kosztami, przychodami, rentownością oraz integracją z fakturami KSeF. Stanowi kluczowy element analityczny i finansowy systemu Krunixbase Business OS, dostępny w pakiecie Premium.

---

## 1. Cele modułu budżetów

- kontrola kosztów projektowych,
- monitorowanie przychodów,
- analiza rentowności,
- integracja z fakturami KSeF,
- automatyzacja działań finansowych,
- raportowanie wyników finansowych.

---

## 2. Funkcje modułu budżetów

### **Budżety projektowe**
- tworzenie budżetu projektu,
- planowane koszty,
- planowane przychody,
- rzeczywiste koszty,
- rzeczywiste przychody,
- rentowność projektu.

### **Koszty**
- koszty operacyjne,
- koszty partnerów,
- koszty materiałów,
- koszty usług,
- koszty cykliczne.

### **Przychody**
- przychody z ofert,
- przychody z faktur KSeF,
- przychody cykliczne,
- przychody projektowe.

### **Integracja z KSeF**
- przypisywanie faktur do budżetu,
- automatyczne aktualizacje kosztów,
- automatyczne aktualizacje przychodów,
- statusy faktur w budżecie.

### **Analiza finansowa**
- rentowność,
- odchylenia,
- prognozy,
- raporty finansowe.

---

## 3. Struktura danych

### **Budżet projektu**
- ID budżetu,
- projekt,
- koszty planowane,
- koszty rzeczywiste,
- przychody planowane,
- przychody rzeczywiste,
- rentowność,
- faktury KSeF,
- historia zmian.

### **Pozycja budżetowa**
- typ (koszt / przychód),
- kwota,
- opis,
- powiązana faktura,
- powiązany etap,
- powiązane zadanie.

---

## 4. Workflow budżetów

### **Przykładowy workflow finansowy**
1. projekt utworzony,  
2. automatyzacja tworzy budżet projektu,  
3. operator dodaje koszty planowane,  
4. oferta zaakceptowana → przychód planowany,  
5. faktura KSeF przypisana → koszt rzeczywisty,  
6. faktura sprzedażowa → przychód rzeczywisty,  
7. raport budżetu generuje rentowność.

### **Workflow automatyczny**
1. IF faktura przypisana do projektu  
2. THEN dodaj ją do budżetu jako koszt/przychód  
3. THEN aktualizuj rentowność  
4. THEN wyślij powiadomienie do managera.

---

## 5. Automatyzacje budżetów

Moduł budżetów współpracuje z silnikiem automatyzacji IF→THEN.

### **Przykłady automatyzacji**
- IF faktura przypisana → THEN dodaj ją do budżetu,
- IF koszt przekroczy plan → THEN utwórz zadanie „analiza kosztów”,
- IF projekt osiągnie rentowność X% → THEN wyślij raport,
- IF przychód z oferty → THEN dodaj przychód planowany,
- IF etap zakończony → THEN aktualizuj koszty etapu.

---

## 6. Integracje budżetów

### **Integracje systemowe**
- Projekty,
- Oferty,
- Partnerzy,
- Zadania,
- Automatyzacje IF→THEN,
- KSeF,
- Raporty.

### **Integracje zewnętrzne**
- systemy księgowe (planowane),
- banki (planowane),
- API finansowe (planowane).

---

## 7. Bezpieczeństwo budżetów

- role i uprawnienia,
- kontrola dostępu do budżetów,
- szyfrowanie danych finansowych,
- logi działań,
- audyt zmian,
- izolacja danych.

---

## 8. Raporty budżetów

- koszty projektów,
- przychody projektów,
- rentowność,
- odchylenia,
- prognozy,
- raporty cykliczne,
- raporty partnerów.

---

## 9. Roadmap modułu budżetów

- integracje bankowe,
- moduł płatności,
- moduł rozliczeń,
- budżety cykliczne,
- budżety partnerów,
- moduł BI finansowy,
- predykcja kosztów i przychodów,
- automatyczne prognozy.

---

## 10. Status modułu budżetów

Moduł budżetów jest częścią pakietu Premium i stanowi kluczowy element finansowy systemu Krunixbase Business OS.

