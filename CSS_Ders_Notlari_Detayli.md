# C# Yazılım Uzmanlığı - CSS Ders Notları (Basit ve Bol Örnekli)

---

## CSS Nedir? Nasıl Eklenir?

**Açıklama:**  
CSS, web sayfasının görünümünü ve tasarımını değiştirir.

**Nasıl Eklenir?**
- Sayfa içi: `<style>` etiketiyle
- Harici dosya: `.css` dosyası ile

**Örnek:**
```html
<style>
  p { color: blue; }
</style>
```
veya
```html
<link rel="stylesheet" href="style.css">
```
```css
/* style.css */
body { background-color: #eeeeee; }
```

---

## Renk, Yazı Tipi ve Metin Biçimlendirme

**Açıklama:**  
Metinlerin rengini, boyutunu ve tipini değiştirmek için CSS kullanılır.

**Örnekler:**
```css
h1 { color: red; }
p { color: green; font-size: 18px; font-family: Arial; }
span { font-weight: bold; font-style: italic; }
```
```html
<h1>Başlık</h1>
<p>Yeşil paragraf</p>
<span>Kalın ve italik yazı</span>
```

---

## Kutu Modeli: Kenar, Boşluk, Doldurma

**Açıklama:**  
Her HTML elemanı bir kutu gibidir. Kenarlık, kenar boşluğu (margin) ve iç boşluk (padding) eklenebilir.

**Örnekler:**
```css
div {
  border: 2px solid black;
  margin: 20px;
  padding: 10px;
  background-color: #d0f0c0;
}
```
```html
<div>Bir kutu örneği</div>
```

---

## Arka Plan Rengi ve Resmi

**Açıklama:**  
Sayfa veya kutuların arkasına renk veya resim koyulabilir.

**Örnekler:**
```css
body {
  background-color: #f8e473;
}
.box {
  background-image: url("https://via.placeholder.com/150");
  background-repeat: no-repeat;
  background-size: cover;
  height: 200px;
  width: 200px;
}
```
```html
<div class="box"></div>
```

---

## Elemanları Yerleştirme ve Boyutlandırma

**Açıklama:**  
Elemanların genişliği, yüksekliği ayarlanabilir; yan yana gelmeleri sağlanabilir.

**Örnekler:**
```css
.kucuk { width: 100px; height: 100px; background: #88f; display: inline-block; }
.buyuk { width: 200px; height: 100px; background: #8f8; display: inline-block; }
```
```html
<div class="kucuk"></div>
<div class="buyuk"></div>
```

---

## Hover Efekti (Üzerine Gelince Değişim)

**Açıklama:**  
Fare ile üzerine gelindiğinde renk veya başka bir özellik değiştirilebilir.

**Örnekler:**
```css
button {
  background: #fdd;
  color: #222;
  padding: 10px;
}
button:hover {
  background: #c8f;
  color: #fff;
}
```
```html
<button>Üzerine Gel!</button>
```

---

## Basit Responsive Tasarım (Mobil Uyumlu)

**Açıklama:**  
Ekran küçülünce tasarım değiştirilebilir.

**Örnekler:**
```css
@media (max-width: 600px) {
  body { background: #f0f; }
  h1 { font-size: 20px; }
}
```

---

## Ödevler

1. Sayfanızda en az bir başlık ve paragrafı renklendirin.
2. Bir kutu (div) oluşturun, kenarlık ve arka plan rengi ekleyin.
3. Bir buton ekleyin, hover efekti ile rengi değişsin.
4. Sayfanızı mobilde farklı renge büründürecek bir media query ekleyin.

---

## Ek Tavsiyeler ve Kaynaklar

- **Editörler:** Visual Studio Code, Notepad++
- **Kaynaklar:** [W3Schools CSS](https://w3schools.com/css/), [MDN CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
- Bol bol deneyin ve kendi örneklerinizi yazın!

---
