# Data Diri
Nama : Ridwan Setio Budi
NIM : 2205101005
## HTML Yang Awal
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Semantic HTML</title>
    <link rel="stylesheet" href="assets/styles/styles.css">
</head>
<body>
    <header>
        <h1>HTML5 Semantic</h1>
    </header>
    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#pengertian">Pengertian</a></li>
            <li><a href="#kesimpulan">Kesimpulan</a></li>
        </ul>
    </nav>
    <section>
        Konten
    </section>
    <footer>
        Copyright
    </footer>
</body>
</html>
```

HTML di atas menggunakan elemen-elemen semantic seperti `header`, `nav`, `section`.

## CSS yang awal

```
nav {
    background: #C9BFBF;
    grid-area: nav;
}
header {
    background: #707070;
    grid-area: header;
    text-align: center;
}
section {
    background: #ABABAB;
    grid-area: section;
}
footer {
    background: #707070;
    grid-area: footer;
    font-size: small;
    text-align: center;
}
body {
    display: grid;
    grid-template-areas: 
    "header header header"
    "nav section section"
    "footer footer footer";
    grid-template-rows: 80px 1fr 50px;
    grid-template-columns: 20% 1fr 18%;
    grid-gap:5px;
    height: 100vh;
    margin: 10px;
}
header,nav,section,footer {
    padding: 5px;
}
```

## HTML yang telah diperbarui
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Semantic HTML</title>
    <link rel="stylesheet" href="assets/styles/styles.css">
</head>
<body>
    <header>
        <h1>HTML5 Semantic</h1>
    </header>
    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#pengertian">Pengertian</a></li>
            <li><a href="#kesimpulan">Kesimpulan</a></li>
        </ul>
    </nav>
    <section>
        <main>
            <article id="home">Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati aliquid mollitia velit hic deserunt impedit accusantium nemo vero ullam sed. Corrupti delectus earum possimus maxime esse. Perspiciatis debitis vitae eum!</article>
            <article id="pengertian">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Minima adipisci repellendus ducimus incidunt maxime! Quisquam, harum nemo dolorem doloremque officiis atque aliquid obcaecati?</article>
            <summary id="kesimpulan">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Eius perferendis nesciunt voluptatibus distinctio sapiente, cum, vel aspernatur consectetur maxime sint blanditiis rem similique dolores corrupti earum non soluta voluptate? Quas, libero? Asperiores officiis cupiditate commodi.</summary>
        </main>
    </section>
    <footer>
        Copyright
    </footer>
</body>
</html>
```
html diperbarui dengan melengkapi tag-tag semantic lainnya seperti main, article dan summary untuk memudahkan keterbacaan. Selain itu, juga ditambahkan atribut id pada tag-tag tersebut untuk memudahkan penandaan.

## CSS yang telah diperbarui
```
:root {
    --primary-color:#ABABAB;
    --secondary-color:#707070;
    --third-color:#C9BFBF;
    --nav-color:#b321a2;
}
html{
    scroll-behavior: smooth;
}

nav {
    background: var(--third-color);
    grid-area: nav;
}
header {
    background: var(--secondary-color);
    grid-area: header;
    text-align: center;
}
section {
    background: var(--primary-color);
    grid-area: section;
}
footer {
    background: var(--secondary-color);
    grid-area: footer;
    font-size: small;
    text-align: center;
}
body {
    display: grid;
    grid-template-areas: 
    "header header header"
    "nav section section"
    "footer footer footer";
    grid-template-rows: 80px 1fr 50px;
    grid-template-columns: 20% 1fr 18%;
    grid-gap:5px;
    height: 100vh;
    margin: 10px;
}
#home {
    grid-area: section;
    height: 80vh;
}
#pengertian {
    grid-area: section;
    height: 80vh;
}
#kesimpulan {
    grid-area: section;
    height: 100vh;
}
li,a {
    color: white;
    background: var(--nav-color);
    margin-bottom: 3px;
    padding: 3px 6px;
    list-style-type: none;
    text-decoration: none;
}
header,nav,section,footer {
    padding: 5px;
}
```
Css tersebut saya tambahkan :root untuk menginisiasi variabel CSS yang dapat digunakan di seluruh dokumen untuk menghindari redudansi pengetikan kode CSS. saya juga melengkapi di html scroll-behavior: smooth untuk membuat scroll menjadi lebih halus. saya juga menambahkan kode css untuk per id yang ditandai # berisi height 80vh dan 100vh untuk mengatur tinggi konten.