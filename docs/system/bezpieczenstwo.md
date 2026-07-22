# Bezpieczeństwo — Krunixbase Business OS

Dokument opisuje pełny model bezpieczeństwa systemu Krunixbase Business OS, obejmujący role, uprawnienia, izolację środowisk, szyfrowanie danych, logi, audyt, bezpieczeństwo API oraz politykę danych.

---

## 1. Założenia bezpieczeństwa

System został zaprojektowany zgodnie z zasadami:

- **izolacji środowisk** — każde wdrożenie działa na osobnym serwerze i bazie danych,
- **minimalnych uprawnień** — użytkownicy mają dostęp tylko do niezbędnych funkcji,
- **pełnej audytowalności** — wszystkie działania są logowane,
- **szyfrowania danych** — dane wrażliwe są szyfrowane,
- **bezpieczeństwa API** — klucze, limity, monitoring,
- **kontroli dostępu** — role, uprawnienia, tokeny,
- **zgodności z dobrymi praktykami branżowymi**.

---

## 2. Role i uprawnienia

System posiada hierarchię ról:

### **Administrator**
- pełny dostęp do systemu,
- zarządzanie użytkownikami,
- konfiguracja modułów,
- dostęp do logów i audytu.

### **Manager**
- dostęp do CRM,
- dostęp do kampanii,
- dostęp do zadań,
- dostęp do raportów,
- brak dostępu do ustawień systemowych.

### **Operator**
- wykonywanie zadań,
- obsługa klientów,
- dostęp do kampanii,
- brak dostępu do konfiguracji.

### **Księgowość**
- dostęp do modułu KSeF,
- dostęp do faktur,
- brak dostępu do kampanii i automatyzacji.

### **Gość**
- dostęp tylko do wybranych modułów,
- brak możliwości edycji.

---

## 3. Izolacja środowisk

Każde wdrożenie systemu posiada:

- osobny serwer,
- osobną bazę danych,
- osobne klucze API,
- osobne logi,
- osobne role i uprawnienia.

System jest **całkowicie odseparowany** od innych wdrożeń oraz od środowisk SeedTools/Krunixbase.

---

## 4. Szyfrowanie danych

System stosuje:

- szyfrowanie danych wrażliwych,
- szyfrowanie tokenów,
- szyfrowanie kluczy API,
- szyfrowanie połączeń (HTTPS),
- szyfrowanie danych w spoczynku (at-rest).

---

## 5. Logi i audyt

System loguje:

- logowania,
- działania użytkowników,
- zmiany danych,
- działania automatyzacji,
- błędy systemowe,
- integracje API,
- operacje KSeF.

Logi są przechowywane w izolowanym środowisku i dostępne tylko dla administratorów.

---

## 6. Bezpieczeństwo API

API systemu posiada:

- klucze API,
- tokeny dostępu,
- limity zapytań,
- monitoring ruchu,
- logi integracji,
- izolację środowisk,
- kontrolę dostępu.

Każda integracja działa przez osobny adapter API.

---

## 7. Polityka danych

System zapewnia:

- pełną kontrolę nad danymi,
- możliwość eksportu danych,
- możliwość usuwania danych,
- izolację danych między użytkownikami,
- brak współdzielenia danych między firmami.

---

## 8. Ryzyka i działania zapobiegawcze

### **Ryzyko: nieautoryzowany dostęp**
- działanie: role, uprawnienia, tokeny.

### **Ryzyko: błędne automatyzacje**
- działanie: testy IF→THEN przed uruchomieniem.

### **Ryzyko: błędy integracji**
- działanie: logi integracji + monitoring API.

### **Ryzyko: utrata danych**
- działanie: backupy + izolacja środowisk.

---

## 9. Monitoring

System posiada:

- monitoring API,
- monitoring automatyzacji,
- monitoring błędów,
- monitoring integracji,
- monitoring KSeF.

---

## 10. Status bezpieczeństwa

System jest gotowy do wdrożenia w środowiskach produkcyjnych i spełnia standardy bezpieczeństwa wymagane w systemach operacyjnych dla firm.

