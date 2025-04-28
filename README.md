<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pengaruh Budaya Asing di Indonesia</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* CSS Reset dan Variabel */
        :root {
            --merah: #e63946;
            --putih: #f1faee;
            --biru-tua: #1d3557;
            --biru: #457b9d;
            --biru-muda: #a8dadc;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', 'Segoe UI', sans-serif;
            line-height: 1.7;
            color: #333;
            background-color: var(--putih);
            overflow-x: hidden;
        }
        
        /* Animasi */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        @keyframes slideInLeft {
            from { opacity: 0; transform: translateX(-50px); }
            to { opacity: 1; transform: translateX(0); }
        }
        
        @keyframes slideInRight {
            from { opacity: 0; transform: translateX(50px); }
            to { opacity: 1; transform: translateX(0); }
        }
        
        /* Header */
        header {
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1554260570-9140fd3b7614?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 2rem 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .header-content {
            max-width: 900px;
            margin: 0 auto;
            padding: 2rem;
            position: relative;
            z-index: 2;
        }
        
        .title-box {
            display: inline-block;
            padding: 1.5rem 2rem;
            border: 3px solid var(--merah);
            background-color: rgba(255, 255, 255, 0.9);
            color: var(--biru-tua);
            margin-bottom: 1.5rem;
            transform: rotate(-2deg);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
            animation: fadeIn 1s ease-out;
        }
        
        .title-box h1 {
            font-size: 2.2rem;
            margin: 0;
            transform: rotate(1deg);
        }
        
        .meta {
            color: var(--putih);
            font-style: italic;
            margin-bottom: 1rem;
            animation: fadeIn 1.5s ease-out;
        }
        
        /* Konten Utama */
        .container {
            max-width: 900px;
            margin: 2rem auto;
            padding: 0 2rem;
        }
        
        section {
            margin-bottom: 3rem;
            padding: 2rem;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.6s ease-out;
        }
        
        section.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        section:nth-child(odd) {
            border-left: 5px solid var(--merah);
        }
        
        section:nth-child(even) {
            border-right: 5px solid var(--biru);
        }
        
        h2 {
            color: var(--biru-tua);
            margin-bottom: 1.5rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px dashed var(--biru-muda);
            position: relative;
        }
        
        h2::after {
            content: "";
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 50px;
            height: 3px;
            background-color: var(--merah);
        }
        
        h3 {
            color: var(--biru);
            margin: 1.5rem 0 1rem;
            position: relative;
            display: inline-block;
        }
        
        h3::before {
            content: "";
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 30px;
            height: 2px;
            background-color: var(--merah);
        }
        
        p {
            margin-bottom: 1rem;
            text-align: justify;
        }
        
        .solution {
            background-color: rgba(168, 218, 220, 0.2);
            padding: 1.5rem;
            border-radius: 8px;
            margin: 1.5rem 0;
            position: relative;
            overflow: hidden;
            transition: transform 0.3s ease;
        }
        
        .solution:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
        }
        
        .solution::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background-color: var(--biru);
        }
        
        .solution-number {
            display: inline-block;
            width: 30px;
            height: 30px;
            background-color: var(--merah);
            color: white;
            border-radius: 50%;
            text-align: center;
            line-height: 30px;
            margin-right: 10px;
            font-weight: bold;
        }
        
        /* Referensi */
        .references {
            background-color: rgba(29, 53, 87, 0.05);
            padding: 1.5rem;
            border-radius: 8px;
            margin-top: 3rem;
        }
        
        .references h2 {
            color: var(--biru-tua);
            border-bottom: none;
        }
        
        .references h2::after {
            display: none;
        }
        
        .references ol {
            padding-left: 1.5rem;
        }
        
        .references li {
            margin-bottom: 0.5rem;
        }
        
        .references a {
            color: var(--biru);
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .references a:hover {
            color: var(--merah);
            text-decoration: underline;
        }
        
        /* Footer */
        footer {
            background-color: var(--biru-tua);
            color: white;
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
        }
        
        .social-share {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 1.5rem;
        }
        
        .social-share a {
            display: inline-block;
            width: 40px;
            height: 40px;
            background-color: white;
            color: var(--biru-tua);
            border-radius: 50%;
            text-align: center;
            line-height: 40px;
            transition: all 0.3s ease;
        }
        
        .social-share a:hover {
            transform: translateY(-3px);
            background-color: var(--merah);
            color: white;
        }
        
        .back-to-top {
            display: inline-block;
            padding: 0.5rem 1rem;
            background-color: var(--merah);
            color: white;
            border-radius: 5px;
            text-decoration: none;
            margin-top: 1rem;
            transition: all 0.3s ease;
        }
        
        .back-to-top:hover {
            background-color: var(--biru);
            transform: translateY(-3px);
        }
        
        /* Dekorasi Khas Indonesia */
        .batik-pattern {
            position: absolute;
            opacity: 0.1;
            z-index: 1;
        }
        
        .batik-1 {
            top: 20px;
            right: 20px;
            width: 150px;
            height: 150px;
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><path d="M20,20 Q30,10 40,20 T60,20 T80,20" stroke="%231d3557" fill="none" stroke-width="2"/><path d="M20,40 Q30,30 40,40 T60,40 T80,40" stroke="%231d3557" fill="none" stroke-width="2"/><path d="M20,60 Q30,50 40,60 T60,60 T80,60" stroke="%231d3557" fill="none" stroke-width="2"/><path d="M20,80 Q30,70 40,80 T60,80 T80,80" stroke="%231d3557" fill="none" stroke-width="2"/></svg>');
            background-repeat: no-repeat;
            animation: rotate 20s linear infinite;
        }
        
        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        
        /* Responsif */
        @media (max-width: 768px) {
            .title-box h1 {
                font-size: 1.8rem;
            }
            
            section {
                padding: 1.5rem;
            }
            
            .container {
                padding: 0 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="batik-pattern batik-1"></div>
        <div class="header-content">
            <div class="title-box">
                <h1>Pengaruh Negatif Budaya Asing terhadap Budaya Lokal Indonesia</h1>
            </div>
            <p class="meta">Artikel Budaya | 28 April 2025</p>
        </div>
    </header>
    
    <div class="container">
        <section id="pengantar">
            <p>Globalisasi membawa arus budaya asing yang masuk ke Indonesia dengan sangat cepat. Meskipun membawa manfaat seperti pembaruan pola pikir dan kemajuan teknologi, pengaruh budaya asing juga menimbulkan dampak negatif yang berpotensi mengikis nilai-nilai luhur dan identitas budaya Indonesia. Berikut beberapa pengaruh negatif tersebut dan solusi yang dapat dilakukan untuk mengatasinya.</p>
        </section>
        
        <section id="dampak-negatif">
            <h2>Dampak Negatif Budaya Asing</h2>
            
            <h3>Lunturnya nilai budaya lokal</h3>
            <p>Budaya asing yang masuk membuat sebagian masyarakat, terutama generasi muda, lebih mengadopsi gaya hidup dan kebiasaan luar negeri, sehingga tradisi seperti gotong royong dan sopan santun mulai terabaikan.</p>
            
            <h3>Menurunnya rasa nasionalisme</h3>
            <p>Ketergantungan pada produk dan budaya asing membuat masyarakat kurang bangga terhadap karya dan budaya dalam negeri, mengurangi rasa cinta tanah air.</p>
            
            <h3>Perubahan gaya hidup remaja yang negatif</h3>
            <p>Pengaruh budaya asing seperti gaya berpakaian terbuka, perilaku konsumtif, dan pergaulan bebas bertentangan dengan norma agama dan budaya lokal, berpotensi merusak moral generasi muda.</p>
            
            <h3>Konsumerisme dan materialisme berlebihan</h3>
            <p>Budaya asing yang menonjolkan status sosial melalui kepemilikan barang mewah bertentangan dengan nilai kesederhanaan Indonesia, menyebabkan tekanan sosial dan finansial.</p>
        </section>
        
        <section id="solusi">
            <h2>Solusi Mengatasi Pengaruh Negatif Budaya Asing</h2>
            
            <div class="solution">
                <h3><span class="solution-number">1</span> Industri Film Lebih Mencakup Ranah Internasional</h3>
                <p>Industri perfilman Indonesia perlu mengembangkan kualitas dan tema film yang tidak hanya menarik pasar lokal tetapi juga internasional. Dengan kualitas produksi yang baik dan cerita yang mengangkat nilai-nilai budaya Indonesia secara positif, film Indonesia dapat memperbaiki citra budaya bangsa di mata dunia dan mengurangi stereotip negatif.</p>
            </div>
            
            <div class="solution">
                <h3><span class="solution-number">2</span> Program TV Berkualitas dan Mengedukasi</h3>
                <p>Stasiun televisi harus kembali menghadirkan program-program yang mendidik dan mengangkat budaya lokal, seperti dokumenter, acara seni tradisional, dan program edukasi yang menarik bagi berbagai kalangan usia.</p>
            </div>
            
            <div class="solution">
                <h3><span class="solution-number">3</span> Platform Media Sosial Lokal</h3>
                <p>Indonesia sudah memiliki banyak media sosial karya anak bangsa seperti Sebangsa, Kwikku, RTRW, dan Hyppe yang menawarkan fitur seru dan komunitas berbasis budaya lokal. Pemerintah dan swasta perlu mendorong penggunaan platform ini sebagai alternatif pengganti media sosial asing.</p>
            </div>
            
            <div class="solution">
                <h3><span class="solution-number">4</span> Kebijakan Sensor yang Ketat</h3>
                <p>Pemerintah harus memperkuat regulasi dan pengawasan terhadap konten film agar tidak menampilkan adegan atau pesan yang bertentangan dengan norma budaya dan moral Indonesia.</p>
            </div>
            
            <div class="solution">
                <h3><span class="solution-number">5</span> Pemasaran melalui Influencer</h3>
                <p>Menggandeng influencer dan public figure yang memiliki pengaruh besar di media sosial untuk mempromosikan budaya dan produk lokal dapat meningkatkan daya tarik masyarakat, khususnya generasi muda, terhadap budaya Indonesia.</p>
            </div>
        </section>
        
        <section id="referensi" class="references">
            <h2>Referensi</h2>
            <ol>
                <li><a href="https://www.kompasiana.com/novanatasha/62b463e4790169377f4372b2/upaya-mengatasi-pengaruh-masuknya-budaya-asing-terhadap-mentalitas-masyarakat-indonesia" target="_blank">Kompasiana - Upaya Mengatasi Pengaruh Budaya Asing</a></li>
                <li><a href="https://www.kompas.com/skola/read/2023/07/29/090000369/cara-menghadapi-pengaruh-sosial-budaya-dari-luar" target="_blank">Kompas - Cara Menghadapi Pengaruh Sosial Budaya</a></li>
                <li><a href="https://bobo.grid.id/read/083709866/5-cara-untuk-menyeleksi-dan-menyaring-nilai-budaya-asing-yang-masuk-ke-indonesia?page=all" target="_blank">Bobo Grid - Menyaring Budaya Asing</a></li>
                <li><a href="https://kumparan.com/tips-dan-trik/5-cara-menangkal-dampak-negatif-globalisasi-dalam-bidang-budaya-20xw2C6idMW" target="_blank">Kumparan - Menangkal Dampak Negatif Globalisasi</a></li>
            </ol>
        </section>
    </div>
    
    <footer>
        <div class="social-share">
            <a href="#" title="Share ke Facebook"><i class="fab fa-facebook-f"></i></a>
            <a href="#" title="Share ke Twitter"><i class="fab fa-twitter"></i></a>
            <a href="#" title="Share ke WhatsApp"><i class="fab fa-whatsapp"></i></a>
            <a href="#" title="Share ke LinkedIn"><i class="fab fa-linkedin-in"></i></a>
        </div>
        <p>© 2025 Artikel Budaya Indonesia. Seluruh hak dilindungi.</p>
        <a href="#" class="back-to-top"><i class="fas fa-arrow-up"></i> Kembali ke Atas</a>
    </footer>
    
    <script>
        // JavaScript untuk animasi scroll
        document.addEventListener('DOMContentLoaded', function() {
            const sections = document.querySelectorAll('section');
            
            // Fungsi untuk mengecek apakah elemen terlihat di viewport
            function checkVisibility() {
                sections.forEach(section => {
                    const sectionTop = section.getBoundingClientRect().top;
                    const sectionBottom = section.getBoundingClientRect().bottom;
                    
                    // Jika 50% elemen terlihat di viewport
                    if (sectionTop < window.innerHeight * 0.75 && sectionBottom > window.innerHeight * 0.25) {
                        section.classList.add('visible');
                    }
                });
            }
            
            // Jalankan saat load dan scroll
            window.addEventListener('load', checkVisibility);
            window.addEventListener('scroll', checkVisibility);
            
            // Tombol kembali ke atas
            const backToTop = document.querySelector('.back-to-top');
            backToTop.addEventListener('click', function(e) {
                e.preventDefault();
                window.scrollTo({
                    top: 0,
                    behavior: 'smooth'
                });
            });
            
            // Tampilkan tombol ketika scroll ke bawah
            window.addEventListener('scroll', function() {
                if (window.pageYOffset > 300) {
                    backToTop.style.opacity = '1';
                    backToTop.style.visibility = 'visible';
                } else {
                    backToTop.style.opacity = '0';
                    backToTop.style.visibility = 'hidden';
                }
            });
            
            // Inisialisasi
            backToTop.style.opacity = '0';
            backToTop.style.visibility = 'hidden';
        });
        
        // Fungsi share media sosial
        function shareSocial(platform) {
            let url = '';
            const currentUrl = encodeURIComponent(window.location.href);
            const title = encodeURIComponent(document.title);
            
            switch(platform) {
                case 'facebook':
                    url = `https://www.facebook.com/sharer/sharer.php?u=${currentUrl}`;
                    break;
                case 'twitter':
                    url = `https://twitter.com/intent/tweet?url=${currentUrl}&text=${title}`;
                    break;
                case 'whatsapp':
                    url = `https://wa.me/?text=${title} ${currentUrl}`;
                    break;
                case 'linkedin':
                    url = `https://www.linkedin.com/shareArticle?mini=true&url=${currentUrl}&title=${title}`;
                    break;
            }
            
            window.open(url, '_blank', 'width=600,height=400');
        }
        
        // Tambahkan event listener untuk tombol share
        document.querySelectorAll('.social-share a').forEach((btn, index) => {
            const platforms = ['facebook', 'twitter', 'whatsapp', 'linkedin'];
            btn.addEventListener('click', (e) => {
                e.preventDefault();
                shareSocial(platforms[index]);
            });
        });
    </script>
</body>
</html>
