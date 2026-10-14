
# LOGPRO-Kelas-A
Tugas halaman perkenalan diri menggunakan HTML.
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Jeqiw Site | About Me</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        :root {
            --navy: #102746;
            --blue: #2878d0;
            --light-blue: #eaf3ff;
            --white: #ffffff;
            --text: #26374b;
            --muted: #6c7d91;
        }

        body {
            font-family: Arial, sans-serif;
            background: #f3f7fc;
            color: var(--text);
            line-height: 1.7;
        }

        /* NAVBAR */
        nav {
            background: var(--navy);
            color: white;
            padding: 17px 7%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 15px;
        }

        .logo {
            font-size: 23px;
            font-weight: bold;
            letter-spacing: 1px;
        }

        .logo span {
            color: #66b6ff;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin-left: 18px;
            font-size: 13px;
            transition: color 0.3s;
        }

        nav a:hover {
            color: #66b6ff;
        }

        /* HERO */
        .hero {
            background: linear-gradient(135deg, #102746, #245d96);
            color: white;
            padding: 75px 7%;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 45px;
            flex-wrap: wrap;
        }

        .profile-img {
            width: 210px;
            height: 210px;
            object-fit: cover;
            border-radius: 50%;
            border: 5px solid #ffffff;
            box-shadow: 0 0 30px rgba(102, 182, 255, 0.3);
        }

        .hero-content {
            max-width: 610px;
        }

        .badge {
            display: inline-block;
            background: rgba(255, 255, 255, 0.12);
            border: 1px solid rgba(255, 255, 255, 0.25);
            padding: 5px 14px;
            border-radius: 30px;
            font-size: 12px;
            margin-bottom: 15px;
        }

        .hero h1 {
            font-size: clamp(30px, 5vw, 46px);
            line-height: 1.2;
            margin-bottom: 12px;
        }

        .hero h1 span {
            color: #79c4ff;
        }

        .hero p {
            color: #dceaff;
            margin-bottom: 18px;
        }

        .hero-buttons {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-block;
            padding: 11px 20px;
            border-radius: 9px;
            text-decoration: none;
            font-weight: bold;
            font-size: 13px;
            transition: 0.3s;
        }

        .btn-primary {
            background: #ffffff;
            color: var(--navy);
        }

        .btn-outline {
            border: 1px solid white;
            color: white;
        }

        .btn:hover {
            transform: translateY(-3px);
            opacity: 0.88;
        }

        /* GENERAL SECTION */
        .container {
            max-width: 1120px;
            margin: auto;
            padding: 45px 22px;
        }

        .section-title {
            font-size: 26px;
            color: var(--navy);
            margin-bottom: 8px;
        }

        .section-desc {
            color: var(--muted);
            margin-bottom: 25px;
            font-size: 14px;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(2, minmax(0, 1fr));
            gap: 22px;
        }

        .card {
            background: white;
            padding: 25px;
            border: 1px solid #e0eafa;
            border-radius: 17px;
            box-shadow: 0 6px 20px rgba(16, 39, 70, 0.045);
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .card:hover {
            transform: translateY(-4px);
            box-shadow: 0 12px 28px rgba(16, 39, 70, 0.09);
        }

        .card h3 {
            color: var(--navy);
            font-size: 19px;
            margin-bottom: 12px;
        }

        .card p {
            font-size: 14px;
        }

        .icon {
            font-size: 27px;
            margin-bottom: 8px;
        }

        .highlight {
            color: var(--blue);
            font-weight: bold;
        }

        /* ABOUT */
        .about-info {
            display: grid;
            grid-template-columns: repeat(2, minmax(0, 1fr));
            gap: 12px;
            margin-top: 18px;
        }

        .info-box {
            background: var(--light-blue);
            border-radius: 10px;
            padding: 12px;
            font-size: 13px;
        }

        /* HOBBIES */
        .hobby-grid {
            display: grid;
            grid-template-columns: repeat(4, minmax(0, 1fr));
            gap: 12px;
            margin-top: 15px;
        }

        .hobby {
            text-align: center;
            padding: 18px 8px;
            background: #f3f7fc;
            border-radius: 12px;
        }

        .hobby p {
            font-weight: bold;
            margin-top: 5px;
            font-size: 13px;
        }

        .hobby small {
            display: block;
            color: var(--muted);
            font-size: 11px;
            margin-top: 4px;
        }

        /* FAVORITES */
        .favorite-list {
            list-style: none;
        }

        .favorite-list li {
            padding: 10px 0;
            border-bottom: 1px solid #edf1f7;
            font-size: 14px;
        }

        .favorite-list li:last-child {
            border-bottom: none;
        }

        .favorite-list li span {
            color: var(--muted);
        }

        /* SKILLS */
        .skill {
            margin-top: 17px;
        }

        .skill-label {
            display: flex;
            justify-content: space-between;
            font-size: 13px;
            margin-bottom: 6px;
        }

        .skill-bar {
            height: 8px;
            background: #e7edf5;
            border-radius: 20px;
            overflow: hidden;
        }

        .skill-progress {
            height: 100%;
            background: linear-gradient(90deg, #2878d0, #65bcff);
            border-radius: 20px;
        }

        /* QUOTE */
        .quote {
            background: var(--light-blue);
            border-left: 4px solid var(--blue);
            padding: 18px;
            border-radius: 8px;
            color: var(--navy);
            font-style: italic;
        }

        /* CONTACT */
        .contact-links {
            display: flex;
            flex-direction: column;
            gap: 12px;
            margin-top: 15px;
        }

        .contact-links a {
            color: var(--blue);
            text-decoration: none;
            font-size: 14px;
            overflow-wrap: anywhere;
        }

        .contact-links a:hover {
            text-decoration: underline;
        }

        /* CAMPUS BANNER */
        .campus {
            background: var(--navy);
            color: white;
            border-radius: 16px;
            padding: 30px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 20px;
            flex-wrap: wrap;
        }

        .campus h3 {
            margin-bottom: 5px;
        }

        .campus p {
            color: #dceaff;
            font-size: 13px;
        }

        .campus .btn {
            background: white;
            color: var(--navy);
        }

        /* FOOTER */
        footer {
            background: #0b1c32;
            color: #c5d3e6;
            text-align: center;
            padding: 25px 15px;
            font-size: 12px;
        }

        footer strong {
            color: white;
        }

        /* RESPONSIVE */
        @media (max-width: 700px) {
            nav {
                justify-content: center;
                text-align: center;
            }

            nav a {
                margin: 5px 7px;
            }

            .hero {
                text-align: center;
                padding: 50px 22px;
                gap: 25px;
            }

            .hero-buttons {
                justify-content: center;
            }

            .grid {
                grid-template-columns: 1fr;
            }

            .hobby-grid {
                grid-template-columns: repeat(2, minmax(0, 1fr));
            }

            .about-info {
                grid-template-columns: 1fr;
            }

            .campus {
                text-align: center;
                justify-content: center;
            }
        }
    </style>
</head>

<body>

    <!-- NAVIGATION -->
    <nav>
        <div class="logo">MJ<span>.</span> Jeqiw Site</div>

        <div>
            <a href="#beranda">Beranda</a>
            <a href="#tentang">Tentang</a>
            <a href="#hobi">Hobi</a>
            <a href="#favorit">Favorit</a>
            <a href="#kontak">Kontak</a>
        </div>
    </nav>

    <!-- HERO / PERKENALAN -->
    <header class="hero" id="beranda">

        <img src="foto.jpg"
             alt="Foto Muhammad Jerricho"
             class="profile-img">

        <div class="hero-content">
            <span class="badge">WELCOME TO MY PERSONAL WEBSITE</span>

            <h1>Halo, Saya <span>Muhammad Jerricho</span></h1>

            <p>
                Mahasiswa Program Studi [Nama Program Studi]
                <br>
                📍 Bandung, Indonesia
            </p>

            <p>
                Saya adalah seseorang yang senang belajar,
                mencoba hal baru, dan mengembangkan diri.
                Website ini adalah tempat untuk mengenal saya
                lebih dekat, mulai dari pendidikan, hobi,
                hingga hal-hal favorit saya.
            </p>

            <div class="hero-buttons">
                <a href="#tentang" class="btn btn-primary">
                    Kenali Saya →
                </a>

                <a href="#favorit" class="btn btn-outline">
                    Hal Favorit Saya
                </a>
            </div>
        </div>

    </header>

    <main>

        <!-- TENTANG SAYA -->
        <section class="container" id="tentang">

            <h2 class="section-title">👋 Tentang Saya</h2>

            <p class="section-desc">
                Sedikit cerita tentang siapa saya dan apa yang saya pelajari.
            </p>

            <div class="grid">

                <article class="card">
                    <div class="icon">🙋‍♂️</div>
                    <h3>Siapa Saya?</h3>

                    <p>
                        Perkenalkan, nama saya
                        <span class="highlight">Muhammad Jerricho</span>.
                        Saya berasal dari Bandung dan saat ini sedang
                        menempuh pendidikan sebagai mahasiswa.
                        Saya ingin terus berkembang, menambah pengalaman,
                        dan menjadi pribadi yang lebih baik.
                    </p>
                </article>

                <article class="card">
                    <div class="icon">🎓</div>
                    <h3>Pendidikan</h3>

                    <p>
                        <strong>Program Studi:</strong>
                        [Nama Program Studi]
                    </p>

                    <p>
                        <strong>Universitas:</strong>
                        [Nama Universitas]
                    </p>

                    <p>
                        <strong>Minat:</strong>
                        Teknologi, website, dan pengembangan diri.
                    </p>
                </article>

            </div>

        </section>

        <!-- HOBI -->
        <section class="container" id="hobi">

            <h2 class="section-title">⚡ Hobi & Aktivitas</h2>

            <p class="section-desc">
                Hal-hal yang saya sukai untuk mengisi waktu luang.
            </p>

            <div class="card">
                <div class="hobby-grid">

                    <div class="hobby">
                        <div class="icon">📚</div>
                        <p>Membaca</p>
                        <small>Menambah wawasan</small>
                    </div>

                    <div class="hobby">
                        <div class="icon">⚽</div>
                        <p>Sepak Bola</p>
                        <small>Olahraga favorit</small>
                    </div>

                    <div class="hobby">
                        <div class="icon">🎮</div>
                        <p>Gaming</p>
                        <small>Hiburan di waktu luang</small>
                    </div>

                    <div class="hobby">
                        <div class="icon">💻</div>
                        <p>Teknologi</p>
                        <small>Belajar hal baru</small>
                    </div>

                </div>
            </div>

        </section>

        <!-- FAVORIT -->
        <section class="container" id="favorit">

            <h2 class="section-title">⭐ Hal Favorit Saya</h2>

            <p class="section-desc">
                Beberapa hal yang bisa menggambarkan selera dan kepribadian saya.
            </p>

            <div class="grid">

                <article class="card">
                    <div class="icon">⚽</div>
                    <h3>Tim Sepak Bola Favorit</h3>

                    <ul class="favorite-list">
                        <li>🏆 Tim favorit: <strong>[Nama Tim]</strong></li>
                        <li>🌍 Liga favorit: <strong>[Nama Liga]</strong></li>
                        <li>👕 Pemain favorit: <strong>[Nama Pemain]</strong></li>
                        <li>🇮🇩 Tim nasional: <strong>[Tim Nasional]</strong></li>
                    </ul>
                </article>

                <article class="card">
                    <div class="icon">🍜</div>
                    <h3>Makanan & Minuman</h3>

                    <ul class="favorite-list">
                        <li>🍛 Makanan favorit: <strong>[Makanan]</strong></li>
                        <li>🥤 Minuman favorit: <strong>[Minuman]</strong></li>
                        <li>🍰 Camilan favorit: <strong>[Camilan]</strong></li>
                        <li>🌶️ Level pedas: <strong>[Level Pedas]</strong></li>
                    </ul>
                </article>

                <article class="card">
                    <div class="icon">🎬</div>
                    <h3>Film & Hiburan</h3>

                    <ul class="favorite-list">
                        <li>🎥 Film favorit: <strong>[Judul Film]</strong></li>
                        <li>📺 Serial favorit: <strong>[Judul Serial]</strong></li>
                        <li>🎵 Genre musik: <strong>[Genre Musik]</strong></li>
                        <li>🎤 Artis favorit: <strong>[Nama Artis]</strong></li>
                    </ul>
                </article>

                <article class="card">
                    <div class="icon">🌎</div>
                    <h3>Preferensi Pribadi</h3>

                    <ul class="favorite-list">
                        <li>🎨 Warna favorit: <strong>[Warna]</strong></li>
                        <li>🌤️ Suasana favorit: <strong>[Suasana]</strong></li>
                        <li>✈️ Destinasi impian: <strong>[Tempat]</strong></li>
                        <li>💭 Hal yang memotivasi: <strong>[Motivasi]</strong></li>
                    </ul>
                </article>

            </div>

        </section>

        <!-- SKILL -->
        <section class="container" id="skill">

            <h2 class="section-title">💻 Keahlian & Minat</h2>

            <p class="section-desc">
                Perjalanan saya dalam mengenal dunia teknologi.
            </p>

            <div class="grid">

                <article class="card">
                    <h3>Yang Sedang Saya Pelajari</h3>

                    <div class="skill">
                        <div class="skill-label">
                            <span>HTML</span>
                            <span>Pemula</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress"
                                 style="width: 35%"></div>
                        </div>
                    </div>

                    <div class="skill">
                        <div class="skill-label">
                            <span>CSS</span>
                            <span>Pemula</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress"
                                 style="width: 25%"></div>
                        </div>
                    </div>

                    <div class="skill">
                        <div class="skill-label">
                            <span>Git & GitHub</span>
                            <span>Pemula</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress"
                                 style="width: 20%"></div>
                        </div>
                    </div>

                    <p style="margin-top: 15px; color: #6c7d91;">
                        Kemampuan akan terus berkembang seiring
                        proses belajar dan latihan.
                    </p>
                </article>

                <article class="card">
                    <div class="icon">🚀</div>
                    <h3>Target Saya</h3>

                    <p>
                        Saya ingin ngopi dengan teman teman saya
                    </p>

                    <br>

                    <p>
                        <strong>Prinsip saya:</strong>
                        mulai dari hal kecil, belajar secara konsisten,
                        dan jangan takut mencoba.
                    </p>
                </article>

            </div>

        </section>

        <!-- QUOTE -->
        <section class="container">

            <div class="card">
                <h2 class="section-title">💭 Kata-Kata Favorit</h2>

                <blockquote class="quote">
                    "Jangan takut untuk memulai.
                    Setiap langkah kecil adalah bagian
                    dari perjalanan besar."
                </blockquote>

                <p style="margin-top: 12px; text-align: right;">
                    — Prinsip hidup saya
                </p>
            </div>

        </section>

        <!-- KONTAK -->
        <section class="container" id="kontak">

            <h2 class="section-title">📬 Hubungi Saya</h2>

            <p class="section-desc">
                Temukan saya melalui platform berikut.
            </p>

            <div class="card">

                <p>
                    Terima kasih sudah berkunjung ke website saya!
                    Senang bisa berbagi sedikit cerita tentang diri saya.
                </p>

                <div class="contact-links">
                    <a href="https://www.instagram.com/"
                       target="_blank"
                       rel="noopener noreferrer">
                        📸 Instagram — [Username Instagram]
                    </a>

                    <a href="https://github.com/"
                       target="_blank"
                       rel="noopener noreferrer">
                        💻 GitHub — [Username GitHub]
                    </a>

                    <a href="mailto:emailkamu@example.com">
                        ✉️ Email — [Alamat Email]
                    </a>
                </div>

            </div>

        </section>

        <!-- KAMPUS -->
        <section class="container">
            <div class="campus">

                <div>
                    <h3>🎓 Kenali Kampus Saya</h3>
                    <p>
                        Kunjungi website resmi kampus untuk
                        mengetahui informasi pendidikan.
                    </p>
                </div>

                <a href="https://www.upi.edu"
                   target="_blank"
                   rel="noopener noreferrer"
                   class="btn">
                    Website UPI →
                </a>

            </div>
        </section>

    </main>

    <!-- FOOTER -->
    <footer>
        <p>
            &copy; 2026 <strong>Jeqiw Site</strong>
            | Dibuat oleh Muhammad Jerricho
        </p>

        <p>Terus belajar, terus berkembang. 🚀</p>

        <p style="margin-top: 10px;">
            <a href="#beranda"
               style="color: #79c4ff; text-decoration: none;">
                ↑ Kembali ke atas
            </a>
        </p>
    </footer>

</body>

