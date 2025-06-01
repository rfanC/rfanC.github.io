<html>
<head>
  <meta charset="UTF-8">
  <title>創作 Art Works – 曹睿凡 – Ruifan Cao</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" type="text/css" href="/style.css" />
  <style>
    .carousel { text-align: center; margin-top: 20px; }
    .carousel img { max-width: 300px; height: auto; border-radius: 5px; cursor: pointer; }
    nav { background-color: #f4f4f4; padding: 10px 0; text-align: center; }
    nav ul { list-style: none; padding: 0; }
    nav ul li { display: inline; margin: 0 15px; }
    nav ul li a { text-decoration: none; color: #333; }
  </style>
</head>
<body>
  <nav>
    <ul>
      <!-- <li><a href="/mywork/">works</a></li> -->
      <!-- <li><a href="/exhibitions/">exhibitions</a></li> -->
      <!-- <li><a href="/about/">about</a></li> -->
      <!-- <li><a href="/contact/">contact</a></li> -->
    </ul>
  </nav>
  <div class="carousel">
    <img id="carousel-image" src="/images/jpg/jpg-s/01sheepdog.jpg" alt="作品縮圖">
  </div>
  <script>
    const works = [
      { thumb: "/images/jpg/jpg-s/1-s.jpg", url: "/https://rfanc.github.io/01sheepdog.html", alt: "牧羊犬" },
      { thumb: "/images/jpg/jpg-s/2-s.jpg", url: "/https://rfanc.github.io/02Tip/", alt: "躍起" },
      { thumb: "/images/jpg/jpg-s/3-s.jpg", url: "/https://rfanc.github.io/03fish.html", alt: "魚都知道方向了" },
      { thumb: "/images/jpg/jpg-s/4-s.jpg", url: "/https://rfanc.github.io/04Locked.html", alt: "大象的鼻子反鎖了門" },
      { thumb: "/images/jpg/jpg-s/5-s.jpg", url: "/https://rfanc.github.io/05sedimentary.html", alt: "沈積岩" },
      { thumb: "/images/jpg/jpg-s/6-s.jpg", url: "/https://rfanc.github.io/06Blank.html", alt: "支起空白" },
      { thumb: "/images/jpg/jpg-s/7-s.jpg", url: "/https://rfanc.github.io/07Kite.html", alt: "風箏線" },
      { thumb: "/images/jpg/jpg-s/8-s.jpg", url: "/https://rfanc.github.io/08direction.html", alt: "到達的地方" },
      { thumb: "/images/jpg/jpg-s/9-s.jpg", url: "/https://rfanc.github.io/09Knight.html", alt: "騎士" },
      { thumb: "/images/jpg/jpg-s/10-s.jpg", url: "/https://rfanc.github.io/10Place.html", alt: "置" },
      { thumb: "/images/jpg/jpg-s/11-s.jpg", url: "/https://rfanc.github.io/11free.html", alt: "自由" }
    ];
    let currentIndex = 0;
const imageElement = document.getElementById("carousel-image");

function updateImage() {
  imageElement.src = works[currentIndex].thumb;
  imageElement.alt = works[currentIndex].alt;
}

imageElement.addEventListener("click", () => {
  window.open(works[currentIndex].url, "_blank");
  currentIndex = (currentIndex + 1) % works.length; // 在點擊後才遞增
  updateImage();
});

setInterval(() => {
  currentIndex = (currentIndex + 1) % works.length;
  updateImage();
}, 5000);

updateImage();
  </script>
</body>
</html>
