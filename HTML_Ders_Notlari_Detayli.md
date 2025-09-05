# C# Yazılım Uzmanlığı - HTML Dersi İçeriği (Açıklamalı ve Örnekli)

---

## Temel HTML Giriş ve Yapısı

**Açıklama:**  
HTML (HyperText Markup Language), web sayfalarının temel yapı taşıdır. Her web uygulamasının ilk adımı HTML ile başlar. Bu bölümde, bir web sayfası dosyasının nasıl oluşturulacağı, temel etiketlerin ne işe yaradığı ve sayfa iskeletinin nasıl kurulduğu gösterilir.

**Konu Başlıkları ve Açıklamaları:**
- **HTML nedir?**  
  Web tarayıcılarının okuyup görüntülediği metin tabanlı bir işaretleme dilidir.
- **HTML dosyası nasıl oluşturulur?**  
  Basit bir metin editörüyle `.html` uzantılı dosya oluşturulur.
- **Temel etiketler:**  
  - `<html>`: Sayfanın tamamını kapsar.
  - `<head>`: Sayfa başlığı, meta bilgiler ve dış dosya bağlantıları burada yer alır.
  - `<body>`: Kullanıcıya görünen içerikler burada bulunur.
- **Başlık ve paragraf etiketleri:**  
  - `<h1> - <h6>`: Farklı seviyelerde başlıklar (büyükten küçüğe).
  - `<p>`: Paragraf oluşturur.

**Örnekler:**
```html
<!DOCTYPE html>
<html>
  <head>
    <title>İlk HTML Sayfam</title>
  </head>
  <body>
    <h1>Merhaba Dünya!</h1>
    <h2>Bu ikinci başlık</h2>
    <p>Web programlamaya hoş geldiniz.</p>
    <p>HTML öğrenmek çok kolay!</p>
  </body>
</html>
```

**Ödev:**  
Kendi adınızı, mesleğinizi ve kısa bir tanıtım metniyle basit bir HTML sayfası oluşturun.

---

## Metin Biçimlendirme ve Linkler

**Açıklama:**  
HTML ile metin üzerinde çeşitli biçimlendirmeler yapılabilir. Ayrıca web sayfaları arasında veya dış sitelere köprüler (linkler) eklenebilir.

**Konu Başlıkları ve Açıklamaları:**
- **Metin biçimlendirme etiketleri:**  
  - `<b>`: Kalın (bold) metin.
  - `<i>`: İtalik metin.
  - `<u>`: Altı çizili metin.
  - `<strong>`: Vurgulu kalın metin (erişilebilirlik için önerilir).
  - `<em>`: Vurgulu italik metin.
  - `<mark>`: Fosforlu işaretleme.
- **Satır ve yatay çizgi:**  
  - `<br>`: Satır sonu ekler.
  - `<hr>`: Yatay çizgi ekler.
- **Liste Türleri:**  
  - `<ul>`: Sırasız liste (madde işaretli).
  - `<ol>`: Sıralı liste (numaralı).
  - `<dl>`, `<dt>`, `<dd>`: Tanımlı liste.
- **Bağlantı (Link) oluşturma:**  
  - `<a href="URL">`: Köprü oluşturur, `target="_blank"` ile yeni sekmede açılır.

**Örnekler:**
```html
<p><strong>Önemli:</strong> HTML öğrenmek için pratik yapmak şarttır.</p>
<p>Hobilerim: <mark>Yazılım</mark>, <i>Fotoğrafçılık</i>, <u>Kitap Okumak</u></p>
<hr>
<ul>
  <li>C#</li>
  <li>HTML</li>
  <li>CSS</li>
</ul>
<ol>
  <li>Başlangıç</li>
  <li>Orta Seviye</li>
  <li>İleri Seviye</li>
</ol>
<dl>
  <dt>HTML</dt>
  <dd>Web sayfası oluşturma dili</dd>
  <dt>CSS</dt>
  <dd>Sayfa tasarım dili</dd>
</dl>
<a href="https://developer.mozilla.org/" target="_blank" title="MDN Web Docs">MDN Web Docs</a>
```

**Ödev:**  
Kendi hobilerinizi sırasız ve sıralı listeyle yazın. Tanımlı bir liste ekleyin ve favori sitenize bir link verin.

---

## Görseller, Tablolar ve Formlar

**Açıklama:**  
Web sayfalarını görsel olarak zenginleştirmek için resim eklemek, verileri düzenli sunmak için tablolar kullanmak ve kullanıcıdan bilgi almak için formlar oluşturmak önemlidir.

**Konu Başlıkları ve Açıklamaları:**
- **Görsel eklemek:**  
  - `<img src="..." alt="...">`: Resim ekler, "alt" açıklama.
  - Genişlik, yükseklik ayarı: `width`, `height` öznitelikleri.
- **Tablo oluşturma:**  
  - `<table>`: Tablo başlatır.
  - `<tr>`: Satır.
  - `<th>`: Başlık hücresi.
  - `<td>`: Veri hücresi.
- **Formlar:**  
  - `<form>`: Form başlatır.
  - `<input>`: Tek satırlık giriş.
  - `<label>`: Alan adı.
  - `<textarea>`: Çok satırlı metin.
  - `<button>`, `<select>`: Buton ve seçenekler.

**Örnekler:**
```html
<img src="https://via.placeholder.com/100" alt="Örnek Resim" width="100">
<table border="1">
  <tr>
    <th>Ad</th>
    <th>Soyad</th>
  </tr>
  <tr>
    <td>Ali</td>
    <td>Yılmaz</td>
  </tr>
</table>
<form>
  <label for="isim">İsminiz:</label>
  <input type="text" id="isim" name="isim"><br>
  <label for="mesaj">Mesajınız:</label>
  <textarea id="mesaj" name="mesaj"></textarea><br>
  <button type="submit">Gönder</button>
</form>
```
**Ek Örnek:**  
```html
<select name="sehir">
  <option value="istanbul">İstanbul</option>
  <option value="ankara">Ankara</option>
  <option value="izmir">İzmir</option>
</select>
```

**Ödev:**  
Aile üyelerinizin bilgilerini tabloya ekleyin, kendinizle ilgili bir form oluşturun ve bir görsel ekleyin.

---

## HTML5 Yenilikleri ve Semantik Etiketler

**Açıklama:**  
HTML5 ile gelen semantik etiketler, kodun anlamlı ve erişilebilir olmasını sağlar. Video ve ses ekleme ile multimedya deneyimi de artar.

**Konu Başlıkları ve Açıklamaları:**
- **Semantik Etiketler:**  
  - `<header>`: Üst bilgi/bölüm başlığı.
  - `<nav>`: Navigasyon menüsü.
  - `<section>`: Bölüm.
  - `<article>`: Makale/yazı.
  - `<aside>`: Yan bilgi.
  - `<footer>`: Alt bilgi.
  - Kodun anlaşılır ve SEO dostu olmasını sağlar.
- **Video ve ses eklemek:**  
  - `<video>`, `<audio>`: Multimedya oynatıcı ekler.
- **Erişilebilirlik:**  
  - Anlamlı etiketlerle engelli kullanıcılar için kolaylık.

**Örnekler:**
```html
<header>
  <h1>Benim Blogum</h1>
  <nav>
    <a href="index.html">Ana Sayfa</a> |
    <a href="hakkimda.html">Hakkımda</a>
  </nav>
</header>
<section>
  <article>
    <h2>HTML Öğreniyorum</h2>
    <p>Bugün HTML5 semantik etiketlerini öğrendim.</p>
  </article>
</section>
<footer>
  <p>© 2025 Tüm Hakları Saklıdır</p>
</footer>
<video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4">
  Tarayıcınız video etiketini desteklemiyor.
</video>
<audio controls>
  <source src="ornek.mp3" type="audio/mpeg">
  Tarayıcınız ses etiketini desteklemiyor.
</audio>
```

**Ödev:**  
Bir blog sayfası tasarlayın, tüm semantik etiketleri kullanın ve örnek bir video/ses dosyası ekleyin.

---

## Proje ve Modern HTML Uygulamaları

**Açıklama:**  
HTML ile modern bir web sayfası şablonu hazırlamak, meta etiketler ve favicon eklemek, SEO ve kod düzeni konularında bilgi sahibi olmak bu bölümde işlenir.

**Konu Başlıkları ve Açıklamaları:**
- **Meta Etiketler:**  
  - Arama motorları ve sosyal medya için bilgi sağlar.
  - Örnek: `<meta name="description" content="Kişisel portfolyo">`
- **Favicon eklemek:**  
  - Tarayıcı sekmesinde küçük simge.
  - `<link rel="icon" href="favicon.ico">`
- **Sayfa düzeni (Wireframe):**  
  - Kağıt üstünde veya dijital olarak sayfa taslağı çizimi.
- **Kod düzeni ve best-practices:**  
  - Doğru girintileme, anlamlı etiket kullanımı, dosya isimlendirme.

**Örnekler:**
```html
<head>
  <meta charset="UTF-8">
  <meta name="description" content="Kişisel portfolyo sayfam">
  <meta name="author" content="Adınız Soyadınız">
  <link rel="icon" href="favicon.ico" type="image/x-icon">
  <title>Portfolyo</title>
</head>
```

**Proje Uygulaması:**  
Her öğrenci, önce bir portfolyo sayfası wireframe’i çizer (kağıt veya dijital). Sonra HTML ile uygular:  
- Kendi fotoğrafı
- Hakkında bölümü (semantik etiketler ile)
- Eğitim veya iş geçmişi tablosu
- İletişim formu
- Dış bağlantılar ve favicon

**Ödev (Proje):**  
Tüm öğrendiklerinizi kullanarak kişisel portfolyo sayfası oluşturun. Sayfanızda en az bir görsel, tablo, form ve semantik etiketler bulunsun.

---

## Ek Kaynaklar & Tavsiyeler

- **Kod Editörü:** Visual Studio Code, Notepad++
- **Online Kaynaklar:** [W3Schools](https://w3schools.com), [MDN Web Docs](https://developer.mozilla.org/)
- **Ekstra:** Github ile ödev paylaşımı ve kod teslimi için rehberlik
- **Ekstra uygulama:** Her ders sonunda mini quiz ve kod incelemesi

---
