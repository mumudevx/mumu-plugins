<p align="center">
  <strong>FitForge</strong> — Claude Code Plugin
</p>

<p align="center">
  <img src="https://img.shields.io/badge/versiyon-1.0.0-blue" alt="versiyon" />
  <img src="https://img.shields.io/badge/lisans-MIT-green" alt="lisans" />
  <img src="https://img.shields.io/badge/claude--code-plugin-purple" alt="claude code plugin" />
</p>

<p align="center">
  <a href="README.md">🇬🇧 English</a> | 🇹🇷 Türkçe
</p>

---

Iki uzman yapay zeka agent ile kisisellestirilmis fitness ve beslenme programi olusturucu. Vucut olculerinize ve hedeflerinize gore haftalik antrenman + beslenme plani uretir.

## Nasil Calisir

1. Vucut olculerinizi, ekipmaninizi ve hedeflerinizi serbest metin olarak yazarsiniz
2. **Marcus Reid** (PT Agent) — bilimsel temelli haftalik antrenman programi olusturur
3. **Dr. Elena Vasquez** (Beslenme Agent) — antrenman yukune gore beslenme plani olusturur
4. Orkestrator iki plani birlestirip size sunar

Her iki agent de WebSearch ile hakemli arastirmalara referans verebilir (PubMed, JISSN, JSCR, Sports Medicine).

## Kurulum

mumu-plugins marketplace uzerinden:

```bash
claude plugin install https://github.com/mumudevx/mumu-plugins.git
```

## Kullanim

### Tam Program Olusturma

```
/fitforge:start 28 yasinda, erkek, 180cm, 85kg, orta aktif, gym erisimim var, kas kazanimi istiyorum
```

`--lang` parametresi cikti dilini belirler (ISO 639-1 kodu). Varsayilan `tr` (Turkce). Ornekler: `en`, `de`, `fr`, `es`, `ar`, `ja`.

```
/fitforge:start --lang en I'm 28, male, 180cm, 85kg, moderately active, gym access, goal is muscle gain
```

### Hazir Prompt Dosyasi ile Kullanim

Vucut verilerinizi bir markdown dosyasinda hazirlayip dogrudan referans verebilirsiniz:

```
/fitforge:start --lang en @starter-prompt-example.md
```

Beklenen format icin `starter-prompt-example.md` dosyasina bakin.

### PT'ye Soru Sorma

```
/fitforge:ask-marcus Hipertrofi icin en iyi tekrar araligi nedir?
```

Marcus Reid antrenman prensipleri, egzersiz formu, progresif asiri yuklenme, yaralanma onleme ve program modifikasyonlari hakkinda sorulari yanitlar.

### Beslenme Uzmanina Soru Sorma

```
/fitforge:ask-elena Antrenman sonrasi ne kadar protein tuketmeliyim?
```

Dr. Elena Vasquez beslenme bilimi, makro hesaplamalari, takviyeler, ogun zamanlamasi, hidrasyon ve diyet modifikasyonlari hakkinda sorulari yanitlar.

## Bilesenler

| Bilesen | Tur | Aciklama |
|---------|-----|----------|
| `fitforge` | Skill | Ana orkestrator workflow |
| `marcus-reid` | Agent | PT — antrenman programi olusturma |
| `dr-elena-vasquez` | Agent | Beslenme uzmani — diyet plani olusturma |
| `/fitforge:start` | Komut | Tam haftalik program olusturma |
| `/fitforge:ask-marcus` | Komut | PT agent ile soru-cevap |
| `/fitforge:ask-elena` | Komut | Beslenme agent ile soru-cevap |

## Lisans

MIT
