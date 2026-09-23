# ⚡ Hydrogen Client — by AESIR

**Minecraft 1.21.11 (Fabric)** için Türkçe, yuvarlak arayüzlü özel istemci modu.
Sağ Shift ile açılan menü, yuvarlak ESC ekranı, RPG temalı can barları, skin/pelerin
kozmetikleri ve tonlarca HUD modülü.

![sürüm](https://img.shields.io/badge/MC-1.21.11-gold) ![yarn](https://img.shields.io/badge/yarn-1.21.11%2Bbuild.6-blue)

---

## 🚀 Kurulum (oyuncu için)

1. **Fabric Loader 0.19.5+** kur (1.21.11 profili için).
2. **Fabric API** (`0.141.6+1.21.11`) jar'ını indir → `.minecraft/mods` klasörüne at.
3. **Hydrogen jar'ını** (`build/libs/hydrogen-1.0.0.jar`) da `mods` klasörüne at.
4. Oyuna gir → **Sağ Shift** 🎉

## 🛠 Derleme (geliştirici için)

```bash
cd hydrogen
./gradlew build          # Java 21+ gerekir
# çıktı: build/libs/hydrogen-1.0.0.jar
```

Sürümler `gradle.properties` içinde:

| Bileşen       | Sürüm              |
|---------------|--------------------|
| Minecraft     | 1.21.11            |
| Yarn mappings | 1.21.11+build.6    |
| Fabric Loader | 0.19.5             |
| Fabric API    | 0.141.6+1.21.11    |
| Loom          | 1.18.2             |

## ✨ Özellikler

### 🎨 Yuvarlak UI API
- GPU'da üretilen **antialiasing'li rounded-rect** dokuları (kendi UI motoru)
- Tüm ekranlarda açılış animasyonu + arka plan blur'u + AESIR altın teması
- **Yuvarlak ESC menüsü** (vanilla ESC yerine geçer — modülden kapatılabilir)

### 🖥 Sağ Shift Menüsü
- Modül kartları + **arama** + kategori sekmeleri (Tümü / HUD / Efektler / Arayüz)
- Hızlı bağlantılar: HUD Düzeni, Tuş Atamaları, **Kozmetikler (YENİ!)**
- "X/23 Etkin" sayacı

### ❤️ RPG HUD (sol üst)
- **AESIR filigranı** (logo + HYDROGEN yazısı)
- **Özel Can Çubukları**: altın çerçeveli panel, RPG kalp ikonları, yarı kalp,
  absorption gösterimi, can sayısı
- FPS, Koordinatlar, Yön, Ping, Saat, Boyut, Sunucu, Zırh, XP, İtem Bilgisi,
  Blok Bilgisi, Hedef Canı modülleri
- **HUD Düzeni** ekranı: her modülü sürükle-bırak ile istediğin yere koy

### 🎭 Kozmetikler
- **Skin Değiştir**: kullanıcı adından (mineskin.eu) veya URL'den skin yükle,
  Klasik/İnce model seçimi, 64x32 → 64x64 eski skin dönüşümü, anında uygulanır
  *(istemci tarafında görünür)*
- **Sunucu komutları**: SkinRestorer kurulu sunucularda `/skin url {url} {model}`
  komutu otomatik gönderilir → **herkes görsün** (komut şablonu config'te)
- **Pelerinler**: minecraftcapes.co.uk API entegrasyonu + özel URL
- **Efektler**: Alev, Buz, Yıldız Tozu, Altın Tozu, Elektrik parçacık efektleri

### ⚙️ Diğer modüller
Tam Parlaklık (gamma 16), Menü Animasyonları, Yuvarlak ESC Menüsü

## 📄 Config

`config/hydrogen-client.json` — modül açık/kapalı durumları, HUD offset'leri,
skin/pelerin ayarları ve sunucu komut şablonu burada saklanır.

## 📁 Yapı

```
src/main/java/...     → ana giriş noktası
src/client/java/...   → tüm client kodu (UI, HUD, ekranlar, mixin'ler)
src/client/resources/ → logo/kalp dokuları, dil dosyaları, mod ikonu
```

MIT License — `LICENSE` dosyasına bak.
