# Lab2Web

## Langkah-langkah Praktikum

1. Membuat dokumen HTML
Buatlah dokumen HTML seperti berikut
```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CSS Dasar</title>
</head>
<body>
<header>
<h1>CSS Internal dan <i>Inline CSS</i></h1>
</header>
<nav>
<a href="lab2_css_dasar.html">CSS Dasar</a>
<a href="lab2_css_eksternal.html">CSS Eksternal</a>
<a href="lab1_tag_dasar.html">HTML Dasar</a>
</nav>
<!-- CSS ID Selector -->
<div id="intro">
<h1>Hello World</h1>
<p>Kami sedang belajar HTML dan CSS dasar, pada mata kuliah <b>Pemrograman
Web</b> di <i>Universitas Pelita Bangsa</i>. Pelajaran pertama yang kami dapat
adalah membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar HTML
dan CSS.</p>
<!-- CSS Class Selector -->
<a class="button btn-primary" href="#intro">Informasi selengkapnya.</a>
</div>
</body>
</html>
```
Selanjutnya buka pada brwoser untuk melihat hasilnya.
![image](https://github.com/ZahraNurhaliza/Lab2Web/blob/main/screenshot/ss.1.png)


2. Mendeklarasikan CSS Internal
Kemudian tambahkan deklarasi CSS internal seperti berikut pada bagian head dokumen.
```html
<head>
<title>CSS Dasar</title>
<style>
body {
font-family:'Open Sans', sans-serif;
}
header {
min-height: 80px;
border-bottom:1px solid #77CCEF;
}
h1 {
font-size: 24px;
color: #0F189F;
text-align: center;
padding: 20px 10px;
}
h1 i {
color:#6d6a6b;
}
</style>
</head>
```
Selanjutnya buka pada brwoser untuk melihat hasilnya.
![image](https://github.com/ZahraNurhaliza/Lab2Web/blob/main/screenshot/ss.2.png)


3. Menambahkan Inline CSS
Kemudian tambahkan deklarasi inline CSS pada tag ```html 
 <p>``` seperti berikut.
```html
<p style="text-align: center; color: #ccd8e4;">
```
Selanjutnya buka pada brwoser untuk melihat hasilnya.
![image](https://github.com/ZahraNurhaliza/Lab2Web/blob/main/screenshot/ss.3.png)


4. Membuat CSS Eksternal
Buatlah file baru dengan nama style_eksternal.css kemudian buatlah deklarasi CSS seperti berikut.
Kemudian tambahkan tag ```html
<link>``` untuk merujuk file css yang sudah dibuat pada bagian ```html
<head>```

```css
nav {
background: #20A759;
color:#fff;
padding: 10px;
}
nav a {
color: #fff;
text-decoration: none;
padding:10px 20px;
}
nav .active,
nav a:hover {
background: #0B6B3A;
}
```
```html
<head>
<!-- menyisipkan css eksternal -->
<link rel="stylesheet" href="style_eksternal.css" type="text/css">
```
Selanjutnya buka pada brwoser untuk melihat hasilnya.
![image](https://github.com/ZahraNurhaliza/Lab2Web/blob/main/screenshot/ss.4.png)


5. Menambahkan CSS Selector
Selanjutnya menambahkan CSS Selector menggunakan ID dan Class Selector. Pada file
style_eksternal.css, tambahkan kode berikut.
```css
/* ID Selector */
#intro {
background: #418fb1;
border: 1px solid #099249;
min-height: 100px;
padding: 10px;
}
#intro h1 {
text-align: left;
border: 0;
color: #fff;
}
/* Class Selector */
.button {
padding: 15px 20px;
background: #bebcbd;
color: #fff;
display: inline-block;
margin: 10px;
text-decoration: none;
}
.btn-primary {
background: #E42A42;
}
```
Selanjutnya buka pada brwoser untuk melihat hasilnya.
![image](https://github.com/ZahraNurhaliza/Lab2Web/blob/main/screenshot/ss.5.png)



## Pertanyaan dan Tugas

1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS
dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.
• Disini saya melakukan perubahan pada warna dan ini lah hasilnya
```css
nav {
    background: #F08080;
    color:#fff;
    padding: 10px;
    }
    nav a {
    color: #fff;
    text-decoration: none;
    padding:10px 20px;
    }
    nav .active,
    nav a:hover {
    background: #0B6B3A;
    }
/* ID Selector */
#intro {
    background: #FFF0F5;
    border: 1px solid #099249;
    min-height: 100px;
    padding: 10px;
    }
    #intro h1 {
    text-align: left;
    border: 0;
    color: #fff;
    }
    /* Class Selector */
    .button {
    padding: 15px 20px;
    background: #bebcbd;
    color: #fff;
    display: inline-block;
    margin: 10px;
    text-decoration: none;
    }
    .btn-primary {
    background: #DC143C;
    }
```
![image](https://github.com/ZahraNurhaliza/Lab2Web/blob/main/screenshot/ss.6.png)


2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan
penjelasannya!
•Pendeklarasian CSS h1 {...} dan #intro h1 {...} memiliki perbedaan dalam cara mereka memilih elemen HTML yang akan diberi gaya. Ini terkait dengan penggunaan selektor CSS dan cara mereka memengaruhi elemen-elemen tersebut. Berikut penjelasan perbedaan antara keduanya:

- h1 {...}:
Ini adalah contoh dari selektor umum (atau sering disebut juga selektor tipe).
Ini akan memilih semua elemen <h1> di seluruh dokumen HTML.
Gaya yang didefinisikan dalam blok CSS ini akan diterapkan pada semua elemen <h1> dalam dokumen.

- #intro h1 {...}:
Ini adalah contoh dari selektor turunan (descendant selector).
Ini akan memilih semua elemen <h1> yang berada di dalam elemen dengan ID "intro".
Gaya yang didefinisikan dalam blok CSS ini hanya akan diterapkan pada elemen-elemen <h1> yang berada dalam elemen dengan ID "intro".


3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada
elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan
penjelasan dan contohnya!
• Ketika ada deklarasi CSS yang didefinisikan secara internal (di dalam tag style dalam dokumen HTML), CSS eksternal (didefinisikan di dalam file eksternal CSS yang dihubungkan dengan dokumen HTML menggunakan tag link ), dan juga inline CSS (didefinisikan langsung di dalam atribut style pada elemen HTML yang sama), maka urutan prioritas atau cascading order yang berlaku adalah sebagai berikut:

- Inline CSS: Deklarasi CSS yang didefinisikan secara inline pada elemen HTML akan memiliki prioritas tertinggi. Ini berarti deklarasi yang didefinisikan dalam atribut style akan menggantikan deklarasi lainnya.
- Internal CSS: Deklarasi yang didefinisikan di dalam tag <style> dalam dokumen HTML akan memiliki prioritas di bawah inline CSS. Ini berarti jika ada konflik antara deklarasi internal dan inline, deklarasi inline yang akan berlaku.
- External CSS: Deklarasi CSS yang didefinisikan dalam file eksternal CSS yang dihubungkan dengan dokumen HTML menggunakan tag link akan memiliki prioritas terendah. Ini berarti jika tidak ada deklarasi inline atau jika deklarasi internal tidak mencakup aturan tertentu, maka deklarasi eksternal yang akan diterapkan.


4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut
terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser?
Berikan penjelasan dan contohnya!
 ```html
( <p id="paragraf-1" class="text-paragraf"> )
```
• Ketika sebuah elemen HTML memiliki ID dan class, CSS akan memprioritaskan deklarasi berdasarkan ID daripada class. Ini karena ID adalah selector yang lebih spesifik daripada class. Jadi, jika ada deklarasi yang sama untuk ID dan class yang sama pada elemen yang sama,deklarasi yang berlaku adalah deklarasi ID.
• conntohnya 
```html
<!DOCTYPE html>
<html>
<head>
<style>
#paragraf-1 {
    color: red;
}

.text-paragraf {
  color: blue;
}
</style>
</head>
<body>
    <p id="paragraf-1" class="text-paragraf">Ini adalah teks paragraf.</p>
</body>
</html>
```
Maka dengan ini hasil dari tulisan "Ini adalah teks paragraf" berwarna merah

## SELESAI