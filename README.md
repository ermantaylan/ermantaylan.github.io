# Erman Taylan — Link Sayfası

Mobil uyumlu, tek sayfalık link sitesi + etkinliğe özel URL/QR üretici.
Tamamen statik — sunucu, veritabanı, bakım gerektirmez.

## Dosyalar

| Dosya | Ne işe yarar |
|---|---|
| `index.html` | Ana sayfa (profil, 4 link, sosyal medya) |
| `generator.html` | Etkinlik linki + QR kod üretici (gizli sayfa, sadece sen kullanırsın) |
| `profile.jpg` | Profil fotoğrafı (yoksa otomatik "ET" avatarı gösterilir) |
| `.nojekyll` | GitHub Pages teknik dosyası (dokunma) |

## GitHub Pages'e kurulum (≈5 dakika)

1. [github.com/new](https://github.com/new) → Repository name: `link` (Public) → **Create repository**
2. Açılan sayfada **"uploading an existing file"** bağlantısına tıkla → bu klasördeki **tüm dosyaları** sürükle-bırak → **Commit changes**
3. Repo'da **Settings → Pages** → Source: *Deploy from a branch* → Branch: `main`, klasör: `/ (root)` → **Save**
4. 1–2 dakika sonra siten yayında:

```
https://ermantaylan.github.io/link/
```

> 💡 Repo adını `ermantaylan.github.io` koyarsan site kök adreste yayınlanır:
> `https://ermantaylan.github.io/` (daha kısa URL, QR'ı da küçültür).

## Kullanım

- **Normal sayfa:** `https://ermantaylan.github.io/link/`
- **Etkinliğe özel:** `https://ermantaylan.github.io/link/?e=Tofaş AI Day`
  → sayfanın üstünde "**Tofaş AI Day** — katılımcıları, hoş geldiniz 👋" rozeti çıkar.
- **Üretici:** `https://ermantaylan.github.io/link/generator.html`
  → etkinlik adını yaz; URL'i kopyala veya QR'ı PNG olarak indir.
  Kutuyu boş bırakırsan genel (etkinliksiz) link/QR üretir.
  Bu sayfaya hiçbir yerden link verilmiyor; adresi yer imlerine ekle.

## Düzenleme

- **Linkler:** `index.html` içinde `<!-- LİNKLER: burayı düzenle -->` bloğu.
  Her link bir `<a class="link">` kartı: `href`, başlık (`<b>`) ve alt yazı (`<span>`).
- **Bio metni:** `<p class="bio">` satırı.
- **Fotoğraf:** `profile.jpg` dosyasını aynı isimle değiştir (kare, en az 400×400 önerilir).
- **Renkler:** her iki dosyanın başındaki `:root` bloğu (`--accent`, `--accent2`).

## Kendi domainin (opsiyonel)

Settings → Pages → **Custom domain** alanına domainini yaz, DNS'te `CNAME` kaydını
`ermantaylan.github.io` adresine yönlendir. HTTPS otomatik gelir.
