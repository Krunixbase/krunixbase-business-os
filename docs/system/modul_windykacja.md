# Moduł Windykacja — Krunixbase Business OS

Moduł Windykacja umożliwia automatyczne monitorowanie zaległych płatności, wysyłanie przypomnień, generowanie działań windykacyjnych, analizę ryzyka finansowego oraz integrację z fakturami KSeF i modułem płatności. Stanowi kluczowy element pakietu Premium.

---

## 1. Cele modułu windykacji

- automatyzacja procesu windykacyjnego,
- monitorowanie zaległych płatności,
- integracja z fakturami KSeF,
- integracja z płatnościami online i bankowymi,
- minimalizacja zaległości finansowych,
- raportowanie ryzyka finansowego.

---

## 2. Funkcje modułu windykacji

### **Monitorowanie zaległości**
- wykrywanie zaległych faktur,
- statusy zaległości,
- priorytety zaległości,
- automatyczne alerty.

### **Przypomnienia i komunikacja**
- przypomnienia e-mail,
- przypomnienia SMS,
- przypomnienia automatyczne (IF→THEN),
- harmonogram przypomnień,
- szablony windykacyjne.

### **Działania windykacyjne**
- zadania windykacyjne,
- działania operacyjne,
- działania prawne (planowane),
- działania partnerskie.

### **Integracja z płatnościami**
- powiązanie zaległości z płatnościami online,
- powiązanie zaległości z transakcjami bankowymi,
- automatyczne aktualizacje statusów.

### **Analiza ryzyka finansowego**
- ryzyka zaległości,
- ryzyka klientów,
- ryzyka partnerów,
- predykcja zaległości (BI).

---

## 3. Struktura danych

### **Zaległość**
- ID zaległości,
- klient,
- faktura,
- kwota,
- termin płatności,
- dni opóźnienia,
- status,
- działania windykacyjne,
- historia komunikacji.

### **Działanie windykacyjne**
- typ działania,
- termin,
- status,
- powiązane zadanie,
- powiązana kampania.

---

## 4. Workflow windykacji

### **Przykładowy workflow operacyjny**
1. faktura KSeF przekracza termin płatności,  
2. system tworzy zaległość,  
3. automatyzacja wysyła przypomnienie,  
4. operator wykonuje zadanie windykacyjne,  
5. klient dokonuje płatności,  
6. status zaległości zmienia się na „opłacona”,  
7. budżet aktualizuje przychód.

### **Workflow automatyczny**
1. IF faktura nieopłacona 7 dni  
2. THEN wyślij przypomnienie e-mail  
3. THEN utwórz zadanie windykacyjne  
4. THEN wyślij SMS po 14 dniach  
5. THEN oznacz ryzyko finansowe.

---

## 5. Automatyzacje windykacji

Moduł windykacji współpracuje z silnikiem automatyzacji IF→THEN.

### **Przykłady automatyzacji**
- IF faktura nieopłacona → THEN utwórz zaległość,
- IF zaległość > 7 dni → THEN wyślij przypomnienie,
- IF zaległość > 14 dni → THEN wyślij SMS,
- IF zaległość > 30 dni → THEN utwórz ryzyko finansowe,
- IF płatność online → THEN zamknij zaległość,
- IF transakcja bankowa dopasowana → THEN aktualizuj status.

---

## 6. Integracje windykacji

### **Integracje systemowe**
- KSeF,
- Płatności,
- Budżety,
- Projekty,
- Partnerzy,
- Zadania,
- Kampanie,
- Automatyzacje IF→THEN,
- BI,
- Mobile.

### **Integracje zewnętrzne**
- operatorzy SMS,
- operatorzy e-mail,
- banki,
- systemy księgowe,
- API prawne (planowane).

---

## 7. Bezpieczeństwo windykacji

- role i uprawnienia,
- kontrola dostępu do zaległości,
- szyfrowanie danych finansowych,
- logi działań,
- audyt zmian,
- izolacja danych.

---

## 8. Raporty windykacji

- zaległości klientów,
- zaległości partnerów,
- zaległości projektów,
- skuteczność działań windykacyjnych,
- ryzyka finansowe,
- raporty cykliczne,
- raporty BI.

---

## 9. Roadmap modułu windykacji

- działania prawne,
- integracje kancelarii prawnych,
- windykacja automatyczna premium,
- windykacja partnerów,
- moduł prowizji windykacyjnych,
- predykcja zaległości (AI),
- moduł BI windykacji.

---

## 10. Status modułu windykacji

Moduł windykacji jest częścią pakietu Premium i stanowi kluczowy element finansowy systemu Krunixbase Business OS.

