# Moduł Automatyzacje — Krunixbase Business OS

Moduł automatyzacji jest centralnym elementem systemu Krunixbase Business OS. Umożliwia tworzenie reguł IF→THEN, które automatyzują działania operacyjne, marketingowe, projektowe oraz finansowe.
Silnik automatyzacji działa w czasie rzeczywistym i jest w pełni zintegrowany z CRM, kampaniami, zadaniami, raportami oraz modułem KSeF.

---

## 1. Cele modułu automatyzacji

- automatyzacja powtarzalnych procesów,
- eliminacja ręcznych działań,
- zwiększenie efektywności operacyjnej,
- integracja działań między modułami,
- tworzenie inteligentnych workflow,
- reagowanie na zdarzenia w czasie rzeczywistym.

---

## 2. Model automatyzacji IF → THEN

Silnik automatyzacji działa według schematu:

```
IF (warunek) THEN (akcja)
```

Każda automatyzacja składa się z:

- **warunku (IF)** — zdarzenie, status, etap, czas, aktywność,
- **akcji (THEN)** — zadanie, e-mail, kampania, zmiana statusu, integracja,
- **opcjonalnych filtrów** — segmenty, tagi, role,
- **opcjonalnych opóźnień** — np. wykonaj po 2 godzinach.

---

## 3. Typy warunków (IF)

### **Warunki CRM**
- klient dodany,
- klient zmienił status,
- klient zmienił etap,
- klient nieaktywny X dni,
- dodano aktywność.

### **Warunki kampanii**
- kampania zakończona,
- klient otworzył e-mail,
- klient kliknął link,
- klient wypisał się z kampanii.

### **Warunki zadań**
- zadanie utworzone,
- zadanie zakończone,
- zadanie opóźnione.

### **Warunki KSeF**
- faktura pobrana,
- faktura wystawiona,
- faktura zmieniła status.

### **Warunki czasowe**
- codziennie o godzinie X,
- co tydzień,
- co miesiąc,
- po X godzinach.

---

## 4. Typy akcji (THEN)

### **Akcje CRM**
- zmiana statusu,
- zmiana etapu,
- przypisanie operatora,
- dodanie aktywności.

### **Akcje kampanii**
- wysyłka kampanii,
- wysyłka e-mail,
- wysyłka SMS.

### **Akcje zadań**
- utworzenie zadania,
- przypisanie zadania,
- zmiana statusu zadania.

### **Akcje KSeF**
- pobranie faktur,
- przypisanie faktury do klienta,
- utworzenie zadania księgowego.

### **Akcje systemowe**
- webhook,
- API,
- powiadomienie,
- raport.

---

## 5. Przykłady automatyzacji

### **Automatyzacja powitalna**
```
IF klient dodany
THEN wyślij kampanię powitalną
```

### **Automatyzacja ofertowa**
```
IF klient przejdzie do etapu "oferta"
THEN utwórz zadanie "przygotuj ofertę"
```

### **Automatyzacja reaktywacyjna**
```
IF klient nieaktywny 30 dni
THEN wyślij kampanię reaktywacyjną
```

### **Automatyzacja KSeF**
```
IF faktura pobrana
THEN przypisz zadanie "sprawdź fakturę"
```

### **Automatyzacja marketingowa**
```
IF kampania zakończona
THEN utwórz raport kampanii
```

---

## 6. Workflow automatyzacji

### **Przykładowy workflow**
1. klient zmienia status,  
2. automatyzacja IF→THEN uruchamia akcję,  
3. system tworzy zadanie,  
4. operator wykonuje zadanie,  
5. automatyzacja reaguje na zakończenie zadania,  
6. system wysyła kampanię,  
7. CRM zapisuje aktywność,  
8. raport generuje statystyki.

---

## 7. Integracje automatyzacji

### **Integracje systemowe**
- CRM,
- kampanie,
- zadania,
- raporty,
- KSeF.

### **Integracje zewnętrzne**
- e-mail,
- SMS,
- social media,
- webhooki,
- API partnerskie.

---

## 8. Bezpieczeństwo automatyzacji

- role i uprawnienia,
- logi automatyzacji,
- audyt działań,
- kontrola dostępu do reguł,
- izolacja środowisk,
- monitoring błędów.

---

## 9. Raporty automatyzacji

- liczba uruchomień,
- skuteczność automatyzacji,
- błędy automatyzacji,
- czas wykonania,
- statystyki modułów.

---

## 10. Roadmap modułu automatyzacji

- automatyzacje wieloetapowe,
- automatyzacje cykliczne,
- automatyzacje projektowe,
- automatyzacje finansowe,
- automatyzacje partnerów,
- automatyzacje social media,
- moduł sekwencji automatycznych.

---

## 11. Status modułu automatyzacji

Moduł automatyzacji jest w pełni gotowy do wdrożenia i stanowi kluczowy element systemu Krunixbase Business OS.

```

---
