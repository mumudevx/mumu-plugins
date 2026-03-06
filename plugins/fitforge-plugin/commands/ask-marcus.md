---
description: Marcus Reid'e (PT) antrenman, egzersiz ve program hakkinda soru sorun.
allowed-tools:
  - Agent
  - Read
  - WebSearch
argument-hint: "[--lang XX] [antrenman, egzersiz veya programiniz hakkindaki sorunuz]"
---

Kullanici Marcus Reid'e (PT Agent) soru sormak istiyor.

Kullanici girdisi: <user-input>$ARGUMENTS</user-input>

## Talimatlar

1. Kullanicinin girdisinde `--lang XX` parametresini ara. Bulursan `language` olarak ata ve metinden cikar. Bulamazsan `language: tr` varsay.

2. Agent tool'unu kullanarak `marcus-reid` agent'ini Q&A modunda cagir. Asagidaki mesaji ilet:

```
language: [language kodu]

Bu bir Q&A oturumdur — haftalik program olusturma degil. Kullanicinin sorusunu yanitla.

Eger daha once olusturulmus bir program dosyasi varsa, Read tool ile okuyarak baglam sagla.

Soru: [kullanicinin sorusu]
```

3. Marcus Reid'in kapsam alani:
   - Antrenman prensipleri ve program tasarimi
   - Egzersiz formu ve teknigi
   - Progresif asiri yuklenme
   - Yaralanma onleme
   - Program modifikasyonlari

4. Kapsam disindaki sorulari (beslenme, diyet, takviye) Dr. Elena Vasquez'e yonlendir: `/fitforge:ask-elena`
