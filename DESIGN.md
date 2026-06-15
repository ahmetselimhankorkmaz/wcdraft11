---
name: wcDraft11
description: 2026 Dünya Kupası draft + turnuva simülasyonu — maç günü stüdyosu netliğinde tarayıcı oyunu
colors:
  cim-yesili: "#16a34a"
  cim-yesili-koyu: "#15803d"
  cim-yesili-zemin: "#f0fdf4"
  projektor-yesili: "#4ade80"
  kupa-altini: "#fbbf24"
  kupa-altini-koyu: "#92400e"
  hakem-mavisi: "#2563eb"
  hakem-mavisi-acik: "#60a5fa"
  kirmizi-kart: "#ef4444"
  korner-turuncusu: "#f97316"
  konfederasyon-moru: "#a855f7"
  stadyum-gecesi: "#0a1628"
  stadyum-paneli: "#1e3a5f"
  gece-cimi: "#0d4a20"
  antrenman-grisi: "#f4f5f7"
  tribun-beyazi: "#ffffff"
  tebesir-cizgisi: "#e5e7eb"
  skorboard-murekkebi: "#111827"
  spiker-grisi: "#6b7280"
  sessiz-gri: "#9ca3af"
  gece-metni: "#e2e8f0"
typography:
  display:
    fontFamily: "Bebas Neue, sans-serif"
    fontSize: "22px-34px"
    fontWeight: 400
    lineHeight: 1.1
    letterSpacing: "1px-3px"
  headline:
    fontFamily: "Bebas Neue, sans-serif"
    fontSize: "18px-20px"
    fontWeight: 400
    lineHeight: 1.2
    letterSpacing: "1px"
  body:
    fontFamily: "DM Sans, sans-serif"
    fontSize: "13px"
    fontWeight: 600
    lineHeight: 1.35
  label:
    fontFamily: "DM Sans, sans-serif"
    fontSize: "10px"
    fontWeight: 700
    letterSpacing: "1.5px"
rounded:
  sm: "6px"
  md: "8px"
  lg: "10px"
  xl: "14px"
  pill: "999px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "12px"
  lg: "16px"
  xl: "28px"
components:
  button-primary:
    backgroundColor: "{colors.cim-yesili}"
    textColor: "{colors.tribun-beyazi}"
    typography: "{typography.display}"
    rounded: "{rounded.lg}"
    padding: "14px"
  button-primary-hover:
    backgroundColor: "{colors.cim-yesili-koyu}"
  button-danger:
    backgroundColor: "{colors.kirmizi-kart}"
    textColor: "{colors.tribun-beyazi}"
    rounded: "{rounded.md}"
    padding: "10px"
  tab:
    backgroundColor: "{colors.tribun-beyazi}"
    textColor: "{colors.sessiz-gri}"
    typography: "{typography.headline}"
    rounded: "7px"
    padding: "6px 14px"
  tab-active:
    backgroundColor: "{colors.cim-yesili-zemin}"
    textColor: "{colors.cim-yesili}"
  card-player:
    backgroundColor: "{colors.tribun-beyazi}"
    textColor: "{colors.skorboard-murekkebi}"
    rounded: "{rounded.lg}"
  chip-team:
    backgroundColor: "{colors.cim-yesili-zemin}"
    textColor: "{colors.cim-yesili}"
    rounded: "{rounded.pill}"
    padding: "5px 9px"
---

# Design System: wcDraft11

## 1. Overview

**Creative North Star: "Maç Günü Stüdyosu"**

wcDraft11, bir yayın stüdyosunun çalışma disipliniyle kurulmuş bir oyun arayüzüdür: aydınlık, düz ve hızlı bir draft odası; perde açıldığında ise koyu lacivert bir simülasyon sahnesi. Heyecan, görsel gürültüyle değil iki kontrast anla üretilir — gün ışığında kadro kurarsın, projektörler altında turnuvayı izlersin. Veri her zaman skorboard netliğindedir: büyük Bebas Neue rakamlar konuşur, DM Sans anlatır, renk yalnız anlam taşıdığında sahaya girer.

Sistem, PRODUCT.md'nin anti-referanslarını açıkça reddeder: jenerik yapay zekâ sitesi görünümü (aşırı gradient, anlamsız glow, şablon kart grid'leri, dev CTA blokları), bahis sitesi esteti̇ği, ücretsiz mobil oyun kalabalığı ve ruhsuz kurumsal SaaS paneli. Tek dekoratif lüks, sahanın kendisidir: çim şeritleri ve tebeşir çizgileri temsilîdir, süs değildir.

**Key Characteristics:**
- İki sahne: aydınlık draft odası (#f4f5f7 zemin, beyaz paneller) ↔ koyu simülasyon gecesi (#0a1628)
- Düz yüzeyler, kenarlıkla ayrışma; gölge yalnız modal ve tepe anlarında
- Bebas Neue rakam/başlık sesi + DM Sans gövde — başka font yok
- Renk = anlam: yeşil eylem, altın ödül, mavi seçim, kırmızı eleme
- ≤150ms geçişler; tıkladığın an cevap alırsın

## 2. Colors

Tailwind kökenli ama rolleri keskin biçimde atanmış bir palet: her renk sahadaki bir şeyin adıdır ve yalnız o işi yapar.

### Primary
- **Çim Yeşili** (#16a34a): Birincil eylem rengi — çarkı çevir butonu, aktif formasyon sekmesi, logo, takım rozeti. Oyuncuyu ileri taşıyan her şey yeşildir.
- **Çim Yeşili Koyu** (#15803d): Birincil butonların hover durumu.
- **Çim Yeşili Zemin** (#f0fdf4): Aktif sekme ve rozet arka planı; yeşilin fısıltısı.
- **Projektör Yeşili** (#4ade80): Koyu simülasyon ekranında yeşilin parlayan karşılığı (logo, "simüle et" vurgusu). Aydınlık zeminde asla kullanılmaz — kontrast yetmez.

### Secondary
- **Kupa Altını** (#fbbf24): Ödül ve tepe anları — kaptan seçimi, kupa, 2026 rozeti. Koyu metin eşi **Kupa Altını Koyu** (#92400e), açık amber zeminlerde metin için.
- **Hakem Mavisi** (#2563eb): Seçim ve odak durumu — seçili oyuncu banner'ı, focus halkası, logo vurgusu. Açık tonu **#60a5fa** koyu zeminde bilgi vurgusu.

### Tertiary
- **Kırmızı Kart** (#ef4444): Yıkıcı eylem ve eleme — sıfırlama onayı, turnuvadan düşme.
- **Korner Turuncusu** (#f97316): "Ülke" slot kartının kimliği (kenarlık + etiket; zemin #fff7ed, değer metni #c2410c).
- **Konfederasyon Moru** (#a855f7): "Konfederasyon" slot kartının kimliği (zemin #faf5ff, değer metni #7c3aed).
- **Stadyum Gecesi** (#0a1628): Simülasyon ekranının zemini; paneller **Stadyum Paneli** (#1e3a5f) ve #0f2550 ile katmanlanır, metin **Gece Metni** (#e2e8f0).
- **Gece Çimi** (#0d4a20): Saha bileşeninin çim gradyanının merkezi (#0a3d1a → #0f5224 şerit deseni). Yalnız sahada yaşar.

### Neutral
- **Antrenman Grisi** (#f4f5f7): Draft odasının gövde zemini.
- **Tribün Beyazı** (#ffffff): Panel ve kart yüzeyleri.
- **Tebeşir Çizgisi** (#e5e7eb): Tüm kenarlıklar ve ayraçlar.
- **Skorboard Mürekkebi** (#111827): Birincil metin ve isimler.
- **Spiker Grisi** (#6b7280): İkincil metin (tur bilgisi, ipuçları).
- **Sessiz Gri** (#9ca3af): Büyük harfli bölüm etiketleri ve pasif sekmeler. Yalnız ≥3:1 kontrast veren büyük/kalın etiketlerde; gövde metni olarak yasak.

### Named Rules
**Altın Kazanılır Kuralı.** Kupa Altını yalnız kazanılmış anlarda görünür: kaptanlık, kupa, ödül. Dekor olarak altın kullanmak yasaktır — enflasyon değerini öldürür.

**Tek Yeşil Kuralı.** Bir ekranda aynı anda tek birincil (yeşil) eylem bulunur. İki yeşil buton görüyorsan biri yanlıştır.

## 3. Typography

**Display Font:** Bebas Neue (sans-serif fallback)
**Body Font:** DM Sans (sans-serif fallback)

**Character:** Stadyum skorboardu ile spiker sesi: Bebas Neue dar, dik ve yüksek sesli — rakamlar, reytingler, başlıklar, buton etiketleri onun; DM Sans sıcak ve okunaklı — açıklamalar, isimler, ipuçları onun. Kondanse display + geometrik-hümanist gövde kontrastı sistemin tek font ikilisidir.

### Hierarchy
- **Display** (400, 22–34px, lh 1.1, ls 1–3px): Slot kart değerleri, oyuncu reytingleri (30px), büyük buton etiketleri, ekran başlıkları. Daima Bebas Neue.
- **Headline** (400, 18–20px, lh 1.2, ls 1–2px): Logo, modal başlıkları, formasyon sekmeleri.
- **Body** (600–700, 13px, lh 1.35): Oyuncu adları, açıklama metinleri, ipucu kutuları. DM Sans.
- **Label** (700, 10–11px, ls 1.5px, UPPERCASE): Bölüm etiketleri ("ÜLKE SEÇ", "OYUNCULAR"). Sessiz Gri (#9ca3af) yalnız bu boyut-ağırlık kombinasyonunda.

### Named Rules
**İki Ses Kuralı.** Bebas Neue bağırır, DM Sans anlatır. Üçüncü bir font, italik süsleme veya gradient metin sisteme giremez.

**Rakam Sahnesi Kuralı.** Sayısal değer (reyting, skor, istatistik) her zaman Bebas Neue ile ve çevresindeki metinden belirgin büyük yazılır; sayı bu oyunun yıldız oyuncusudur.

## 4. Elevation

Sistem düz-öncelikli çalışır: yüzeyler gölgesizdir, ayrışma Tebeşir Çizgisi (#e5e7eb) kenarlıklar ve zemin ton farkıyla (#f4f5f7 ↔ #fff) sağlanır. Gölge bir durum tepkisidir, varsayılan değil: hover'da kartlara hafif renkli ima (örn. `0 2px 8px rgba(22,163,74,0.13)`), modallarda belirgin kaldırma (`0 24px 80px rgba(0,0,0,0.3)`), koyu simülasyon ekranında ise düşük yoğunluklu renkli ışımalar (`0 0 10px rgba(96,165,250,0.10)` + ince iç beyaz çizgi) katman hissi verir. Saha bileşeni tek istisnadır: `inset 0 0 60px rgba(0,0,0,0.3)` ile stadyum derinliği taşır.

### Shadow Vocabulary
- **Hover iması** (`0 2px 8px rgba(22,163,74,0.13)`): Oyuncu kartı hover'ı; renk, eylemin rengini izler.
- **Odak halkası** (`0 0 0 3px rgba(37,99,235,0.15)` + `outline: 3px solid rgba(37,99,235,0.35)`): Seçim ve klavye odağı, daima Hakem Mavisi.
- **Modal kaldırma** (`0 24px 80px rgba(0,0,0,0.3)`): Yalnız diyalog ve tepe-an ekranları.
- **Gece ışıması** (`0 0 10px rgba(<renk>,0.10-0.15), inset 0 1px 0 rgba(255,255,255,0.06)`): Koyu sim panellerinde durum rengiyle hafif parlama.

### Named Rules
**Düz Saha Kuralı.** Yüzeyler dinlenirken düzdür. Gölge yalnız duruma (hover, odak, modal) cevap olarak belirir; kalıcı gölgeli kart yasaktır.

## 5. Components

Bileşen karakteri: **hızlı ve net** — geçişler ≤150ms, tıkladığın an cevap alırsın. Süslü easing, bounce, bekleme yok.

### Buttons
- **Shape:** Yumuşak köşe (10px); küçük yardımcı butonlar 6–8px.
- **Primary (spin-btn):** Çim Yeşili zemin, beyaz Bebas Neue etiket (22px, ls 3px), 14px dikey dolgu, tam genişlik. Hover'da koyulaşır (#15803d), aktif baskıda `scale(0.985)`.
- **Hover / Focus:** `background 0.15s, transform 0.1s`; klavye odağı Hakem Mavisi halka.
- **Disabled:** Yeşilin soluk tonları (#bbf7d0 zemin, #86efac metin) — gri değil, "henüz değil" diyen yeşil.
- **Danger:** Kırmızı Kart (#ef4444) zemin, yalnız yıkıcı onaylarda ("SIFIRLA →").

### Chips
- **Style:** Takım rozeti — Çim Yeşili Zemin (#f0fdf4), #bbf7d0 kenarlık, pill (999px), 11px/800 yeşil metin.
- **State:** Tek durumlu kimlik göstergesi; tıklanabilir değil.

### Cards / Containers
- **Corner Style:** Oyuncu kartları 10px; slot kartları 14px; saha 16px.
- **Background:** Tribün Beyazı; kimlikli slot kartları kendi tint'ini taşır (#fff7ed turuncu, #faf5ff mor).
- **Shadow Strategy:** Düz Saha Kuralı — dinlenirken gölgesiz, hover'da renkli ima.
- **Border:** 1.5–2px Tebeşir Çizgisi; durum rengi kenarlığın tamamını değiştirir (seçimde mavi, hover'da yeşil). Asla tek kenarlı renk şeridi değil.
- **Internal Padding:** 8–18px; yoğun veri kartlarında sıkı (8px), kimlik kartlarında geniş (16–18px).
- **Signature detay:** Oyuncu kartı altında 6 sütunlu mikro istatistik ızgarası — 7px etiket, 13px Bebas değer, 3px renkli dolum çubuğu.

### Inputs / Fields
- **Style:** Beyaz zemin, Tebeşir Çizgisi kenarlık, 10px köşe, 14px DM Sans.
- **Focus:** Hakem Mavisi halka (`outline: 3px solid rgba(37,99,235,0.35), offset 2px`).

### Navigation
- **Style:** 48px sabit üst bar — beyaz zemin, alt kenarlık; solda Bebas logo (yeşil + mavi vurgu), ortada tur bilgisi (Spiker Grisi), sağda takım rozeti. Mobilde tek satırda sıkışır, rozet `calc(100vw - 32px)` ile taşmaz.
- **Formasyon sekmeleri (f-tab):** Beyaz zemin, 2px kenarlık, Bebas 15px; aktifte yeşil kenarlık + tint zemin.

### Saha (Signature Component)
Dikey futbol sahası: yatay şeritli çim gradyanı (#0a3d1a → #0f5224), %8–13 opaklıkta beyaz tebeşir çizgileri (orta yuvarlak, ceza sahaları, orta nokta), 16px köşe, içe gölge ile stadyum derinliği. Oyuncu slotları bu sahnenin üzerine dizilir. Bu, sistemdeki tek temsilî gradient iznidir.

## 6. Do's and Don'ts

### Do:
- **Do** yeşili yalnız birincil eyleme ver; ekran başına tek yeşil buton (Tek Yeşil Kuralı).
- **Do** sayıları Bebas Neue ile büyük yaz (reyting 30px, slot değeri 34px); rakam yıldız oyuncudur.
- **Do** durumu kenarlık rengiyle anlat: seçim = Hakem Mavisi tam kenarlık + hafif halka, hover = Çim Yeşili.
- **Do** geçişleri 100–150ms tut; `transform: scale(0.985)` baskı hissi yeterli abartıdır.
- **Do** koyu sim ekranında açık-zemin renklerinin gece karşılıklarını kullan (#4ade80, #60a5fa, #e2e8f0) — aydınlık tonlar gece kontrast veremez.
- **Do** WCAG AA'yı koru: gövde metni ≥4.5:1; Sessiz Gri (#9ca3af) yalnız ≥3:1 veren büyük/kalın etiketlerde.

### Don't:
- **Don't** "jenerik yapay zekâ sitesi" görünümü: aşırı gradient, anlamsız glow efektleri, şablon kart grid'leri, birbirinin aynısı büyük CTA blokları (PRODUCT.md anti-referansı, kelimesi kelimesine).
- **Don't** bahis sitesi estetiği: yeşil-altın neon, agresif yanıp sönen butonlar. Altın yalnız kazanılır (Altın Kazanılır Kuralı).
- **Don't** ücretsiz mobil oyun kalabalığı: sahte para, parlayan rozetler, pop-up yağmuru.
- **Don't** kurumsal SaaS paneli sterilliği: ruhsuz gri dashboard; gri gövde metni (#9ca3af) yasak.
- **Don't** dekoratif gradient — gradient yalnız temsilîdir (çim). Butonda, metinde, kart zemininde gradient yasak; `background-clip: text` kesinlikle yasak.
- **Don't** tek kenarlı renk şeridi (border-left aksan); durum daima tam kenarlıkla anlatılır.
- **Don't** kalıcı kart gölgesi; gölge durum tepkisidir (Düz Saha Kuralı).
- **Don't** üçüncü font, bounce/elastic easing, 150ms üstü arayüz geçişi.
