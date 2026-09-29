# Dart Vader

Eski, sıcak bir barın köşesinde her akşam aynı sandalyede oturan bir müdavim var. Adını kimse tam bilmez; herkes ona "abi" der. Klasik dart artık ona yetmiyor. Bir gece barmen bir teklifle gelir: tahtaya yeni eklentiler, darta özel güçler. Hedef basit: o geceye kadar kimsenin kıramadığı skoru kırmak.

**Dart Vader**, klasik dartın üstüne dart özellikleri ve tahtada vurulabilen eklentiler ekleyen, dikey ekran için tasarlanmış bir tarayıcı oyunudur. Tek bir HTML dosyasıdır; kurulum gerektirmez.

## Oynamak

`index.html` dosyasını herhangi bir tarayıcıda açman yeterli. Telefonda dikey tutarak oynanır; masaüstünde ortada dikey bir oyun alanı olarak açılır.

## Nasıl oynanır?

1. **Yön (X ekseni):** Tahtanın altındaki kaydırıcı sağa sola gider. İstediğin sütuna geldiğinde tıkla ya da ekrana dokun.
2. **Güç (Y ekseni):** Sağdaki güç kaydırıcısı iner çıkar. Güç arttıkça dart tahtada daha yukarıya saplanır. Doğru yükseklikte dokun, el dartı fırlatır.

### Puanlama

- Vurduğun dilimin puanı; dış ince halka ×2, iç ince halka ×3, merkezin dış halkası 25, en içteki nokta Bull 50.
- **Mesafe çarpanı:** 10 m'de ×1, her 2 metrede +1 (28 m'de ×10).

### Dart özellikleri (sağ alt köşe)

| Özellik | Etki | Hak |
|---|---|---|
| Dev | Dart büyür; vurduğun dilim ve iki komşusundan en yükseği sayılır | 2 |
| Buz | Kaydırıcılar yarı hızda hareket eder | 2 |
| Ateş | İki komşu dilimin puanı da eklenir | 2 |
| Altın | Atışın puanı ikiye katlanır | 1 |

Her atışta bir özellik seçilebilir.

### Tahtadaki eklentiler

- **×2 / ×3 halkaları:** Puanı katlar.
- **+50 bira kapağı:** Bonus puan verir.
- **+1 halkası:** Fazladan bir dart kazandırır.

## Modlar

### Standart

10 dart, 10 metreden başlarsın. Puan eşiklerini geçtikçe tahta 2 metre uzaklaşır ve mesafe çarpanı büyür. Toplam puanın rekor olarak saklanır.

### Challenge (10 level)

| Level | Mesafe | Dart | Hedef Puan | Yeni numara |
|---|---|---|---|---|
| 1 | 10 m | 10 | 100 | Klasik dart |
| 2 | 12 m | 9 | 200 | Dev dart |
| 3 | 14 m | 9 | 350 | Buz dartı |
| 4 | 16 m | 8 | 500 | Ateş dartı |
| 5 | 18 m | 8 | 700 | Altın dart |
| 6 | 20 m | 8 | 900 | |
| 7 | 22 m | 7 | 1150 | |
| 8 | 24 m | 7 | 1400 | |
| 9 | 26 m | 7 | 1700 | |
| 10 | 28 m | 6 | 2100 | |

- Hedefe ulaşırsan **SUCCESS**, ulaşamazsan **FAIL**.
- Her level 0–3 yıldızla puanlanır: hedef = 1 yıldız, hedefin 1,25 katı = 2 yıldız, 1,5 katı = 3 yıldız.
- Sonraki level, öncekinden en az 1 yıldız kazanarak açılır.

## Klavye

| Tuş | İşlev |
|---|---|
| Boşluk / Enter | Kaydırıcıyı durdur / fırlat |
| 1–4 | Dev, Buz, Ateş, Altın özelliğini seç |
| Esc / P | Mola |

## Özellikler

- Nostaljik ahşap bar: sallanan ampul, hafif duman, neon tabela, kareli gömlekli el
- Oyundan oyuna değişen tahta renkleri: siyah-beyaz-kırmızı, yeşil-kahverengi-kırmızı, lacivert-bordo-gri
- Atışlarına yorum yapan barmen
- Tarayıcıda anlık üretilen bar blues'u ve ses efektleri (Ayarlar'dan kapatılabilir)
- Rekor, yıldızlar ve ayarlar tarayıcıda saklanır

## Dosya yapısı

```
dart-vader/
├── index.html    ← Tek dosyada eksiksiz oyun
└── README.md
```

## Emeği geçenler

- **Oyun fikri ve tasarım:** Numan Mak
- **İlham:** Klasik dart · Kedi Köpek Kavgası

## Yol haritası

- [ ] Gerçek ses kayıtları (dart çarpma, alkış)
- [ ] Liderlik tablosu
- [ ] Animasyonlu abi karakteri
- [ ] Günlük challenge modu
- [ ] PWA / çevrimdışı destek
