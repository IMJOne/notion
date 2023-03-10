![notion](https://user-images.githubusercontent.com/110226567/213738417-9f523b25-751f-4518-9c78-78b95bb1041d.png)

# ๐ Notion

Notion ๊ณต์ ์น์ฌ์ดํธ ํด๋ก  ์ฝ๋ฉ ๐ [Demo](https://imjone.github.io/notion/)

<br/>

## ๐ข ํ๋ก์ ํธ ๊ฐ์

์ฒซ ์น ํ๋ก์ ํธ๋ก ์งํํ Notion ํด๋ก  ์ฝ๋ฉ ์ฌ์ดํธ์๋๋ค.<br />
์ ์ ์ต์  ์ดํ ์ค ํ๋๋ผ์ ๊ด๋ จ๋ ํ๋ก์ ํธ๋ฅผ ํ๋์ฏค ์งํํด๋ณด๊ณ  ์ถ์์ต๋๋ค.<br />
๋ชจ๋ฐ์ผ ๋ฐ ํ๋ธ๋ฆฟ, PC ํ๊ฒฝ์์ ๋ชจ๋ ๋ณด๊ธฐ ํธํ๋๋ก ๋ฐ์ํ์ผ๋ก ์ ์ํ์์ต๋๋ค.

<br/>

## ๐จ๏ธ ์ฌ์ฉ ๊ธฐ์ 

<p>
  <img src="https://img.shields.io/badge/HTML-e34f26?style=flat-square&logo=HTML5&logoColor=white" />
  <img src="https://img.shields.io/badge/CSS-1572b6?style=flat-square&logo=CSS3&logoColor=white" />
  <img src="https://img.shields.io/badge/JavaScript-f7df1e?style=flat-square&logo=JavaScript&logoColor=white" />
</p>

<br/>

## ๐ ์ฃผ์ ๊ธฐ๋ฅ

- ๋ชจ๋ฐ์ผ ํ๊ฒฝ์ ๊ณ ๋ คํ ๋ฐ์ํ ์์
- ์คํฌ๋กค๊ฐ์ ๋ฐ๋ฅธ ์น์ ๋ฑ์ฅ ์ ๋๋ฉ์ด์
- ํด๋ฆญ ์ ํ์ด์ง ์ต์๋จ์ผ๋ก ์ด๋ํ๋ ๋ฒํผ
- ์นดํ๊ณ ๋ฆฌ๋ณ ์ํ ์ด๋ฏธ์ง ํํฐ๋ง ๊ธฐ๋ฅ
- ์ค์์ดํผ ๋ผ์ด๋ธ๋ฌ๋ฆฌ๋ฅผ ํ์ฉํ ์ฌ๋ผ์ด๋

<br/>

## ๐ป ์์ค ์ฝ๋

์ ์ฒด ์ฝ๋ ๋ณด๋ฌ ๊ฐ๊ธฐ ๐ [Notion](https://imjone.notion.site/Notion-7260e6b7c68e467995630c2e52b664d5)

### ๐ ์คํฌ๋กค ํค๋ & ๋ฉ๋ด๋ฐ

ํ์ด์ง ์ฒซ ์คํฌ๋กค ์, ํค๋์ ๋ฉ๋ด๋ฐ์ ์คํ์ผ์ด ๋์ ์ผ๋ก ๋ณ๊ฒฝ๋ฉ๋๋ค. (box-shadow, height)<br>
`scroll` ์ด๋ฒคํธ๋ฅผ ๋ฑ๋กํ์ฌ ์คํฌ๋กค๊ฐ์ด header์ ๋์ด๊ฐ๋ณด๋ค ํด ๊ฒฝ์ฐ CSS ํด๋์ค๋ฅผ ๋ถ์ฌํ๊ณ ,<br>
๊ทธ๋ ์ง ์์ ๊ฒฝ์ฐ ํด๋์ค๋ฅผ ๋ค์ ์ ๊ฑฐํ๋ ์์ผ๋ก ๊ตฌํํ์์ต๋๋ค.

```javascript
const header = document.querySelector('header');
const headerHeight = header.offsetHeight;
const navbarMenu = document.querySelector('.navbar_menu');

document.addEventListener('scroll', () => {
  if (window.scrollY > headerHeight) {
    header.classList.add('scrollHeader');
    if (window.innerWidth <= 768) {
      navbar.classList.add('scrollNav');
    }
  } else {
    header.classList.remove('scrollHeader');
    if (window.innerWidth <= 768) {
      navbar.classList.remove('scrollNav');
    }
  }
});
```

### ๐ ํ ์น์ ํฌ๋ช๋ ์กฐ์ 

์คํฌ๋กค ๋น์จ์ ๋ฐ๋ผ ํฌ๋ช๋๊ฐ ์ ์ ํ๊ฒ ํ ๋น๋๋๋ก ํ๊ธฐ ์ํด์,<br />
ํ์ฌ ์คํฌ๋กค๊ฐ(`window.scrollY`)์ home ์น์์ ๋์ด๊ฐ์ผ๋ก ๋๋ ํ 1์์ ๋นผ์ฃผ์์ต๋๋ค.<br />
์ฐ์ฐ ๊ฒฐ๊ณผ์ ๋ฐ๋ผ opacity ์์ฑ์ ๊ฐ์ด ๋์ ์ผ๋ก ํ ๋น๋ฉ๋๋ค.

```javascript
const homeInner = document.querySelector('#home .inner');
const homeHeight = home.offsetHeight;

document.addEventListener('scroll', () => {
  homeInner.style.opacity = 1 - window.scrollY / homeHeight;
  // opacity (0 : transparent, 1 : untransparent)
});
```

### ๐ ์ด๋ฏธ์ง ํํฐ๋ง

์นดํ๊ณ ๋ฆฌ๋ณ๋ก ์ ์ ํ ์ํ ์ด๋ฏธ์ง๋ฅผ ๋ณด์ฌ์ฃผ๋ ๋ทฐ์ด ๊ธฐ๋ฅ์ ๊ตฌํํ์์ต๋๋ค.<br />
๋จผ์  ๊ฐ๊ฐ์ ์นดํ๊ณ ๋ฆฌ๋ง๋ค index ์ญํ ์ ํ๋ `data-order` ์์ฑ์ ์ ์ํฉ๋๋ค.<br />
๊ฐ ์์ ํด๋ฆญ ์, ํด๋น ์์ฑ์ ๊ฐ๊ณผ ๋์ผํ ํ์ผ๋ช์ ๊ฐ์ง ์ด๋ฏธ์ง๊ฐ ๋ณด์ฌ์ง๊ฒ ๋ฉ๋๋ค.

```html
<!-- Category -->
<ul class="uses_album_categories">
  <li data-order="1">โ๏ธ ๋ฉ๋ชจ</li>
  <li data-order="2">๐ ์์</li>
  <li data-order="3">๐ ๋ณด๊ณ ์</li>
  <li data-order="4">๐จ ๋์์ธ</li>
  <li data-order="5">๐ ๋ฉ๋ด์ผ</li>
</ul>

<!-- Image -->
<div class="uses_album_photo">
  <img src="img/uses/uses_photo1.webp" alt="template image" />
</div>
```

```javascript
const albumCategory = document.querySelector('.uses_album_categories');
const albumPhoto = document.querySelector('.uses_album_photo img');

albumCategory.addEventListener('click', e => {
  const target = e.target.nodeName === 'LI' ? e.target : e.target.parentNode;
  const order = target.dataset.order;
  if (target.nodeName === 'LI') albumPhoto.setAttribute('src', `img/uses/uses_photo${order}.webp`);
  else return;
});
```

<br/>

## ๐ ๋ฐฐ์ด ์  ๋ฐ ๋๋ ์ 

- ์ ๋๋ฉ์ด์ ๋ผ์ด๋ธ๋ฌ๋ฆฌ์ ๋งค๋ ฅ๊ณผ ํธ๋ฆฌํจ์ ์๊ฒ ๋์์ต๋๋ค.
- ๋ชจ๋ฐ์ผ ์๋์ธ ๋งํผ ์ด๊ธฐ ๋ฐ์ํ ์คํ์ผ ๊ธฐํ์ด ์ ๋ง ์ค์ํ๋ค๊ณ  ๋๊ผ์ต๋๋ค.
- ์๋ฐ์คํฌ๋ฆฝํธ์ ์กฐ๊ธ ๋ ์นํด์ง ์ ์๋ ์ข์ ๊ณ๊ธฐ๊ฐ ๋์์ต๋๋ค.
