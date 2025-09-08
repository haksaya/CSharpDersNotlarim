# C# Yazılım Uzmanlığı - Bootstrap Ders Notları (Basit ve Bol Örnekli)

---

## Bootstrap Nedir? Nasıl Eklenir?

**Açıklama:**  
Bootstrap, hazır tasarım ve düzen bileşenleri sağlayan popüler bir CSS framework’üdür. Web sayfalarını hızlıca şık ve mobil uyumlu yapmak için kullanılır.

**Nasıl Eklenir?**
- CDN ile eklenir (en kolay yol):

**Örnek:**
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css">
```

---

## Hazır Butonlar

**Açıklama:**  
Bootstrap ile farklı renk ve şekillerde butonlar ekleyebilirsiniz.

**Örnekler:**
```html
<button class="btn btn-primary">Mavi Buton</button>
<button class="btn btn-success">Yeşil Buton</button>
<button class="btn btn-danger">Kırmızı Buton</button>
<button class="btn btn-outline-secondary">Çerçeveli Buton</button>
```

---

## Başlıklar ve Metinler

**Açıklama:**  
Başlık ve metinleri kolayca biçimlendirebilirsiniz.

**Örnekler:**
```html
<h1 class="display-1">Büyük Başlık</h1>
<p class="text-muted">Soluk renkli metin</p>
<p class="text-success">Yeşil metin</p>
<p class="fw-bold">Kalın metin</p>
```

---

## Kutu ve Kartlar (Card)

**Açıklama:**  
Bilgi kutuları ve kartlarla içerik sunabilirsiniz.

**Örnekler:**
```html
<div class="card" style="width: 18rem;">
  <img src="https://via.placeholder.com/150" class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">Kart Başlığı</h5>
    <p class="card-text">Kart içeriği buraya yazılır.</p>
    <a href="#" class="btn btn-primary">Detay</a>
  </div>
</div>
```

---

## Grid Sistemi ve Kolonlar

**Açıklama:**  
Sayfa düzeni için kolayca satır ve sütunlar (kolonlar) oluşturulur.

**Örnekler:**
```html
<div class="container">
  <div class="row">
    <div class="col-4 bg-primary text-white">1. Sütun</div>
    <div class="col-4 bg-warning">2. Sütun</div>
    <div class="col-4 bg-success text-white">3. Sütun</div>
  </div>
</div>
```

---

## Formlar

**Açıklama:**  
Bootstrap ile şık ve düzenli formlar hazırlanabilir.

**Örnekler:**
```html
<form>
  <div class="mb-3">
    <label for="email" class="form-label">Email adresi</label>
    <input type="email" class="form-control" id="email">
  </div>
  <div class="mb-3">
    <label for="sifre" class="form-label">Şifre</label>
    <input type="password" class="form-control" id="sifre">
  </div>
  <button type="submit" class="btn btn-primary">Giriş Yap</button>
</form>
```

---

## Resim ve İkonlar

**Açıklama:**  
Resimler ve ikonları kolayca ekleyebilirsiniz.

**Örnekler:**
```html
<img src="https://via.placeholder.com/100" class="img-fluid rounded" alt="Responsive Resim">
<!-- Bootstrap ikonları için ayrı CDN ekleyin -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.5/font/bootstrap-icons.css">
<i class="bi bi-alarm" style="font-size: 2rem; color: red;"></i>
```

---

## Navigasyon Bar (Menü)

**Açıklama:**  
Kolayca mobil uyumlu üst menü oluşturabilirsiniz.

**Örnekler:**
```html
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Logo</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item"><a class="nav-link active" href="#">Ana Sayfa</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Hakkında</a></li>
        <li class="nav-item"><a class="nav-link" href="#">İletişim</a></li>
      </ul>
    </div>
  </div>
</nav>
```

---

## Ödevler

1. Sayfanıza mavi ve yeşil iki buton ekleyin.
2. Bir kart (card) içinde bir başlık ve metin gösterin.
3. Grid sistemiyle 3 sütun oluşturun ve her birine farklı arka plan verin.
4. Bootstrap ile basit bir form ekleyin.
5. Sayfanızın en üstüne bir navigasyon bar ekleyin.

---

## Ek Tavsiyeler ve Kaynaklar

- **Kaynaklar:** [Bootstrap Resmi Sitesi](https://getbootstrap.com/), [Bootstrap Components](https://getbootstrap.com/docs/5.3/components/)
- Her örneği kopyalayıp kendi sayfanızda deneyin!

---
