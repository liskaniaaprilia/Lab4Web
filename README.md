# CSS Layout

### 1. Web Layout
Web layout merupakan kerangka yang mengatur penempatan tata letak sebuah elemen pada halaman web. Tata letak element seperti navigasi, header, tombol CTA (Call to Action), dan elemen lainnya pada halaman web, sehingga tampilan web dapat disesuaikan dengan desain yang ada. Dengan layout website yang tepat, informasi akan tampil dengan lebih menawan dan fungsional. 

### 2. Box Element
Element HTML dapat dianggap sebagai sebuah Box atau kotak. Box tersebut digunakan untuk membuat layout web. Pada dasarnya semua element HTML adalah box dengan beberapa perbedaan. Ada yang floating ada juga yang tanpa floating.

### 3. CSS Float Property
CSS Float Property memungkinkan elemen HTML dibuat seolah-olah mengambang diantara elemen yang lainnya. Dengan konsep tersebut dapat dengan mudah menentukan posisi atau letak sebuah elemen HTML. Sehingga dalam membuat layout web dapat dengan mudah dilakukan. Property yang digunakan untuk mendefinisikan adalah float dan clear.

# Praktikum - 4

1. Pembuatan dokumen HTML
Persiapan membuat dokumen HTML dengan nama file lab4_box.html seperti berikut.

``` HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Box Element</title>
</head>
<body>
    <header>
        <h1>Box Element</h1>
    </header>
</body>
</html>
```

2. Membuat Box Elememt
Kemudian tambahkan kode untuk membuat box element dengan tag div seperti berikut.

```HTML
<section>
    <div class="div1">Div 1</div>
    <div class="div2">Div 2</div>
    <div class="div3">Div 3</div>
</section>
```

3. CSS Float Property
Selanjutnya tambahkan deklarasi CSS pada head untuk membuat float element, seperti berikut.

```HTML
<style>
    div {
    float:left;
    padding: 10px;
    }
    .div1 {
    background: red;
    }
    .div2 {
    background: yellow;
    }
    .div3 {
    background: green;
    }
</style>
```

- Output 

![IMG.1](Screenshot/PNG%20-%201.png)

4. Mengatur Clearfix Element
Clearfix digunakan untuk mengatur element setelah float element. Property clear digunakan untuk
mengaturnya.

- Tambahkan element div lainnya seteleah div3 seperti berikut.

```HTML
<section>
    <div class="div1">Div 1</div>
    <div class="div2">Div 2</div>
    <div class="div3">Div 3</div>
    <div class="div4">Div 4</div>
</section>
```

- Kemudian atur property clear pada CSS, seperti berikut.

```HTML 
<style>
.div4 {
        background-color: blue;
        clear: left;
        float: none;
}
</style>
```

- Output

![IMG.2](Screenshot/PNG%20-%202.png)

5. Membuat Layout Sederhana

- Buat folder baru dengan nama lab4_layout, kemudian buatlah file baru didalamnya dengan nama home.html, dan file css dengan nama style.css.

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
    </div>
</body>
</html>
```

- Kemudian tulis kode berikut.

```HTML
<header>
    <h1>Layout Sederhana</h1>
</header>
<nav>
    <a href="home.html" class="active">Home</a>
    <a href="artikel.html">Artikel</a>
    <a href="about.html">About</a>
    <a href="contact.html">Contact</a>
</nav>
<section id="hero"></section>
<section id="wrapper">
    <section id="main"></section>
    <aside id="sidebar"></aside>
</section>
<footer>
    <p>&copy; 2021 - Universitas Pelita Bangsa</p>
</footer>
```

- Output

![IMG.3](Screenshot/PNG%20-%203.png)

- Kemudian tambahkan kode CSS untuk membuat layoutnya.

```CSS
/* import google font */
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400
;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap');
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0
,300;0,700;1,300&display=swap');

/* Reset CSS */
* {
    margin: 0;
    padding: 0;
}

body {
    line-height:1;
    font-size:100%;
    font-family:'Open Sans', sans-serif;
    color:#5a5a5a;
}

#container {
    width: 980px;
    margin: 0 auto;
    box-shadow: 0 0 1em #cccccc;
}

/* header */
header {
    padding: 20px;
}
header h1 {
    margin: 20px 10px;
    color: #b5b5b5;
}
```

- Output

![IMG.4](Screenshot/PNG%20-%204.png)

6. Membuat Navigasi
Kemudian selanjutnya mengatur navigasi.

```CSS
/* navigasi */
nav {
    display: block;
    background-color: #1f5faa;
    }

nav a {
    padding: 15px 30px;
    display: inline-block;
    color: #ffffff;
    font-size: 14px;
    text-decoration: none;
    font-weight: bold;
    }

nav a.active,
nav a:hover {
    background-color: #2b83ea;
    }
```

- Output

![IMG.5](Screenshot/PNG%20-%205.png)

7. Membuat Hero Panel
Selanjutnya membuat hero panel. Tambahkan kode HTML dan CSS seperti berikut.

```HTML
<section id="hero">
    <h1>Hello World!</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
    <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
</section>
```

```CSS
/* Hero Panel */
#hero {
    background-color: #e4e4e5;
    padding: 50px 20px;
    margin-bottom: 20px;
    }
#hero h1 {
    margin-bottom: 20px;
    font-size: 35px;
    }
#hero p {
    margin-bottom: 20px;
    font-size: 18px;
    line-height: 25px;
    }
```

- Output

![IMG.6](Screenshot/PNG%20-%206.png)

8. Mengatur Layout Main dan Sidebar
Selanjutnya mengatur main content dan sidebar, tambahkan CSS float.

```CSS
/* main content */
#wrapper {
    margin: 0;
    }

#main {
    float: left;
    width: 640px;
    padding: 20px;
    }

/* sidebar area */
#sidebar {
    float: left;
    width: 260px;
    padding: 20px;
    }
```

9. Membuat Sidebar Widget
Kemudian selanjutnya menambahkan element lain dalam sidebar.

```HTML
<aside id="sidebar">
    <div class="widget-box">
        <h3 class="title">Widget Header</h3>
        <ul>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
        </ul>
    </div>
    <div class="widget-box">
        <h3 class="title">Widget Text</h3>
        <p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt
    arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer
    pharetra est nunc, nec pretium nunc pretium ac.</p>
    </div>
</aside>
```

- Kemudian tambahkan CSS.

```CSS
/* widget */
.widget-box {
    border:1px solid #eee;
    margin-bottom:20px;
    }

.widget-box .title {
    padding:10px 16px;
    background-color:#428bca;
    color:#fff;
    }

.widget-box ul {
    list-style-type:none;
    }

.widget-box li {
    border-bottom:1px solid #eee;
    }
.widget-box li a {
    padding:10px 16px;
    color:#333;
    display:block;
    text-decoration:none;
    }
.widget-box li:hover a {
    background-color:#eee;
    }
.widget-box p {
    padding:15px;
    line-height:25px;
    }
```

- Output

![IMG.7](Screenshot/PNG%20-%207.png)

10. Mengatur Footer
Selanjutnya mengatur tampilan footer. Tambahkan CSS untuk footer.

```CSS
/* footer */
footer {
    clear:both;
    background-color:#1d1d1d;
    padding:20px;
    color:#eee;
}
```

- Output

![IMG.8](Screenshot/PNG%20-%208.png)

10. Menambahkan Elemen lainnya pada Main Content

```HTML
<section id="main">
    <div class="row">
        <div class="box">
            <img src="https://dummyimage.com/120/db7d25/fff.png" alt=""
class="image-circle">
            <h3>Heading</h3>
            <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis
    euismod.</p>
            <a href="#" class="btn btn-default">View detail</a>
        </div>
        <div class="box">
            <img src="https://dummyimage.com/120/3e73e6/fff.png" alt=""
class="image-circle">
            <h3>Heading</h3>
            <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis
    euismod.</p>
            <a href="#" class="btn btn-default">View detail</a>
        </div>
        <div class="box">
            <img src="https://dummyimage.com/120/71e6d4/fff.png" alt=""
    class="image-circle">
            <h3>Heading</h3>
            <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis
    euismod.</p>
            <a href="#" class="btn btn-default">View detail</a>
        </div>
    </div>
</section>
```

```CSS
/* box */
.box {
    display:block;
    float:left;
    width:33.333333%;
    box-sizing:border-box;
    -moz-box-sizing:border-box;
    -webkit-box-sizing:border-box;
    padding:0 10px;
    text-align:center;
}

.box h3 {
    margin: 15px 0;
}

.box p {
    line-height: 20px;
    font-size: 14px;
    margin-bottom: 15px;
}

box img {
    border: 0;
    vertical-align: middle;
}

.image-circle {
    border-radius: 50%;
}

.row {
    margin: 0 -10px;
    box-sizing: border-box;
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
}

.row:after, .row:before,
.entry:after, .entry:before {
    content:'';
    display:table;
}

.row:after,
.entry:after {
    clear:both;
}
```

- Output

![IMG.9](Screenshot/PNG%20-%209.png)

11. Menambahkan Content Artikel
Selanjutnya membuat content artikel. Tambahkan HTML berikut pada main content.

```HTML
<hr class="divider" />
    <article class="entry">
        <h2>First featurette heading.</h2>
        <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
    elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
    vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
    pretium ac.</p>
    </article>
    <hr class="divider" />
    <article class="entry">
        <h2>First featurette heading.</h2>
        <img src="https://dummyimage.com/150/7b8a70/fff.png" alt=""
    class="right-img">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
    elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
    vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
    pretium ac.</p>
    </article>
```

- Kemudian tambahkan CSS.

```CSS
.divider {
    border:0;
    border-top:1px solid #eeeeee;
    margin:40px 0;
    }

/* entry */
.entry {
    margin: 15px 0;
    }

.entry h2 {
    margin-bottom: 20px;
}

.entry p {
    line-height: 25px;
}

.entry img {
    float: left;
    border-radius: 5px;
    margin-right: 15px;
}

.entry .right-img {
    float: right;
}
```

- Output

![IMG.10](Screenshot/PNG%20-%2010.png)

### Pertanyaan dan Tugas

1. Tambahkan Layout untuk menu About
=> buat single layout yang berisi deskripsi, portfolio, dll

```HTML
<!DOCTYPE html>
<html>
<head>
    <title>About Us</title>
    <style>
        body {
            font-family: 'Times New Roman', Times, serif;
            background-color: #ffffff;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #2fabfd;
            color: #fff;
            text-align: center;
            padding: 10px;
        }

        nav {
            background-color: #b6d8ff;
            padding: 10px;
        }

        nav ul {
            list-style: none;
            padding: 0;
        }

        nav li {
            display: inline;
            margin-right: 10px;
        }

        .container {
            width: 80%;
            margin: 0 auto;
            padding: 20px;
            background-color: #fff;
        }

        .about-section {
            background-color: #abe6f8;
            padding: 20px;
        }

        .about-section h2 {
            color: #333;
        }

        .about-section h3 {
            color: #333;
        }

        .about-section p {
            margin-bottom: 15px;
        }
    </style>
</head>
<body>
    <header>
        <h1>About</h1>
    </header>
    <div class="container">
        <div class="about-section">
            <h2>About Us</h2>
            <p>Website layout merupakan kerangka yang mengatur tata letak navigasi, tombol CTA, dan elemen lainnya pada website. 
            Dengan layout website yang tepat, informasi akan tampil dengan lebih menawan dan fungsional.
            Halaman web sering kali dibagi menjadi header, menu, konten, dan footer: Ada banyak sekali desain tata letak yang dapat dipilih.</p>
            <p> - Sebuah elemen HTML dapat kita anggap sebagai sebuah box/
                kotak. </p>
            <p> - Digunakan pada saat merancang layout tampilan sebuah
                website.</p>
            <P> - Pada dasarnya berfungsi sebagai tempat yang membungkus isi
                dari elemen elemen HTML.</P> 
            <P> - Tag yang biasanya digunakan untuk merancang tampilan adalah
                <div>, walaupun tag lain juga bisa menerapkan box model.</P>
            <P> - Terdiri atas 4 bagian: Margin, Border, Padding, Content.</p>
            
            <h3>About Me</h3>
            <div class="contact-info">
                <p>Name: Liskania Aprilia </p>
                <p>Address: Grand Cikarang City Blok G 33/17</p>
                <p>Message: 0838 - 9762 - 1933</p>
                <p>Email: <a href="liskaniaaprilia172004@gmail.com">liskaniaaprilia172004@gmail.com</a></p>
            </div>
        </div>
    </div>
</body>
</html>
```

- Output
![IMG.11](Screenshot/PNG%20-%2011.png)

2. Tambahkan layout untuk menu Contact
=> yang berisi form isian: nama, email, message, dll

```HTML
<!DOCTYPE html>
<html>
<head>
    <title>Contact Person</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #fd569c;
            color: #fff;
            text-align: center;
            padding: 10px;
        }

        nav {
            background-color: #ffe1f6;
            padding: 10px;
        }

        nav ul {
            list-style: none;
            padding: 0;
        }

        nav li {
            display: inline;
            margin-right: 10px;
        }

        .container {
            width: 60%;
            margin: 0 auto;
            padding: 10px;
            background-color: #fab9e4;
        }

        .contact-info {
            background-color: #ffd2ec;
            padding: 20px;
        }

        form {
            max-width: 400px;
            margin: 0 auto;
        }

        label, input, textarea {
            display: block;
            margin-bottom: 10px;
        }

    </style>
</head>
<body>
    <header>
        <h1>Contact Person</h1>
    </header>
    <div class="container">
        <section id="contact" class="contact">

            <head>
                <title>Formulir Kontak</title>
            </head>
            <body>
                <form action="proses_formulir.php" method="post">
                    <label for="nama">Nama :</label>
                    <input type="text" id="nama" name="nama" required>
            
                    <label for="email">Email :</label>
                    <input type="email" id="email" name="email" required>
            
                    <label for="pesan">Message :</label>
                    <textarea id="pesan" name="pesan" rows="4" required></textarea>
            
                    <input type="submit" value="Submit">
                </form>
            </body>     
            
        </section>
    </div>
</body>
</html>
```

- Output
![IMG.12](Screenshot/PNG%20-%2012.png)

# FINISH