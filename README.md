<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Benim Profesyonel Portföyüm</title>
<meta name="description" content="Kişisel portföyüm, projelerim ve iletişim bilgilerim.">
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
<script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
<style>
/* Genel Stil */
body { margin:0; font-family:'Roboto',sans-serif; scroll-behavior:smooth; background-color:#f5f5f5; }
header { background-color:#4CAF50; color:white; padding:20px; text-align:center; position:sticky; top:0; z-index:1000; transition: all 0.3s ease; }
header.scrolled { background-color:#333; box-shadow:0 4px 10px rgba(0,0,0,0.3); }
header nav a { color:white; text-decoration:none; margin:0 10px; font-weight:bold; }
header nav a:hover { text-decoration:underline; }
section { padding:60px 20px; opacity:0; transform:translateY(20px); transition: all 0.6s ease; }
section.visible { opacity:1; transform:translateY(0); }
h2 { margin-bottom:20px; color:#333; text-align:center; }
section#hakkimda { background-color:#e0f7fa; text-align:center; }
section#projelerim { background: linear-gradient(120deg, #fff3e0, #ffe0b2); }
section#iletisim { background: linear-gradient(120deg, #f3e5f5, #e1bee7); text-align:center; }
.parallax { background-attachment: fixed; background-size: cover; background-position: center; min-height:400px; display:flex; justify-content:center; align-items:center; color:white; font-size:2em; }
.card-container { display:flex; justify-content:center; gap:20px; flex-wrap:wrap; }
.card { border:1px solid #ccc; background-color:white; padding:10px; width:200px; transition: transform 0.3s, box-shadow 0.3s; }
.card:hover { transform: translateY(-15px) scale(1.05); box-shadow:0 15px 25px rgba(0,0,0,0.3); }
.card img { width:100%; }
button { background-color:#4CAF50; color:white; border:none; padding:10px 15px; cursor:pointer; border-radius:5px; }
button:hover { background-color:#45a049; }
form input, form textarea { width:80%; padding:10px; margin:5px 0; border-radius:5px; border:1px solid #ccc; }
form button { margin-top:10px; }
footer { background-color:#333; color:white; text-align:center; padding:10px; }
@media screen and (max-width:768px){
    header, nav{text-align:center; display:block;}
    .card-container{flex-direction:column; align-items:center;}
    form input, form textarea{width:90%;}
}
</style>
</head>
<body>

<header>
    <h1>Benim Profesyonel Portföyüm</h1>
    <nav>
        <a href="#hakkimda">Hakkımda</a> |
        <a href="#projelerim">Projelerim</a> |
        <a href="#iletisim">İletişim</a>
    </nav>
</header>

<section id="hakkimda">
    <h2>Hakkımda</h2>
    <p>Merhaba! Benim adım [İsminiz]. Web geliştirme ve tasarım konularında projeler yapıyorum. Bu portföy sayfasında çalışmalarımı ve iletişim bilgilerimi bulabilirsiniz.</p>
</section>

<section class="parallax" style="background-image:url('https://via.placeholder.com/1200x600');">
    Benim Özel Bölümüm
</section>

<section id="projelerim">
    <h2>Projelerim</h2>
    <div class="card-container">
        <div class="card">
            <img src="https://via.placeholder.com/200" alt="Proje 1" loading="lazy">
            <h3>Proje 1</h3>
            <p>Kısa açıklama buraya gelecek.</p>
            <button onclick="alert('Proje 1 tıklandı!')">Detay</button>
        </div>
        <div class="card">
            <img src="https://via.placeholder.com/200" alt="Proje 2" loading="lazy">
            <h3>Proje 2</h3>
            <p>Kısa açıklama buraya gelecek.</p>
            <button onclick="alert('Proje 2 tıklandı!')">Detay</button>
        </div>
    </div>
</section>

<section id="iletisim">
    <h2>İletişim</h2>
    <p>Email: benimmail@example.com</p>
    <form action="mailto:benimmail@example.com" method="post" enctype="text/plain">
        <input type="text" name="name" placeholder="Adınız" required><br>
        <input type="email" name="email" placeholder="Email" required><br>
        <textarea name="message" placeholder="Mesajınız" required></textarea><br>
        <button type="submit">Gönder</button>
    </form>
    <div style="margin-top:20px;">
        <a href="https://www.facebook.com" target="_blank"><i class="fab fa-facebook fa-2x"></i></a>
        <a href="https://www.twitter.com" target="_blank"><i class="fab fa-twitter fa-2x"></i></a>
        <a href="https://www.instagram.com" target="_blank"><i class="fab fa-instagram fa-2x"></i></a>
    </div>
</section>

<footer>
    &copy; 2025 Benim Profesyonel Portföyüm
</footer>

<script>
// Scroll animasyonu
window.addEventListener('scroll', function() {
    document.querySelectorAll('section').forEach(section => {
        const rect = section.getBoundingClientRect();
        if(rect.top < window.innerHeight - 100) section.classList.add('visible');
    });
});
// Menü scroll efekti
window.addEventListener('scroll', function(){
    const header = document.querySelector('header');
    if(window.scrollY > 50) header.classList.add('scrolled');
    else header.classList.remove('scrolled');
});
</script>

</body>
</html>
