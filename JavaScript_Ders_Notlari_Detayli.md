# C# Yazılım Uzmanlığı - JavaScript Dersi İçeriği (Açıklamalı ve Örnekli)

---

## JavaScript’e Giriş ve Temel Kullanımı

**Açıklama:**  
JavaScript, web sayfalarına dinamik özellikler kazandırmak için kullanılan bir programlama dilidir. HTML ve CSS ile yapıyı ve tasarımı oluşturduktan sonra, JavaScript ile etkileşim ve mantık eklenir.

**Konu Başlıkları ve Açıklamaları:**
- **JavaScript nedir? Neden kullanılır?**  
  - Web’de etkileşim, animasyon, veri kontrolü ve arka plan işlemler için kullanılır.
- **Sayfaya nasıl eklenir?**  
  - `<script>` etiketi ile HTML dosyasına gömülür veya harici dosya ile bağlanır.
- **Temel yazım kuralları:**  
  - Değişken tanımı, değer atama, fonksiyon oluşturma.

**Örnekler:**
```html
<!-- Sayfa içi JavaScript -->
<script>
  alert('JavaScript çalışıyor!');
</script>

<!-- Harici dosya ile -->
<script src="script.js"></script>
```
```javascript
// script.js
let mesaj = "Merhaba JavaScript!";
console.log(mesaj);
```

**Ödev:**  
Bir HTML sayfasında "Merhaba JavaScript!" mesajı gösteren kodu hem sayfa içi hem harici olarak yazın.

---

## Değişkenler, Veri Tipleri ve Operatörler

**Açıklama:**  
Değişkenler, değer tutmak için kullanılır. Veri tipleri ve operatörler ile sayısal/mantıksal işlemler yapılır.

**Konu Başlıkları ve Açıklamaları:**
- **Değişken tanımı:**  
  - `var`, `let`, `const`
- **Temel veri tipleri:**  
  - String, Number, Boolean, Array, Object
- **Operatörler:**  
  - Aritmetik (+, -, *, /)
  - Karşılaştırma (==, ===, !=, <, >)
  - Mantıksal (&&, ||, !)

**Örnekler:**
```javascript
let ad = "Ali";
const yas = 25;
let aktif = true;
let sayilar = [1, 2, 3, 4];
let kisi = { ad: "Ayşe", soyad: "Kaya" };

console.log(ad + " " + yas);
console.log(aktif && yas > 18); // true
console.log(sayilar[2]); // 3
```

**Ödev:**  
Bir kişinin adı, yaşı ve aktiflik durumunu değişkenlerle tutun, aritmetik ve mantıksal işlemlerle ekrana yazdırın.

---

## Koşullar ve Döngüler

**Açıklama:**  
Koşul ifadeleri ile programın akışını kontrol edebiliriz. Döngülerle tekrar eden işlemler yapılır.

**Konu Başlıkları ve Açıklamaları:**
- **Koşul ifadeleri:**  
  - `if`, `else if`, `else`
  - `switch`
- **Döngüler:**  
  - `for`, `while`, `do...while`
  - Dizi içinde gezinmek için `for...of`, `forEach`

**Örnekler:**
```javascript
let not = 85;
if (not >= 90) {
  console.log("Pekiyi");
} else if (not >= 70) {
  console.log("İyi");
} else {
  console.log("Orta");
}

for(let i = 0; i < 5; i++) {
  console.log("Sayı: " + i);
}

let isimler = ["Ali", "Ayşe", "Mehmet"];
isimler.forEach(function(isim) {
  console.log(isim);
});
```

**Ödev:**  
Bir dizi oluşturun ve tüm elemanlarını döngüyle ekrana yazdırın. Not sistemine göre koşullarla “Geçti/Kaldı” mesajı verin.

---

## Fonksiyonlar ve Olaylar

**Açıklama:**  
Fonksiyonlar kodun tekrar kullanılmasını sağlar. Olaylar sayesinde kullanıcı etkileşimi yakalanır.

**Konu Başlıkları ve Açıklamaları:**
- **Fonksiyon tanımı:**  
  - Geleneksel ve ok fonksiyonu (arrow function)
  - Parametre ve dönüş değeri
- **Olaylar:**  
  - Tıklama, fare, klavye gibi olaylar
  - HTML elementlerine olay ekleme

**Örnekler:**
```javascript
function topla(a, b) {
  return a + b;
}
console.log(topla(2, 3));

const selamla = (isim) => {
  console.log("Merhaba " + isim);
};
selamla("Merve");

// Olay yakalama
document.getElementById("btn").onclick = function() {
  alert("Butona tıklandı!");
};
```
```html
<button id="btn">Tıkla</button>
```

**Ödev:**  
Bir fonksiyon yazın ve ekrana bir mesaj verdirin. Bir butona tıklanınca mesaj gösteren bir olay ekleyin.

---

## DOM Manipülasyonu ve Modern JS Özellikleri

**Açıklama:**  
JavaScript ile sayfa içeriğini (DOM) değiştirebilir, modern ES6+ özelliklerini kullanabilirsiniz.

**Konu Başlıkları ve Açıklamaları:**
- **DOM nedir?**
  - HTML elemanlarına erişim ve değiştirme
- **Temel DOM işlemleri:**  
  - `document.getElementById`, `querySelector`
  - İçerik değiştirme: `innerHTML`, `textContent`
  - Stil değiştirme: `.style`
- **Modern JS:**  
  - Template string: \`${deger}\`
  - Destructuring, spread, map/filter/find

**Örnekler:**
```javascript
// İçeriği değiştirme
document.getElementById("mesaj").textContent = "Yeni mesaj!";

// Stil değiştirme
document.getElementById("mesaj").style.color = "red";

// Modern özellikler
const ogrenci = { ad: "Zeynep", yas: 20 };
const { ad, yas } = ogrenci;
console.log(`Ad: ${ad}, Yaş: ${yas}`);

let sayilar = [1,2,3,4];
let yeniler = sayilar.map(s => s * 2);
console.log(yeniler); // [2,4,6,8]
```
```html
<div id="mesaj">Burada mesaj gözükecek</div>
```

**Ödev:**  
Bir div’in içeriğini ve stilini JavaScript ile değiştirin. Bir diziyi map ile dönüştürüp sonucu ekrana yazdırın.

---

## Ek Kaynaklar & Tavsiyeler

- **Kod Editörü:** Visual Studio Code, Notepad++
- **Online Kaynaklar:** [W3Schools - JS](https://w3schools.com/js/), [MDN JS](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- **Ekstra:** Github ile kod paylaşımı ve ödev teslimi için rehberlik
- **Ekstra uygulama:** Her ders sonunda mini quiz ve kod incelemesi

---

**Not:**  
Derslerde bolca canlı kodlama ve örnek üzerinde uygulama yapınız. Öğrencilerden kendi kodlarını denemelerini ve kodlarını paylaşmalarını isteyiniz.