<div align="center">

  <h1>PIXVIA AI STUDIO</h1>
  <p><strong>Enterprise-Grade Generative AI Image & Video Platform</strong></p>

  <p>
    <a href="#fitur-utama"><img src="https://img.shields.io/badge/Versi-v1.0.0.0-0ea5e9?style=for-the-badge&logo=git" alt="Versi v1.0.0.0" /></a>
    <a href="#persyaratan-sistem"><img src="https://img.shields.io/badge/PHP-8.1%2B-777bb4?style=for-the-badge&logo=php&logoColor=white" alt="PHP 8.1+" /></a>
    <a href="#penyimpanan-multi-cloud"><img src="https://img.shields.io/badge/Storage-Cloudflare%20R2%20%2B%20SSD-f38020?style=for-the-badge&logo=cloudflare&logoColor=white" alt="Cloudflare R2" /></a>
    <a href="#gateway-pembayaran"><img src="https://img.shields.io/badge/Payment-Duitku%20%26%20Manual-10b981?style=for-the-badge" alt="Payment Gateway" /></a>
    <a href="#arsitektur"><img src="https://img.shields.io/badge/Style-shadcn%20Dark%20Zinc-27272a?style=for-the-badge" alt="Design Standard" /></a>
  </p>

  <p>
    Platform studio kreatif generasi gambar, video, dan manipulasi visual berbasis AI modern.<br />
    Dibangun dengan arsitektur <strong>Native PHP MVC murni</strong>, <strong>Tailwind CSS</strong>, dan <strong>Vanilla JavaScript</strong>.<br />
    Ringan, berkecepatan tinggi, tanpa dependensi Node.js di server, dan siap dipasang langsung pada <strong>Laragon Local</strong> maupun <strong>cPanel Shared Hosting</strong>.
  </p>

  <p>
    <a href="#fitur-utama">Fitur Utama</a> •
    <a href="#arsitektur-multi-layer">Arsitektur AI & Storage</a> •
    <a href="#panduan-instalasi">Panduan Instalasi</a> •
    <a href="#kredensial-demo">Kredensial Demo</a> •
    <a href="#skema-database">Database</a>
  </p>

</div>

<hr />

<h2>Daftar Isi</h2>

<ul>
  <li><a href="#ringkasan-sistem">Ringkasan Sistem</a></li>
  <li><a href="#fitur-utama">Fitur Utama</a></li>
  <li><a href="#arsitektur-multi-layer">Arsitektur Multi-Layer & Failover</a></li>
  <li><a href="#penyimpanan-cloud-skala-besar">Penyimpanan Cloud Skala Besar (Multi-Bucket R2)</a></li>
  <li><a href="#sistem-monetisasi--kredit">Sistem Monetisasi & Pengaturan Kredit</a></li>
  <li><a href="#panduan-instalasi">Panduan Instalasi (Laragon & cPanel)</a></li>
  <li><a href="#kredensial-demo">Kredensial Akun & Lisensi Demo</a></li>
  <li><a href="#struktur-direktori">Struktur Direktori</a></li>
  <li><a href="#kebijakan-desain">Kebijakan Desain & Standar Teknis</a></li>
</ul>

<hr />

<h2 id="ringkasan-sistem">Ringkasan Sistem</h2>

<p>
  <strong>Pixvia AI</strong> mengadaptasi seluruh keunggulan platform generasi visual ke dalam format SaaS mandiri yang terstruktur. Platform ini dilengkapi dengan sistem failover otomatis lintas multi-provider, kluster penyimpanan terdistribusi Cloudflare R2 tanpa biaya egress bandwidth, dynamic watermark branding untuk pengguna freemium, serta panel administrasi komprehensif.
</p>

<table>
  <thead>
    <tr>
      <th width="30%">Komponen</th>
      <th width="70%">Spesifikasi Teknis</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Backend Framework</strong></td>
      <td>Native PHP MVC Murni (Routing, Controller, Service Layer, Middleware, CSRF Shield, Rate Limiting)</td>
    </tr>
    <tr>
      <td><strong>Frontend UI / UX</strong></td>
      <td>Tailwind CSS & Vanilla JavaScript murni berstandar <em>shadcn/ui Dark Zinc</em> dengan dukungan Light/Dark mode</td>
    </tr>
    <tr>
      <td><strong>Database</strong></td>
      <td>Hybrid Database Engine (SQLite otomatis tanpa setup, serta dukungan penuh MySQL / MariaDB)</td>
    </tr>
    <tr>
      <td><strong>AI Router Engine</strong></td>
      <td>Multi-Provider Router (9Router Pool, Hugging Face FLUX.1, Pollinations AI, External Worker Node)</td>
    </tr>
    <tr>
      <td><strong>Penyimpanan Cloud</strong></td>
      <td>Multi-Bucket Cloudflare R2 Native Signature V4 dengan rotasi otomatis dan failover ke Local SSD</td>
    </tr>
    <tr>
      <td><strong>Gateway Pembayaran</strong></td>
      <td>Integrasi Duitku (QRIS Realtime, Virtual Account, E-Wallet) dan Verifikasi Transfer Manual</td>
    </tr>
  </tbody>
</table>

<hr />

<h2 id="fitur-utama">Fitur Utama</h2>

<h3>1. Generasi Visual AI (Image & Video)</h3>
<ul>
  <li><strong>AI Magic Prompt Enhancer:</strong> Mengubah prompt ringkas pengguna menjadi instruksi visual sinematik beresolusi tinggi menggunakan AI internal yang dapat dikonfigurasi admin.</li>
  <li><strong>Multi-Engine Fallback:</strong> Pemrosesan generasi berurutan dari 9Router, Hugging Face, Worker Nodes, hingga fallback instan ke Pollinations FLUX.</li>
  <li><strong>AI Motion Video:</strong> Konversi Text-to-Video dan Image-to-Video dengan kontrol pergerakan kamera (Drone Zoom, Cinematic Pan, Orbit 360, Tilt Reveal).</li>
  <li><strong>Preset Gaya Artistik:</strong> 8 pilihan preset siap pakai (Cinematic 8K, Commercial Product, Studio Portrait, Anime, 3D Animation, Retro, Cyberpunk, Caricature).</li>
  <li><strong>Dual Upload & Blend:</strong> Kemampuan menggabungkan dua gambar referensi (komposisi karakter dan latar) secara simultan.</li>
</ul>

<h3>2. Proteksi & Monetisasi Pintar</h3>
<ul>
  <li><strong>Dynamic Watermark GD:</strong> Penambahan badge semi-transparan otomatis berisi logo geometris dan nama situs untuk pengguna gratisan.</li>
  <li><strong>Clean Export VIP:</strong> Pengguna berlisensi VIP atau langganan aktif mendapatkan hasil ekspor bersih tanpa watermark.</li>
  <li><strong>Sistem Reward Pendaftaran Fleksibel:</strong> Pengaturan perolehan kredit gratis yang dapat ditentukan administrator (Kredit Daftar Akun, Verifikasi Email, dan Kelengkapan Profil).</li>
  <li><strong>Lisensi Lifetime & Serial Key:</strong> Verifikasi kode lisensi sekali aktivasi untuk membuka akses VIP tanpa batas.</li>
</ul>

<h3>3. Dashboard & Administrasi Lengkap</h3>
<ul>
  <li><strong>Public Status Dashboard (<code>/status</code>):</strong> Halaman pemantauan latensi node AI, status kesehatan storage pool, dan ketersediaan layanan publik secara transparan.</li>
  <li><strong>Audit Log & Keamanan:</strong> Pencatatan aktivitas transaksi, error sistem, dan log pergantian kunci failover.</li>
  <li><strong>Manajemen Pengguna & Transaksi:</strong> Kendali penuh saldo kredit, status keanggotaan, persetujuan bukti bayar manual, dan pengaturan gateway.</li>
</ul>

<hr />

<h2 id="arsitektur-multi-layer">Arsitektur Multi-Layer & Failover</h2>

<pre>
[ Permintaan Pengguna ]
          │
          ▼
┌──────────────────────────────────────────────┐
│          Pixvia AI Engine Router             │
└──────┬───────────────┬───────────────┬───────┘
       │               │               │
       ▼ (Prioritas 1)  ▼ (Prioritas 2)  ▼ (Fallback Terakhir)
┌──────────────┐ ┌──────────────┐ ┌──────────────────┐
│   9Router    │ │ Hugging Face │ │  Pollinations    │
│ Multi-Key    │ │    FLUX.1    │ │  High-Speed FLUX │
│   Pool       │ │  Inference   │ │                  │
└──────┬───────┘ └──────┬───────┘ └────────┬─────────┘
       │                │                  │
       └────────────────┴──────────────────┘
                        │
                        ▼ (Output Binary)
       ┌────────────────────────────────┐
       │   Watermark Decision Engine    │
       │   - VIP: 100% Bersih           │
       │   - Free: Dynamic Watermark    │
       └────────────────┬───────────────┘
                        │
                        ▼
       ┌────────────────────────────────┐
       │   Storage Pool Service         │
       │   (Cloudflare R2 / Local SSD)  │
       └────────────────────────────────┘
</pre>

<hr />

<h2 id="penyimpanan-cloud-skala-besar">Penyimpanan Cloud Skala Besar (Multi-Bucket R2)</h2>

<p>
  Untuk mengantisipasi ratusan ribu generasi media tanpa membebani hosting lokal dan tanpa biaya bandwidth keluar (Zero Egress Fee), Pixvia AI mengintegrasikan <strong>Cloudflare R2 Multi-Account Pooling</strong>.
</p>

<ul>
  <li><strong>Distribusi Akun & Bucket:</strong> Administrator dapat mendaftarkan beberapa akun Cloudflare R2 sekaligus dalam format multi-line di panel admin.</li>
  <li><strong>Algoritma Round-Robin:</strong> File baru disimpan secara bergantian antar bucket yang aktif untuk menyeimbangkan kuota dan beban server.</li>
  <li><strong>Failover Local SSD:</strong> Jika seluruh koneksi bucket mengalami kendala, sistem secara otomatis menyimpan aset ke direktori lokal tanpa menggagalkan proses generasi pengguna.</li>
  <li><strong>Implementasi AWS SigV4 Native:</strong> Dibuat menggunakan algoritma kriptografi murni di PHP tanpa memerlukan dependensi composer AWS SDK yang berat.</li>
</ul>

<hr />

<h2 id="sistem-monetisasi--kredit">Sistem Monetisasi & Pengaturan Kredit</h2>

<p>
  Admin memiliki kendali penuh atas pembagian saldo kredit gratis untuk mendorong retensi dan akuisisi pengguna baru:
</p>

<table>
  <thead>
    <tr>
      <th>Aksi Pengguna</th>
      <th>Kredit Default</th>
      <th>Konfigurasi Admin</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Pendaftaran Akun Baru</td>
      <td>3 Kredit</td>
      <td>Dapat diubah via Pengaturan Sistem</td>
    </tr>
    <tr>
      <td>Verifikasi Alamat Email</td>
      <td>2 Kredit</td>
      <td>Kredit otomatis bertambah setelah link verifikasi diklik</td>
    </tr>
    <tr>
      <td>Melengkapi Profil Pengguna</td>
      <td>2 Kredit</td>
      <td>Diberikan satu kali setelah nama dan biodata terisi</td>
    </tr>
    <tr>
      <td>Klaim Voucher Promo</td>
      <td>Variabel</td>
      <td>Dikelola di menu manajemen kupon voucher</td>
    </tr>
  </tbody>
</table>

<hr />

<h2 id="panduan-instalasi">Panduan Instalasi</h2>

<h3>Lingkungan Lokal (Laragon)</h3>
<ol>
  <li>Clone repositori ini ke dalam direktori <code>www</code> Laragon:
    <pre><code>cd C:\laragon\www
git clone https://github.com/username/pixvia.git</code></pre>
  </li>
  <li>Pastikan modul Apache dan MySQL sudah berjalan di Laragon.</li>
  <li>Akses platform melalui browser:
    <pre><code>http://localhost/pixvia/
atau
http://pixvia.test/</code></pre>
  </li>
  <li>Database SQLite akan terbuat secara otomatis saat pertama kali dibuka. Jika ingin menggunakan MySQL, sesuaikan konfigurasi pada file <code>config/database.php</code>.</li>
</ol>

<h3>Lingkungan Produksi (cPanel / DirectAdmin)</h3>
<ol>
  <li>Unggah seluruh file ke direktori <code>public_html</code> atau subdomain tujuan.</li>
  <li>Pastikan versi PHP yang aktif adalah <strong>PHP 8.1</strong> atau yang lebih baru dengan ekstensi <code>curl</code>, <code>pdo</code>, <code>gd</code>, dan <code>mbstring</code> aktif.</li>
  <li>Pastikan folder <code>uploads/</code> dan <code>database/</code> memiliki izin tulis (permission 755 atau 775).</li>
  <li>Buka URL situs Anda untuk memicu inisialisasi awal.</li>
</ol>

<hr />

<h2 id="kredensial-demo">Kredensial Demo</h2>

<h3>Akun Administrator</h3>
<ul>
  <li><strong>URL Admin:</strong> <code>/admin</code></li>
  <li><strong>Email:</strong> <code>admin@pixvia.ai</code></li>
  <li><strong>Password:</strong> <code>admin123</code></li>
</ul>

<h3>Serial Key Lisensi VIP (Aktivasi Instan)</h3>
<ul>
  <li><code>PIXVIA-VIP-2026-LIFETIME-PRO</code></li>
  <li><code>PIXVIA-PRO-8899-UNLIMITED</code></li>
  <li><code>PIXVIA-CREATOR-5544-STUDIO</code></li>
</ul>

<h3>Kupon Saldo Promo</h3>
<ul>
  <li><code>PIXVIAFREE50</code> (Bonus 50 kredit saldo)</li>
</ul>

<hr />

<h2 id="struktur-direktori">Struktur Direktori</h2>

<pre>
pixvia/
├── app/
│   ├── Controllers/         # Controller aplikasi (Admin, Api, Auth, Studio, Status, dll.)
│   ├── Core/                # Engine dasar (Database, Router, Security, View)
│   └── Services/            # Layanan bisnis (AiEngine, StoragePoolService, R2Client, dll.)
├── assets/
│   ├── css/                 # Stylesheet khusus dan Tailwind utility
│   └── js/                  # Interaktivitas studio dan skrip client
├── config/                  # Konfigurasi database dan pengaturan inti
├── database/                # Skema migrasi dan file basis data SQLite
├── uploads/                 # Direktori penyimpanan media lokal
├── views/                   # Template tampilan antarmuka (Admin, Billing, Studio, Auth)
├── .htaccess                # Konfigurasi URL rewriting Apache
├── index.php                # Front controller utama
└── README.md                # Dokumentasi proyek
</pre>

<hr />

<h2 id="kebijakan-desain">Kebijakan Desain & Standar Teknis</h2>

<div align="center">
  <table>
    <tr>
      <td align="center" width="50%">
        <strong>Zero Purple Policy</strong><br />
        Bebas sepenuhnya dari gradasi warna ungu atau violet. Menggunakan palet Zinc profesional dengan aksen fungsional yang terukur.
      </td>
      <td align="center" width="50%">
        <strong>Zero Emoji Policy</strong><br />
        Seluruh antarmuka tidak menggunakan emoticon keyboard Unicode. Semua visual direpresentasikan melalui ikon SVG presisi.
      </td>
    </tr>
  </table>
</div>

<hr />

<div align="center">
  <p>Dikembangkan untuk keandalan produksi visual AI modern.</p>
  <p><strong>&copy; 2026 Pixvia AI Platform. All rights reserved.</strong></p>
</div>
