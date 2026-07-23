# **Moduł Bezpieczeństwo — Krunixbase Business OS**

Bezpieczeństwo jest fundamentem Krunixbase Business OS.  
Moduł bezpieczeństwa zapewnia ochronę danych, kontrolę dostępu, audyt działań oraz zgodność z wymaganiami prawnymi.

---

## 🔐 Zakres modułu

- ochrona danych użytkowników  
- kontrola dostępu i uprawnień  
- szyfrowanie komunikacji  
- audyt działań  
- logi bezpieczeństwa  
- zgodność z RODO  
- integracja z systemami monitoringu  

---

## 🛡️ 1. Warstwa komunikacji

### **TLS 1.3**
Wszystkie połączenia są zabezpieczone protokołem TLS 1.3.

### **Szyfrowanie danych**
- szyfrowanie danych w tranzycie  
- szyfrowanie danych w spoczynku (at‑rest)  
- szyfrowanie kluczy API  

---

## 👥 2. Role i uprawnienia

System posiada hierarchiczny model uprawnień:

- **Administrator** — pełny dostęp  
- **Manager** — dostęp operacyjny  
- **Użytkownik** — dostęp ograniczony  
- **Gość** — dostęp tylko do wybranych modułów  

Uprawnienia można nadawać:

- globalnie  
- per moduł  
- per rekord  
- per akcja  

---

## 📜 3. Audyt działań

Każda akcja w systemie jest rejestrowana:

- logi operacyjne  
- logi bezpieczeństwa  
- logi API  
- logi automatyzacji  
- logi zmian danych  

Przykład wpisu audytu:

```
[2026-07-23 14:12:55] USER: 1029
ACTION: projects.update
TARGET: project_id=88
STATUS: success
```

---

## 🧩 4. Powiązania z modułami

### Bezpieczeństwo → API  
Autoryzacja tokenowa, walidacja, rate‑limits.

### Bezpieczeństwo → Automatyzacje  
Kontrola, które automatyzacje mogą działać na danych.

### Bezpieczeństwo → Baza danych  
Szyfrowanie, indeksy bezpieczeństwa, kontrola dostępu.

### Bezpieczeństwo → UI  
Ukrywanie elementów interfejsu na podstawie roli.

---

## 🗄️ 5. Architektura modułu

### Warstwa danych
- tabele logów  
- tabele uprawnień  
- tabele ról  
- tabele tokenów  

### Warstwa logiki
- walidacja uprawnień  
- kontrola dostępu  
- audyt działań  
- szyfrowanie  

### Warstwa API
- `/auth/login`  
- `/auth/refresh`  
- `/auth/roles`  
- `/auth/audit`  

---

## ⚠️ 6. Zgodność z RODO

System implementuje:

- prawo do usunięcia danych  
- prawo do eksportu danych  
- anonimizację danych  
- rejestrowanie zgód  
- minimalizację danych  

---

## 📄 7. Dokumentacja powiązana

- **[moduł architektura](modul_architektura.md)**  
- **[moduł API](modul_api.md)**  
- **[moduł automatyzacje]{modul_automatyzacje.md)**  
- **[moduł baza danych](modul_baza_danych.md)**  

---

## 🏁 8. Status modułu

Moduł bezpieczeństwo jest:

- opisany,  
- udokumentowany,  
- zgodny z architekturą,  
- gotowy do implementacji.
