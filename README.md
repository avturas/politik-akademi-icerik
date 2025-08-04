# 🏛️ Politika Akademi İçerik Deposu

Bu repository, **Politika Akademi** platformunun eğitim içeriklerini barındırır. İçerikler `.md` (Markdown) formatında olup, `index.json` dosyasında kategorilere ve modüllere ayrılmış şekilde listelenir. Bu yapı, frontend uygulaması tarafından içerikleri dinamik olarak sunmak amacıyla kullanılır.

---

## 📂 İçerik Yapısı

Her içerik şu alanlarla tanımlanır:

| Alan       | Açıklama                                                                |
| ---------- | ----------------------------------------------------------------------- |
| `title`    | İçerik başlığı                                                          |
| `slug`     | URL dostu kısa ad (benzersiz tanımlayıcı)                               |
| `category` | Genel konu başlığı (örn. _Tarihi ve Kuramsal Temeller_)                 |
| `module`   | Alt modül başlığı (örn. _Siyasetin Tarihsel Temelleri ve Gücün Evrimi_) |
| `path`     | Markdown dosyasının depodaki tam yolu                                   |

---

## 🧭 Örnek `index.json` Girdisi

```json
{
  "title": "Roma Cumhuriyeti ve İmparatorlukta Yönetişim",
  "slug": "07-roma-cumhuriyeti-ve-imparatorlukta-yonetisim",
  "category": "Tarihi ve Kuramsal Temeller",
  "module": "Siyasetin Tarihsel Temelleri ve Gucun Evrimi",
  "path": "tarihi-ve-kuramsal-temeller/siyasetin-tarihsel-temelleri-ve-gucun-evrimi/07-roma-cumhuriyeti-ve-imparatorlukta-yonetisim.md"
}
```

---

## 📁 Dosya Hiyerarşisi

```
tarihi-ve-kuramsal-temeller/
└── siyasetin-tarihsel-temelleri-ve-gucun-evrimi/
    ├── 01-siyaset-nedir-kavramsal-giris-ve-tarihsel-arka-plan.md
    ├── 02-iktidar-mesrutiyet-ve-otorite-uzerine-temel-kavramlar.md
    ├── 03-ilkel-toplumlarda-guc-otorite-ve-liderlik-yapilari.md
    ├── ...
```

---

## ⚙️ Nasıl Kullanılır?

Bu repository doğrudan frontend uygulama tarafından okunur:

- `index.json` dosyası tüm içeriklerin listesini, sıralamasını ve başlıklarını barındırır.
- Her içerik `path` değeriyle belirtilen bir `.md` dosyasına karşılık gelir.
- İçerik bileşenleri bu dosyaları GitHub üzerinden `raw` olarak çeker ve Markdown renderer ile kullanıcıya sunar.

---

## 🧾 Yeni İçerik Eklemek

1. Uygun kategori ve modül klasörü altına yeni bir `.md` dosyası ekleyin.
2. `index.json` dosyasına aşağıdaki formatta yeni bir nesne ekleyin:

```json
{
  "title": "Yeni İçerik Başlığı",
  "slug": "slug-uyumlu-baslik",
  "category": "Kategori Adı",
  "module": "Modül Adı",
  "path": "kategori/modul/slug-uyumlu-baslik.md"
}
```

3. Pull request oluşturun.

---

## ⚠️ Uyarı

Bu içeriklerin tamamı **ChatGPT tarafından otomatik olarak oluşturulmuştur**.  
Kaynak kontrolü yapılmamıştır ve çeşitli **bilimsel, tarihsel veya teorik hatalar içerebilir**.  
Lütfen akademik veya resmi bir amaçla kullanmadan önce doğruluğunu mutlaka kontrol ediniz.

---

## 🔍 Notlar

- Tüm dosya adları `kebab-case` biçiminde yazılmalıdır.
- Markdown dosyaları UTF-8 formatında ve `#` ile başlayan başlık yapısında olmalıdır.
- Frontend sistem, `index.json` sırasını koruyarak içerikleri gösterir.

---

## 🔓 Lisans

Bu içerikler **kamusal alan (public domain)** olarak sunulmuştur.

**Tüm kullanıcılar içerikleri özgürce kullanabilir, kopyalayabilir, değiştirebilir ve dağıtabilir.**  
Herhangi bir izin, atıf veya ücret gerekmemektedir.
