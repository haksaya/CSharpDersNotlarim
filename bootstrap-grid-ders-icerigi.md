# Bootstrap Grid Sistemi – Ders İçeriği

## 1. Bootstrap Grid Sisteminin Temeli

**Grid nedir?**
- Sayfayı satır (row) ve sütunlara (column) bölen, esnek ve duyarlı (responsive) bir yapıdır.
- Bootstrap’te grid sistemi 12 sütundan oluşur.

---

## 2. Temel Yapı

```html
<div class="container">
  <div class="row">
    <div class="col">Sütun 1</div>
    <div class="col">Sütun 2</div>
    <div class="col">Sütun 3</div>
  </div>
</div>
```
- Her `.col` eşit genişlikte olur ve toplamda 12’ye bölünür.

---

## 3. Sütun Genişliklerini Belirlemek

```html
<div class="row">
  <div class="col-4">4 Birim</div>
  <div class="col-8">8 Birim</div>
</div>
```
- Toplam 12 birim olmalı.

---

## 4. Duyarlı (Responsive) Grid Kullanımı

```html
<div class="row">
  <div class="col-12 col-md-6">Sol</div>
  <div class="col-12 col-md-6">Sağ</div>
</div>
```
- Küçük ekranda alt alta, büyük ekranda yan yana olur.

---

## 5. Daha Fazla Örnek

**3 Sütunlu Galeri:**
```html
<div class="row">
  <div class="col-12 col-md-4">Fotoğraf 1</div>
  <div class="col-12 col-md-4">Fotoğraf 2</div>
  <div class="col-12 col-md-4">Fotoğraf 3</div>
</div>
```

**Farklı Sütun Dağılımı:**
```html
<div class="row">
  <div class="col-3">Menü</div>
  <div class="col-9">İçerik</div>
</div>
```

---

## 6. Offset (Kaydırma) Kullanımı

```html
<div class="row">
  <div class="col-6 offset-3">Ortalanmış Sütun</div>
</div>
```
- `offset-3` ile 3 sütun sağdan boşluk bırakılır.

---

## 7. Sıralama (Order) ve Hizalama (Align)

**Sıralama:**
```html
<div class="row">
  <div class="col order-2">2. Sütun</div>
  <div class="col order-1">1. Sütun</div>
</div>
```

**Dikey Hizalama:**
```html
<div class="row align-items-center" style="height: 150px;">
  <div class="col">Ortalanmış</div>
</div>
```

---

## 8. İç içe Grid (Nested Grid)

```html
<div class="row">
  <div class="col-8">
    <div class="row">
      <div class="col-6">A</div>
      <div class="col-6">B</div>
    </div>
  </div>
  <div class="col-4">C</div>
</div>
```

---

## 9. Pratik Uygulama: Duyarlı Kartlar

```html
<div class="container">
  <div class="row">
    <div class="col-12 col-sm-6 col-lg-3">
      <div class="card">Kart 1</div>
    </div>
    <div class="col-12 col-sm-6 col-lg-3">
      <div class="card">Kart 2</div>
    </div>
    <div class="col-12 col-sm-6 col-lg-3">
      <div class="card">Kart 3</div>
    </div>
    <div class="col-12 col-sm-6 col-lg-3">
      <div class="card">Kart 4</div>
    </div>
  </div>
</div>
```

---

## 10. Sık Yapılan Hatalar ve İpuçları

- Sütun toplamı bir satırda her zaman 12 olmalı.
- Satır ve sütun yapısı dışına çıkmamaya dikkat edin.
- Responsive sınıfları kullanarak her ekrana uygun tasarım yapın.

---

## 11. Faydalı Kaynaklar

- [Bootstrap Grid Dokümantasyonu](https://getbootstrap.com/docs/5.3/layout/grid/)
- [Bootstrap Örnekleri](https://getbootstrap.com/docs/5.3/examples/)
