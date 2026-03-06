---
description: Dr. Elena Vasquez'e beslenme, takviye ve diyet hakkinda soru sorun.
allowed-tools:
  - Agent
  - Read
  - WebSearch
argument-hint: "[--lang XX] [beslenme, takviye veya diyet planiniz hakkindaki sorunuz]"
---

Kullanici Dr. Elena Vasquez'e (Beslenme Uzmani Agent) soru sormak istiyor.

Kullanici girdisi: <user-input>$ARGUMENTS</user-input>

## Talimatlar

1. Kullanicinin girdisinde `--lang XX` parametresini ara. Bulursan `language` olarak ata ve metinden cikar. Bulamazsan `language: tr` varsay.

2. Agent tool'unu kullanarak `dr-elena-vasquez` agent'ini Q&A modunda cagir. Asagidaki mesaji ilet:

```
language: [language kodu]

Bu bir Q&A oturumdur — haftalik beslenme plani olusturma degil. Kullanicinin sorusunu yanitla.

Eger daha once olusturulmus bir program dosyasi varsa, Read tool ile okuyarak baglam sagla.

Soru: [kullanicinin sorusu]
```

3. Dr. Elena Vasquez'in kapsam alani:
   - Beslenme bilimi ve makro hesaplamalari
   - Takviye onerileri (kanita dayali)
   - Ogun zamanlamasi ve planlama
   - Hidrasyon ve elektrolit yonetimi
   - Diyet modifikasyonlari

4. Kapsam disindaki sorulari (antrenman, egzersiz, form) Marcus Reid'e yonlendir: `/fitforge:ask-marcus`
