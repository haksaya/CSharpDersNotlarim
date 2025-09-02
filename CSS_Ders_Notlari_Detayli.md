# C# Yazılım Uzmanlığı - CSS Dersi İçeriği (Açıklamalı ve Örnekli)

---

## CSS’e Giriş ve Temel Kullanımı

**Açıklama:**  
CSS, web sayfalarının görünümünü ve düzenini kontrol etmek için kullanılır. HTML ile yapı kurulur, CSS ile tasarım yapılır. Bu bölümde CSS’in sayfaya nasıl eklendiği ve temel yazım kuralları anlatılır.

**Konu Başlıkları ve Açıklamaları:**
- **CSS nedir? Neden kullanılır?**
  - Renk, yazı tipi, boşluk, kenarlık ve konumlandırma için kullanılır.
- **CSS nasıl eklenir?**
  - Satır içi (`style` özniteliği)
  - Sayfa içi (`<style>` etiketi ile)
  - Harici dosya (`.css` dosyası ile `<link rel="stylesheet">`)
- **Temel söz dizimi:**
  - Seçici { özellik: değer; }

**Örnekler:**
```html
<!-- Harici dosya ile -->
<link rel="stylesheet" href="style.css">

<!-- Sayfa içi stil -->
<style>
  p { color: blue; }
</style>

<!-- Satır içi stil -->
<p style="color: green;">Yeşil Paragraf</p>
```
```css
/* style.css */
body { background-color: #f2f2f2; }
h1   { color: darkred; }
```

**Ödev:**  
Bir HTML sayfanızı hem sayfa içi hem harici CSS ile renklendirin ve başlık/paragrafları biçimlendirin.

---

## Seçiciler ve Metin Biçimlendirme

**Açıklama:**  
CSS seçicileri ile belirli HTML elemanlarını hedefleyip stillendirmek mümkündür. Metin ile ilgili özellikler sayfanın okunabilirliğini artırır.

**Konu Başlıkları ve Açıklamaları:**
- **Temel seçiciler:**  
  - Etiket seçici: `p { ... }`
  - Sınıf seçici: `.kirmizi { ... }`
  - ID seçici: `#ozel { ... }`
  - Çoklu seçici: `h1, h2 { ... }`
- **Metin biçimlendirme:**  
  - Renk: `color`
  - Yazı tipi: `font-family`
  - Boyut: `font-size`
  - Kalınlık: `font-weight`
  - Stil: `font-style`
  - Hizalama: `text-align`

**Örnekler:**
```css
h1 { color: navy; }
.kirmizi { color: red; }
#ozel { font-size: 24px; font-style: italic; }
p { font-family: Arial, Helvetica, sans-serif; }
h2, h3 { text-align: center; }
```
```html
<h1>Başlık</h1>
<p class="kirmizi">Bu kırmızı bir paragraf.</p>
<p id="ozel">Bu özel bir paragraf.</p>
```

**Ödev:**  
Sayfanızda farklı başlıkları ve paragrafları seçici kullanarak biçimlendirin. En az bir sınıf ve bir ID seçicisi kullanın.

---

## Kutu Modeli ve Arka Planlar

**Açıklama:**  
CSS’de her eleman bir kutudur. Kutu modeli (box model) ile kenar boşlukları, doldurma (padding), kenarlık (border) ve arka planları yönetebilirsiniz.

**Konu Başlıkları ve Açıklamaları:**
- **Kutu modeli nedir?**
  - `width`, `height`, `padding`, `margin`, `border`
- **Arka plan özellikleri:**  
  - Renk: `background-color`
  - Resim: `background-image`
  - Tekrar: `background-repeat`
  - Konum: `background-position`
- **Kenarlık ayarları:**  
  - `border-width`, `border-style`, `border-color`
- **Kutu gölgeleri:**  
  - `box-shadow`

**Örnekler:**
```css
.box {
  width: 300px;
  padding: 20px;
  margin: 10px auto;
  border: 2px solid #333;
  background-color: #e0ffff;
  box-shadow: 2px 2px 8px #888;
}
body {
  background-image: url('arka_plan.jpg');
  background-repeat: no-repeat;
  background-size: cover;
}
```
```html
<div class="box">Kutu Modeli Uygulaması</div>
```

**Ödev:**  
Bir kutu (div) oluşturun. Kenar boşluğunu, doldurmayı, kenarlığı ve arka plan rengini ayarlayın. Sayfaya arka plan resmi ekleyin.

---

## Konumlandırma, Yerleşim ve Görsel Biçimlendirme

**Açıklama:**  
Sayfa düzenini kurmak için elemanları farklı şekillerde konumlandırabilir ve görselleri biçimlendirebilirsiniz.

**Konu Başlıkları ve Açıklamaları:**
- **Konumlandırma:**  
  - `position: static, relative, absolute, fixed, sticky`
  - `top`, `left`, `right`, `bottom`
- **Yüzen elemanlar:**  
  - `float`, `clear`
- **Görsel biçimlendirme:**  
  - Genişlik/yükseklik: `width`, `height`
  - Kenarlık, yuvarlatma: `border-radius`
  - Görselin hizalanması

**Örnekler:**
```css
.resim {
  width: 150px;
  border-radius: 10px;
  float: left;
  margin-right: 20px;
}
.kapsayici {
  position: relative;
  top: 50px;
  left: 30px;
  background: #fff8dc;
  padding: 15px;
}
```
```html
<img src="profil.jpg" class="resim" alt="Profil Foto">
<div class="kapsayici">Bu kutu, sayfanın belli bir yerine konumlandırıldı.</div>
```

**Ödev:**  
Sayfanızda bir görseli biçimlendirin, bir kutuyu konumlandırın ve en az bir elemanı yüzen olarak ayarlayın.

---

## Responsive Tasarım ve Modern CSS Özellikleri

**Açıklama:**  
Farklı ekran boyutlarında iyi görünen sayfalar tasarlamak için responsive (duyarlı) tasarım teknikleri ve modern CSS özellikleri kullanılır.

**Konu Başlıkları ve Açıklamaları:**
- **Responsive tasarım:**  
  - `@media` sorguları ile ekran boyutuna göre stil değiştirme
- **Flexbox:**  
  - Kolay yerleşim için: `display: flex`, `justify-content`, `align-items`
- **Grid Layout:**  
  - Karmaşık yerleşimler için: `display: grid`
- **Geçişler ve animasyonlar:**  
  - `transition`, `animation`

**Örnekler:**
```css
@media (max-width: 600px) {
  body { background-color: #ffd700; }
  h1 { font-size: 20px; }
}
.flex-kapsayici {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.kutu {
  width: 100px;
  height: 100px;
  background: #aaf;
  transition: background 0.3s;
}
.kutu:hover {
  background: #faa;
}
```
```html
<div class="flex-kapsayici">
  <div class="kutu">1</div>
  <div class="kutu">2</div>
  <div class="kutu">3</div>
</div>
```

**Ödev:**  
Sayfanızı mobil cihazlar için uyumlu hale getirin. Flexbox ile yan yana kutular oluşturun ve bir kutuya hover efektli geçiş ekleyin.

---

## Ek Kaynaklar & Tavsiyeler

- **Kod Editörü:** Visual Studio Code, Notepad++
- **Online Kaynaklar:** [W3Schools - CSS](https://w3schools.com/css/), [MDN CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
- **Ekstra:** Github ile ödev paylaşımı ve kod teslimi için rehberlik
- **Ekstra uygulama:** Her ders sonunda mini quiz ve kod incelemesi

---

**Not:**  
Derslerde bolca canlı kodlama ve örnek üzerinde uygulama yapınız. Öğrencilerden kendi stillerini denemelerini ve kodlarını paylaşmalarını isteyiniz.