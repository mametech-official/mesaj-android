# 📱 Mesaj — Android (Google Play Store) Resmi Deposu

Bu depo, **Mesaj — Yeni Nesil Anlık İletişim** uygulamasının **Google Play Store (Android)** için hazırlanmış yerel **Capacitor + Android Studio (Gradle)** projesidir.

- **Paket Kimliği (Application ID):** `com.mametech.mesaj`
- **Uygulama Adı:** `Mesaj`
- **Hazır İzinler (`AndroidManifest.xml`):**
  - 📷 Kamera (`CAMERA` — Görüntülü görüşme ve fotoğraf çekimi)
  - 🎙️ Mikrofon (`RECORD_AUDIO`, `MODIFY_AUDIO_SETTINGS` — Sesli/görüntülü arama ve sesli mesaj)
  - 📍 Yüksek Doğruluklu GPS Konumu (`ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION` — Canlı harita ve konum paylaşımı)
  - 🔔 Bildirim ve Titreşim (`POST_NOTIFICATIONS`, `VIBRATE`)

---

## 🚀 1. Otomatik `.AAB` (Google Play) ve `.APK` İndirme (GitHub Actions)

Bilgisayarınıza Android Studio kurmanıza gerek kalmadan, bu depoya yapılan her güncellemede **GitHub Actions** otomatik olarak hem telefonunuza kurabileceğiniz **`.apk`** dosyasını hem de **Google Play Console**'a yükleyebileceğiniz imzalı **`.aab` (Android App Bundle)** dosyasını üretir:

1. Bu deponun üst menüsünden **[Actions](../../actions)** sekmesine tıklayın.
2. En üstteki yeşil onaylı **Android APK & Google Play AAB Build** çalışmasına tıklayın.
3. Sayfanın altındaki **Artifacts** bölümünden **`Mesaj-Android-GooglePlay-Paketleri`** dosyasını indirin:
   - `app-release.aab` → **Google Play Console**'a doğrudan yüklenen mağaza paketi.
   - `app-release.apk` → Android telefonlara doğrudan kurulabilen imzalı sürüm.
   - `mesaj-release.keystore` → Uygulama imzalama anahtarı (güncellemeler için saklayın).

---

## 🛠️ 2. Android Studio ile Açma ve Geliştirme

Projeyi kendi bilgisayarınızda Android Studio ile açmak isterseniz:

```bash
git clone https://github.com/mametech-official/mesaj-android.git
cd mesaj-android
npm install
npx cap sync android
npx cap open android
```

Ardından Android Studio içinde **Build > Generate Signed Bundle / APK** menüsünden Google Play `.aab` çıktısı alabilirsiniz.

---

## 🔗 Diğer Platform Depoları
- 🌐 **Web (PWA) Deposu:** [mametech-official/mesaj](https://github.com/mametech-official/mesaj)
- 🍎 **Apple (iOS / App Store) Deposu:** [mametech-official/mesaj-apple](https://github.com/mametech-official/mesaj-apple)
