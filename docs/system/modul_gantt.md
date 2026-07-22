# Moduł Gantt — Krunixbase Business OS

Moduł Gantt umożliwia wizualizację projektów, etapów i zadań w formie wykresów Gantta. Stanowi rozszerzenie modułu projektów i budżetów, zapewniając pełną kontrolę nad harmonogramami, zależnościami oraz obciążeniem zespołu.

---

## 1. Cele modułu Gantt

- wizualizacja harmonogramów projektowych,
- kontrola zależności między zadaniami,
- monitorowanie postępu etapów,
- analiza obciążenia zespołu,
- integracja z budżetami i KSeF,
- automatyzacja działań projektowych.

---

## 2. Funkcje modułu Gantt

### **Wykresy projektowe**
- wizualizacja całego projektu,
- etapy projektu,
- zadania projektowe,
- zależności między zadaniami,
- statusy etapów i zadań.

### **Zarządzanie harmonogramem**
- edycja terminów,
- przesuwanie zadań,
- automatyczne aktualizacje etapów,
- automatyczne aktualizacje budżetu.

### **Zależności**
- zależności typu „start → start”,
- zależności typu „start → koniec”,
- zależności typu „koniec → koniec”,
- zależności między projektami (planowane).

### **Obciążenie zespołu**
- przypisania użytkowników,
- analiza obciążenia,
- wykrywanie przeciążeń,
- rekomendacje automatyczne (planowane).

### **Integracja z budżetami**
- koszty etapów,
- koszty zadań,
- aktualizacja budżetu na podstawie harmonogramu.

---

## 3. Struktura danych

### **Wykres Gantt**
- projekt,
- etapy,
- zadania,
- zależności,
- terminy,
- statusy,
- powiązania z budżetem,
- powiązania z fakturami KSeF.

### **Zależność**
- typ zależności,
- zadanie źródłowe,
- zadanie docelowe,
- opóźnienie (lag),
- priorytet.

---

## 4. Workflow Gantt

### **Przykładowy workflow projektowy**
1. projekt utworzony,  
2. etapy dodane,  
3. zadania przypisane do etapów,  
4. wykres Gantt generuje harmonogram,  
5. operator przesuwa zadanie,  
6. etap aktualizuje termin,  
7. budżet aktualizuje koszty,  
8. automatyzacja tworzy zadanie „analiza opóźnień”.

### **Workflow automatyczny**
1. IF zadanie opóźnione  
2. THEN przesunięcie zależnych zadań  
3. THEN aktualizacja etapu  
4. THEN aktualizacja budżetu  
5. THEN powiadomienie managera.

---

## 5. Automatyzacje Gantt

Moduł Gantt współpracuje z silnikiem automatyzacji IF→THEN.

### **Przykłady automatyzacji**
- IF zadanie przesunięte → THEN aktualizuj etap,
- IF etap przesunięty → THEN aktualizuj budżet,
- IF projekt opóźniony → THEN utwórz zadanie „analiza opóźnień”,
- IF zależność naruszona → THEN wyślij powiadomienie,
- IF faktura KSeF przypisana → THEN aktualizuj koszty etapu.

---

## 6. Integracje Gantt

### **Integracje systemowe**
- Projekty,
- Zadania,
- Etapy,
- Budżety,
- Partnerzy,
- Automatyzacje IF→THEN,
- KSeF,
- Raporty,
- Mobile.

### **Integracje zewnętrzne**
- kalendarz,
- systemy projektowe (planowane),
- API partnerskie.

---

## 7. Bezpieczeństwo Gantt

- role i uprawnienia,
- kontrola dostępu do projektów,
- logi działań,
- audyt zmian,
- izolacja danych,
- szyfrowanie dokumentów projektowych.

---

## 8. Raporty Gantt

- opóźnienia projektów,
- statusy etapów,
- obciążenie zespołu,
- zależności krytyczne,
- koszty etapów,
- koszty zadań,
- rentowność projektów.

---

## 9. Roadmap modułu Gantt

- zależności między projektami,
- automatyczne harmonogramy,
- predykcja opóźnień,
- integracje księgowe,
- integracje bankowe,
- moduł BI projektowy,
- wykresy krytycznej ścieżki (CPM),
- automatyczne rekomendacje harmonogramu.

---

## 10. Status modułu Gantt

Moduł Gantt jest częścią pakietu Premium i stanowi kluczowy element zarządzania projektami w systemie Krunixbase Business OS.

