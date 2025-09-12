# JavaScript DOM Ders İçeriği

---

## 1. DOM Nedir? Nasıl Çalışır?

- **DOM (Document Object Model)**, bir web sayfasının HTML yapısını ağaç şeklinde temsil eder ve JavaScript ile bu yapıya erişip değiştirebilmemizi sağlar.
- Her HTML etiketi bir "node" (düğüm) olarak kabul edilir.

**Örnek:**
```html
<body>
  <h1>Başlık</h1>
  <p>Paragraf</p>
</body>
```
Bu yapı DOM’da şöyle görünür:
```
document
 └── html
      └── body
           ├── h1
           └── p
```

---

## 2. DOM'da Eleman Seçme Yöntemleri

### 2.1 ID ile Seçme
```html
<p id="msg">Merhaba!</p>
<button onclick="degistir()">Değiştir</button>
<script>
  function degistir() {
    document.getElementById("msg").innerHTML = "Değişti!";
  }
</script>
```
**Açıklama:**  
`getElementById("msg")` kodu ile `id`'si "msg" olan etiketi seçiyoruz ve içeriğini değiştiriyoruz.

---

### 2.2 Class ile Seçme
```html
<div class="kutu">Kutu1</div>
<div class="kutu">Kutu2</div>
<script>
  var kutular = document.getElementsByClassName("kutu");
  kutular[0].style.background = "yellow";
  kutular[1].style.background = "lightblue";
</script>
```
**Açıklama:**  
Aynı class’a sahip birden fazla eleman seçilebilir; dizi gibi indekslenir.

---

### 2.3 Tag ile Seçme
```html
<p>Birinci</p>
<p>İkinci</p>
<script>
  document.getElementsByTagName("p")[1].innerHTML = "İkinci Paragraf";
</script>
```

---

### 2.4 querySelector ve querySelectorAll
```html
<p class="mesaj">Mesaj1</p>
<p class="mesaj">Mesaj2</p>
<script>
  document.querySelector(".mesaj").style.color = "green"; // İlk mesajı seçer
  document.querySelectorAll(".mesaj")[1].style.color = "blue"; // İkinci mesajı seçer
</script>
```
**Açıklama:**  
CSS seçici kuralları ile tek veya birden fazla eleman seçilebilir.

---

## 3. İçerik ve Özellik Değiştirme

### 3.1 innerHTML, textContent
```html
<p id="bilgi">Bilgi</p>
<button onclick="degistir()">Değiştir</button>
<script>
  function degistir() {
    document.getElementById("bilgi").innerHTML = "<b>Kalın</b> metin";
    document.getElementById("bilgi").textContent = "Sadece düz metin";
  }
</script>
```
**Açıklama:**  
- `innerHTML`: HTML kodunu değiştirmeye yarar.
- `textContent`: Sadece metni değiştirir.

---

### 3.2 Özellik (Attribute) Değiştirme
```html
<img id="resim" src="ilk.jpg">
<button onclick="degistir()">Resmi Değiştir</button>
<script>
  function degistir(){
    document.getElementById("resim").setAttribute("src", "ikinci.jpg");
  }
</script>
```
**Açıklama:**  
`setAttribute` ile HTML etiketinin herhangi bir özelliği değiştirilebilir.

---

### 3.3 Stil (CSS) Değiştirme
```html
<p id="stil">Stil değişecek</p>
<button onclick="renkDegistir()">Renk Değiştir</button>
<script>
  function renkDegistir(){
    var p = document.getElementById("stil");
    p.style.color = "purple";
    p.style.fontSize = "24px";
    p.style.background = "#eee";
  }
</script>
```
**Açıklama:**  
Her HTML elemanının stilleri doğrudan değiştirilebilir.

---

## 4. Yeni Eleman Ekleme, Silme, Taşıma

### 4.1 Yeni Eleman Ekleme (createElement, appendChild)
```html
<ul id="liste"></ul>
<button onclick="ekle()">Ekle</button>
<script>
  function ekle() {
    var li = document.createElement("li");
    li.textContent = "Yeni Eleman";
    document.getElementById("liste").appendChild(li);
  }
</script>
```
**Açıklama:**  
Yeni bir etiket oluşturup mevcut bir etikete ekleyebiliriz.

---

### 4.2 Eleman Silme (removeChild)
```html
<ul id="liste">
  <li>Silinecek</li>
</ul>
<button onclick="sil()">Sil</button>
<script>
  function sil() {
    var liste = document.getElementById("liste");
    var eleman = liste.children[0];
    liste.removeChild(eleman);
  }
</script>
```
**Açıklama:**  
Seçilen bir etiketi DOM’dan kaldırmak için kullanılır.

---

## 5. Olaylar (Events) ve Etkileşim

### 5.1 Olay Dinleyici Ekleme
```html
<button id="btn">Tıkla</button>
<script>
  document.getElementById("btn").addEventListener("click", function() {
    alert("Tıklama algılandı!");
  });
</script>
```

---

### 5.2 Form Kontrolü Örneği
```html
<form id="form">
  <input type="text" id="isim" placeholder="Adınız">
  <button type="submit">Gönder</button>
</form>
<script>
  document.getElementById("form").addEventListener("submit", function(e){
    e.preventDefault();
    var ad = document.getElementById("isim").value;
    if(ad === "") {
      alert("Adınızı giriniz!");
    } else {
      alert("Merhaba " + ad);
    }
  });
</script>
```
**Açıklama:**  
Form gönderildiğinde JavaScript ile kontrol sağlanır.

---

## 6. Mini Uygulama: Dinamik Liste

```html
<input type="text" id="girdi" placeholder="Yeni eleman">
<button onclick="ekle()">Ekle</button>
<ul id="dinamikListe"></ul>
<script>
  function ekle() {
    var veri = document.getElementById("girdi").value;
    if(veri.trim() === "") return;
    var li = document.createElement("li");
    li.textContent = veri;
    document.getElementById("dinamikListe").appendChild(li);
    document.getElementById("girdi").value = "";
  }
</script>
```
**Açıklama:**  
Kullanıcıdan veri alıp DOM’a yeni eleman eklenir.

---

## 7. İpuçları ve Sık Hatalar

- Eleman seçerken doğru ID, class ve tag ismi kullanın.
- Olay dinleyicileri eklerken, seçtiğiniz elemanın var olduğundan emin olun.
- Kodunuzu küçük parçalara bölerek test edin.
- DOM ile çalışırken güvenlik için kullanıcıdan gelen veriyi kontrol edin.

---

## Kaynaklar

- [W3Schools DOM](https://www.w3schools.com/js/js_htmldom.asp)
- [MDN DOM](https://developer.mozilla.org/tr/docs/Web/API/Document_Object_Model)
