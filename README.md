<!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fajry | Video Editor Portfolio</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            overflow-x: hidden;
        }

        .glass-nav {
            background: rgba(255, 255, 255, 0.7);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
        }

        .hero-pattern {
            background-color: #ffffff;
            background-image: radial-gradient(#3b82f6 0.5px, transparent 0.5px), radial-gradient(#3b82f6 0.5px, #ffffff 0.5px);
            background-size: 20px 20px;
            background-position: 0 0, 10px 10px;
            opacity: 0.05;
        }

        .skill-card {
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .skill-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 25px -5px rgb(0 0 0 / 0.1), 0 8px 10px -6px rgb(0 0 0 / 0.1);
        }

        .animate-float {
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }

        .gradient-text {
            background: linear-gradient(90deg, #2563eb, #7c3aed);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        /* Reveal on scroll simple implementation */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease-out;
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-900">

    <!-- Navigation -->
    <nav class="fixed w-full z-[100] glass-nav border-b border-slate-200/50">
        <div class="max-w-7xl mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#" class="text-2xl font-extrabold tracking-tighter text-blue-600">FAJRY<span class="text-slate-400">.</span></a>
            
            <!-- Mobile Menu Toggle -->
            <button id="menu-btn" class="md:hidden text-slate-600 focus:outline-none p-2">
                <i class="fas fa-bars text-xl"></i>
            </button>

            <!-- Desktop Menu -->
            <ul class="hidden md:flex space-x-10 font-semibold text-slate-600">
                <li><a href="#home" class="hover:text-blue-600 transition-colors">Home</a></li>
                <li><a href="#about" class="hover:text-blue-600 transition-colors">About</a></li>
                <li><a href="#skills" class="hover:text-blue-600 transition-colors">Skills</a></li>
                <li><a href="#portfolio" class="hover:text-blue-600 transition-colors">Portfolio</a></li>
                <li><a href="#contact" class="bg-blue-600 text-white px-6 py-2 rounded-full hover:bg-blue-700 transition-all shadow-md">Hubungi Saya</a></li>
            </ul>
        </div>

        <!-- Mobile Menu Overlay -->
        <div id="mobile-menu" class="hidden md:hidden absolute top-full left-0 w-full bg-white border-b border-slate-200 shadow-xl overflow-hidden transition-all duration-300">
            <ul class="flex flex-col p-6 space-y-4 font-bold">
                <li><a href="#home" class="mobile-link block text-slate-600 py-2">Home</a></li>
                <li><a href="#about" class="mobile-link block text-slate-600 py-2">About</a></li>
                <li><a href="#skills" class="mobile-link block text-slate-600 py-2">Skills</a></li>
                <li><a href="#portfolio" class="mobile-link block text-slate-600 py-2">Portfolio</a></li>
                <li><a href="#contact" class="mobile-link block text-blue-600 py-2">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="relative min-h-screen flex items-center pt-20 overflow-hidden">
        <div class="absolute inset-0 hero-pattern"></div>
        <div class="max-w-7xl mx-auto px-6 grid md:grid-cols-2 gap-16 items-center relative z-10">
            <div class="order-2 md:order-1 text-center md:text-left">
                <span class="inline-block px-4 py-1.5 mb-6 text-sm font-bold tracking-widest text-blue-700 bg-blue-100 rounded-full uppercase">
                    Video Editor & Creative Specialist
                </span>
                <h1 class="text-5xl md:text-7xl font-extrabold mb-6 leading-tight text-slate-900">
                    Hi, I'm <span class="gradient-text">Fajry Rizky</span>
                </h1>
                <p class="text-lg md:text-xl text-slate-600 mb-10 max-w-lg leading-relaxed mx-auto md:mx-0">
                    "Halo! Kenalin, saya Fajry. Saya senang bisa berkarya melalui visual. Mari berkolaborasi untuk menciptakan cerita yang luar biasa!"
                </p>
                <div class="flex flex-col sm:flex-row gap-4 justify-center md:justify-start">
                    <a href="#portfolio" class="bg-blue-600 text-white px-10 py-4 rounded-2xl font-bold hover:bg-blue-700 transition-all shadow-xl shadow-blue-200 flex items-center justify-center group">
                        Lihat Karya
                        <i class="fas fa-arrow-right ml-2 group-hover:translate-x-1 transition-transform"></i>
                    </a>
                    <a href="#contact" class="bg-white text-slate-700 border-2 border-slate-200 px-10 py-4 rounded-2xl font-bold hover:bg-slate-50 transition-all flex items-center justify-center">
                        Konsultasi
                    </a>
                </div>
            </div>
            
            <div class="order-1 md:order-2 flex justify-center">
                <div class="relative">
                    <!-- Decorative shapes -->
                    <div class="absolute -top-10 -right-10 w-32 h-32 bg-purple-200 rounded-full mix-blend-multiply filter blur-xl opacity-70 animate-pulse"></div>
                    <div class="absolute -bottom-10 -left-10 w-32 h-32 bg-blue-200 rounded-full mix-blend-multiply filter blur-xl opacity-70 animate-pulse delay-700"></div>
                    
                    <div class="relative w-72 h-72 md:w-96 md:h-96 animate-float">
                        <div class="absolute inset-0 bg-gradient-to-tr from-blue-600 to-purple-500 rounded-3xl rotate-6 opacity-20"></div>
                        <img src="https://raw.githubusercontent.com/mmfrzqqrbni/Fajri-/refs/heads/main/IMG-20260131-WA0008.jpg" 
                             alt="Muhammad Fajry Rizky" 
                             class="relative z-10 w-full h-full object-cover rounded-3xl border-4 border-white shadow-2xl"
                             onerror="this.src='https://via.placeholder.com/500x500?text=Fajry'">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-32 bg-white relative">
        <div class="max-w-5xl mx-auto px-6">
            <div class="reveal">
                <div class="text-center mb-12">
                    <h2 class="text-4xl font-extrabold mb-4 text-slate-900">Tentang Saya</h2>
                    <div class="w-24 h-1.5 bg-blue-600 mx-auto rounded-full"></div>
                </div>
                <div class="grid md:grid-cols-2 gap-12 items-center">
                    <div class="space-y-6 text-slate-600 text-lg leading-relaxed">
                        <p class="font-medium text-slate-800">
                            Saya adalah seorang individu yang berdedikasi tinggi dengan latar belakang kedisiplinan yang kuat.
                        </p>
                        <p>
                            Latar belakang saya dibangun di atas pengalaman belajar dan keterlibatan aktif dalam berbagai proyek. Saya terbiasa mengasah kedisiplinan serta tanggung jawab untuk memastikan setiap tugas selesai dengan hasil terbaik.
                        </p>
                    </div>
                    <div class="bg-slate-50 p-8 rounded-3xl border border-slate-100 shadow-sm">
                        <h3 class="font-bold text-xl mb-4 text-blue-600">Visi Saya</h3>
                        <p class="text-slate-600 italic">
                            "Mampu memberikan kontribusi nyata pada industri kreatif dan pelayanan, mengandalkan kemampuan pemecahan masalah untuk membantu tim mencapai target maksimal."
                        </p>
                        <div class="mt-6 flex space-x-4">
                            <div class="flex flex-col">
                                <span class="text-2xl font-bold text-slate-900">100%</span>
                                <span class="text-sm text-slate-500 uppercase tracking-tighter">Commitment</span>
                            </div>
                            <div class="w-px h-10 bg-slate-200"></div>
                            <div class="flex flex-col">
                                <span class="text-2xl font-bold text-slate-900">Adaptif</span>
                                <span class="text-sm text-slate-500 uppercase tracking-tighter">Fast Learner</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="py-32 bg-slate-50">
        <div class="max-w-7xl mx-auto px-6">
            <div class="text-center mb-20 reveal">
                <h2 class="text-4xl font-extrabold mb-4">Keahlian & Karakter</h2>
                <p class="text-slate-500">Nilai-nilai inti yang saya bawa dalam setiap pekerjaan.</p>
            </div>
            
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
                <!-- Skill 1 -->
                <div class="skill-card bg-white p-10 rounded-3xl shadow-sm border border-slate-100 reveal" style="transition-delay: 100ms;">
                    <div class="w-16 h-16 bg-blue-50 text-blue-600 rounded-2xl flex items-center justify-center text-3xl mb-6">
                        <i class="fas fa-clock"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-3 text-slate-900">Manajemen Waktu</h3>
                    <p class="text-slate-500 leading-relaxed text-sm">Kemampuan mengelola deadline dengan efisiensi tinggi tanpa mengurangi kualitas.</p>
                </div>
                <!-- Skill 2 -->
                <div class="skill-card bg-white p-10 rounded-3xl shadow-sm border border-slate-100 reveal" style="transition-delay: 200ms;">
                    <div class="w-16 h-16 bg-purple-50 text-purple-600 rounded-2xl flex items-center justify-center text-3xl mb-6">
                        <i class="fas fa-medal"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-3 text-slate-900">Kedisiplinan</h3>
                    <p class="text-slate-500 leading-relaxed text-sm">Integritas dalam bekerja yang terasah dari pengalaman organisasi intensif.</p>
                </div>
                <!-- Skill 3 -->
                <div class="skill-card bg-white p-10 rounded-3xl shadow-sm border border-slate-100 reveal" style="transition-delay: 300ms;">
                    <div class="w-16 h-16 bg-green-50 text-green-600 rounded-2xl flex items-center justify-center text-3xl mb-6">
                        <i class="fas fa-bolt"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-3 text-slate-900">Adaptasi</h3>
                    <p class="text-slate-500 leading-relaxed text-sm">Cepat memahami alur kerja baru dan tren teknologi video terbaru.</p>
                </div>
                <!-- Skill 4 -->
                <div class="skill-card bg-white p-10 rounded-3xl shadow-sm border border-slate-100 reveal" style="transition-delay: 400ms;">
                    <div class="w-16 h-16 bg-orange-50 text-orange-600 rounded-2xl flex items-center justify-center text-3xl mb-6">
                        <i class="fas fa-shield-alt"></i>
                    </div>
                    <h3 class="text-xl font-bold mb-3 text-slate-900">Tanggung Jawab</h3>
                    <p class="text-slate-500 leading-relaxed text-sm">Menyelesaikan apa yang dimulai dengan standar hasil yang memuaskan.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Portfolio & Experience -->
    <section id="portfolio" class="py-32 bg-white">
        <div class="max-w-7xl mx-auto px-6">
            <div class="grid lg:grid-cols-2 gap-20">
                <!-- Karya / Project -->
                <div class="reveal">
                    <h2 class="text-3xl font-extrabold mb-10 inline-flex items-center">
                        <span class="w-8 h-8 bg-blue-600 rounded-lg mr-3 flex items-center justify-center text-white text-sm">
                            <i class="fas fa-film"></i>
                        </span>
                        Proyek Kreatif
                    </h2>
                    <div class="group relative overflow-hidden rounded-3xl shadow-2xl transition-all">
                        <div class="absolute inset-0 bg-blue-900/40 group-hover:bg-blue-900/10 transition-colors z-10"></div>
                        <img src="https://images.unsplash.com/photo-1574717024653-61fd2cf4d44d?auto=format&fit=crop&q=80&w=800" 
                             alt="Video Editing Project" 
                             class="w-full h-80 object-cover group-hover:scale-110 transition duration-700">
                        <div class="absolute bottom-0 left-0 w-full p-8 z-20 translate-y-2 group-hover:translate-y-0 transition-transform">
                            <span class="bg-blue-600 text-white text-xs font-bold px-3 py-1 rounded-full uppercase tracking-wider">Video Editing</span>
                            <h3 class="text-2xl font-extrabold text-white mt-3 mb-2">Visual Storytelling</h3>
                            <p class="text-blue-50/80 text-sm">Fokus pada transisi halus, color grading, dan narasi yang kuat.</p>
                        </div>
                    </div>
                </div>

                <!-- Pengalaman -->
                <div class="reveal">
                    <h2 class="text-3xl font-extrabold mb-10 inline-flex items-center">
                        <span class="w-8 h-8 bg-purple-600 rounded-lg mr-3 flex items-center justify-center text-white text-sm">
                            <i class="fas fa-briefcase"></i>
                        </span>
                        Pengalaman
                    </h2>
                    <div class="space-y-6">
                        <div class="bg-slate-50 p-8 rounded-3xl border border-slate-100 flex gap-6 group hover:border-blue-200 transition-colors">
                            <div class="shrink-0 w-14 h-14 bg-white rounded-2xl shadow-sm flex items-center justify-center text-blue-600 group-hover:bg-blue-600 group-hover:text-white transition-all">
                                <i class="fas fa-users-cog text-2xl"></i>
                            </div>
                            <div>
                                <span class="text-sm font-bold text-blue-600 uppercase">Organisasi</span>
                                <h3 class="text-xl font-extrabold text-slate-900 mt-1">PASKIBRA</h3>
                                <p class="text-slate-500 mt-3 leading-relaxed">
                                    Membentuk fondasi karakter dalam hal kedisiplinan, kerjasama tim di bawah tekanan, serta ketahanan mental yang tinggi.
                                </p>
                            </div>
                        </div>
                        
                        <div class="bg-slate-50 p-8 rounded-3xl border border-slate-100 flex gap-6 opacity-60">
                            <div class="shrink-0 w-14 h-14 bg-white rounded-2xl shadow-sm flex items-center justify-center text-slate-400">
                                <i class="fas fa-plus text-2xl"></i>
                            </div>
                            <div class="flex items-center">
                                <p class="text-slate-500 font-medium italic">Pengalaman lainnya akan segera ditambahkan...</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-32 relative overflow-hidden bg-slate-900">
        <div class="absolute top-0 right-0 w-1/3 h-full bg-blue-600/10 skew-x-12 translate-x-1/2"></div>
        <div class="max-w-7xl mx-auto px-6 relative z-10">
            <div class="text-center mb-20 reveal">
                <h2 class="text-4xl font-extrabold mb-4 text-white">Ayo Mulai Sesuatu</h2>
                <p class="text-slate-400">Saya terbuka untuk kolaborasi proyek video maupun peluang karir lainnya.</p>
            </div>
            
            <div class="grid md:grid-cols-3 gap-6 max-w-5xl mx-auto">
                <!-- WhatsApp -->
                <a href="https://wa.me/628121540719" target="_blank" class="flex flex-col items-center p-10 bg-slate-800/50 backdrop-blur-sm rounded-3xl border border-slate-700 hover:border-green-500 transition-all group reveal">
                    <div class="w-16 h-16 bg-green-500/10 text-green-500 rounded-2xl flex items-center justify-center text-3xl mb-6 group-hover:scale-110 transition-transform">
                        <i class="fab fa-whatsapp"></i>
                    </div>
                    <h3 class="font-bold text-xl text-white mb-2">WhatsApp</h3>
                    <p class="text-slate-400 text-sm">0812-1540-719</p>
                </a>
                
                <!-- Instagram -->
                <a href="https://instagram.com/mmfrzqqrbni" target="_blank" class="flex flex-col items-center p-10 bg-slate-800/50 backdrop-blur-sm rounded-3xl border border-slate-700 hover:border-pink-500 transition-all group reveal" style="transition-delay: 100ms;">
                    <div class="w-16 h-16 bg-pink-500/10 text-pink-500 rounded-2xl flex items-center justify-center text-3xl mb-6 group-hover:scale-110 transition-transform">
                        <i class="fab fa-instagram"></i>
                    </div>
                    <h3 class="font-bold text-xl text-white mb-2">Instagram</h3>
                    <p class="text-slate-400 text-sm">@mmfrzqqrbni</p>
                </a>
                
                <!-- Email -->
                <a href="mailto:fajripuch@gmail.com" class="flex flex-col items-center p-10 bg-slate-800/50 backdrop-blur-sm rounded-3xl border border-slate-700 hover:border-blue-500 transition-all group reveal" style="transition-delay: 200ms;">
                    <div class="w-16 h-16 bg-blue-500/10 text-blue-500 rounded-2xl flex items-center justify-center text-3xl mb-6 group-hover:scale-110 transition-transform">
                        <i class="far fa-envelope"></i>
                    </div>
                    <h3 class="font-bold text-xl text-white mb-2">Email</h3>
                    <p class="text-slate-400 text-sm">fajripuch@gmail.com</p>
                </a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="py-20 bg-white border-t border-slate-100">
        <div class="max-w-7xl mx-auto px-6 text-center">
            <h2 class="text-2xl font-extrabold tracking-tighter text-blue-600 mb-8">FAJRY.</h2>
            <div class="flex justify-center space-x-8 mb-10">
                <a href="#" class="text-slate-400 hover:text-pink-500 transition-colors text-xl"><i class="fab fa-instagram"></i></a>
                <a href="#" class="text-slate-400 hover:text-green-500 transition-colors text-xl"><i class="fab fa-whatsapp"></i></a>
                <a href="#" class="text-slate-400 hover:text-blue-500 transition-colors text-xl"><i class="far fa-envelope"></i></a>
            </div>
            <p class="text-slate-400 text-sm font-medium">
                &copy; 2026 Fajry Portfolio. Dibuat dengan dedikasi dan tanggung jawab.
            </p>
        </div>
    </footer>

    <script>
        // Mobile Menu Logic
        const menuBtn = document.getElementById('menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');
        const mobileLinks = document.querySelectorAll('.mobile-link');

        menuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        mobileLinks.forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });

        // Simple Reveal Animation on Scroll
        function reveal() {
            var reveals = document.querySelectorAll(".reveal");
            for (var i = 0; i < reveals.length; i++) {
                var windowHeight = window.innerHeight;
                var elementTop = reveals[i].getBoundingClientRect().top;
                var elementVisible = 150;
                if (elementTop < windowHeight - elementVisible) {
                    reveals[i].classList.add("active");
                }
            }
        }

        window.addEventListener("scroll", reveal);
        // Run once on load
        window.onload = reveal;
    </script>
</body>
</html>
