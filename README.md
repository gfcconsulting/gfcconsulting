<!DOCTYPE html>
<html lang="fr" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GFC Consulting | Gestion, Finance, Conseil</title>
    <meta name="description" content="GFC Consulting vous accompagne dans la gestion, la finance et le conseil pour optimiser vos performances et soutenir votre croissance à Casablanca.">
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=DM+Sans:opsz,wght@9..40,300;400;500;600&family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400&display=swap" rel="stylesheet">
    
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['DM Sans', 'sans-serif'],
                        serif: ['Playfair Display', 'serif'],
                    },
                    colors: {
                        brand: {
                            dark: '#0B1C33',
                            primary: '#00AEEF', /* Bright cyan-blue matching the official logo */
                            accent: '#00D4FF',
                            light: '#F8FAFC',
                        }
                    },
                    animation: {
                        'fade-in-up': 'fadeInUp 0.8s ease-out forwards',
                        'fade-in': 'fadeIn 1s ease-out forwards',
                    },
                    keyframes: {
                        fadeInUp: {
                            '0%': { opacity: '0', transform: 'translateY(30px)' },
                            '100%': { opacity: '1', transform: 'translateY(0)' },
                        },
                        fadeIn: {
                            '0%': { opacity: '0' },
                            '100%': { opacity: '1' },
                        }
                    }
                }
            }
        }
    </script>

    <style>
        /* Custom Aesthetic Enhancements */
        body {
            background-color: #F8FAFC;
            color: #0B1C33;
        }
        
        .gradient-mesh {
            background-color: #0B1C33;
            background-image: 
                radial-gradient(at 0% 0%, rgba(14, 165, 233, 0.15) 0px, transparent 50%),
                radial-gradient(at 100% 0%, rgba(0, 212, 255, 0.1) 0px, transparent 50%),
                radial-gradient(at 100% 100%, rgba(14, 165, 233, 0.15) 0px, transparent 50%),
                radial-gradient(at 0% 100%, rgba(0, 212, 255, 0.1) 0px, transparent 50%);
        }

        .glass-card {
            background: rgba(255, 255, 255, 0.7);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.5);
            box-shadow: 0 8px 32px rgba(11, 28, 51, 0.05);
        }

        .text-gradient {
            background: linear-gradient(135deg, #00AEEF 0%, #00D4FF 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hover-lift {
            transition: transform 0.3s cubic-bezier(0.34, 1.56, 0.64, 1), box-shadow 0.3s ease;
        }
        .hover-lift:hover {
            transform: translateY(-8px);
            box-shadow: 0 20px 40px rgba(14, 165, 233, 0.15);
        }

        /* Scroll Reveal Utility */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s cubic-bezier(0.5, 0, 0, 1);
        }
        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        .nav-blur {
            backdrop-filter: blur(16px);
            background: rgba(255, 255, 255, 0.85);
            border-bottom: 1px solid rgba(11, 28, 51, 0.05);
        }
    </style>
</head>
<body class="antialiased overflow-x-hidden">

    <!-- Navigation -->
    <nav class="fixed w-full z-50 nav-blur transition-all duration-300" id="navbar">
        <div class="max-w-7xl mx-auto px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <div class="flex items-center gap-3">
                    <div class="w-10 h-10 bg-brand-primary rounded-lg flex items-center justify-center text-white font-sans font-bold text-lg tracking-tighter">GFC</div>
                    <div class="flex flex-col">
                        <span class="font-sans font-bold text-xl text-brand-dark tracking-tight">GFC CONSULTING</span>
                        <span class="text-[10px] uppercase tracking-widest text-brand-primary font-semibold">Gestion, Finance, Conseil</span>
                    </div>
                </div>
                <div class="hidden md:flex items-center gap-8">
                    <a href="#mission" class="text-sm font-medium text-brand-dark/70 hover:text-brand-primary transition-colors">Mission</a>
                    <a href="#services" class="text-sm font-medium text-brand-dark/70 hover:text-brand-primary transition-colors">Services</a>
                    <a href="#expertise" class="text-sm font-medium text-brand-dark/70 hover:text-brand-primary transition-colors">Expertise</a>
                    <a href="#contact" class="px-6 py-2.5 bg-brand-dark text-white text-sm font-semibold rounded-full hover:bg-brand-primary transition-all duration-300 shadow-lg hover:shadow-brand-primary/30">Nous Contacter</a>
                </div>
                <button class="md:hidden text-brand-dark" id="mobile-menu-btn">
                    <i data-lucide="menu" class="w-6 h-6"></i>
                </button>
            </div>
        </div>
        <!-- Mobile Menu -->
        <div class="hidden md:hidden bg-white border-t border-gray-100 absolute w-full" id="mobile-menu">
            <div class="px-6 py-4 space-y-4">
                <a href="#mission" class="block text-brand-dark font-medium">Mission</a>
                <a href="#services" class="block text-brand-dark font-medium">Services</a>
                <a href="#expertise" class="block text-brand-dark font-medium">Expertise</a>
                <a href="#contact" class="block text-brand-primary font-semibold">Nous Contacter</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="relative min-h-screen flex items-center gradient-mesh pt-20 overflow-hidden">
        <!-- Decorative Elements -->
        <div class="absolute top-1/4 right-0 w-96 h-96 bg-brand-primary/10 rounded-full blur-3xl"></div>
        <div class="absolute bottom-0 left-0 w-72 h-72 bg-brand-accent/10 rounded-full blur-3xl"></div>

        <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10 grid lg:grid-cols-2 gap-12 items-center">
            <div class="space-y-8 animate-fade-in-up">
                <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-white/10 border border-white/20 backdrop-blur-sm">
                    <span class="w-2 h-2 rounded-full bg-brand-accent animate-pulse"></span>
                    <span class="text-sm font-medium text-white/90">Cabinet d'expertise à Casablanca</span>
                </div>
                <h1 class="font-serif text-5xl lg:text-7xl font-bold text-white leading-[1.1]">
                    Votre partenaire pour une <span class="text-gradient">gestion performante</span>.
                </h1>
                <p class="text-lg text-white/70 max-w-lg leading-relaxed">
                    GFC Consulting vous accompagne dans la gestion, la finance et le conseil pour optimiser vos performances, sécuriser vos décisions et soutenir votre croissance.
                </p>
                <div class="flex flex-wrap gap-4">
                    <a href="#contact" class="px-8 py-4 bg-brand-primary text-white font-semibold rounded-full hover:bg-brand-accent transition-all duration-300 shadow-xl shadow-brand-primary/20 flex items-center gap-2">
                        Démarrer un projet
                        <i data-lucide="arrow-right" class="w-4 h-4"></i>
                    </a>
                    <a href="#services" class="px-8 py-4 bg-white/10 text-white font-semibold rounded-full border border-white/20 hover:bg-white/20 transition-all duration-300 backdrop-blur-sm">
                        Nos services
                    </a>
                </div>
            </div>
            
            <div class="relative hidden lg:block animate-fade-in" style="animation-delay: 0.3s;">
                <div class="relative rounded-2xl overflow-hidden shadow-2xl border border-white/10 group">
                    <!-- Professional Photo -->
                    <img src="https://images.unsplash.com/photo-1556761175-5973dc0f32e7?auto=format&fit=crop&q=80&w=1000" alt="Consulting professionnel GFC" class="w-full h-[500px] object-cover transition-transform duration-700 group-hover:scale-105">
                    
                    <!-- Dark Overlay for readability -->
                    <div class="absolute inset-0 bg-gradient-to-t from-brand-dark/90 via-brand-dark/20 to-transparent"></div>
                    
                    <!-- Logo Overlaid on Image (as requested: PHOTO + LOGO SUR IMAGE) -->
                    <div class="absolute top-6 right-6 glass-card p-4 rounded-xl flex items-center gap-3 animate-fade-in-up" style="animation-delay: 0.6s;">
                        <div class="w-12 h-12 bg-brand-primary rounded-lg flex items-center justify-center text-white font-sans font-bold text-xl tracking-tighter shadow-lg">GFC</div>
                        <div class="flex flex-col">
                            <span class="font-sans font-bold text-lg text-brand-dark tracking-tight leading-none">GFC CONSULTING</span>
                            <span class="text-[9px] uppercase tracking-widest text-brand-primary font-bold mt-1">Gestion, Finance, Conseil</span>
                        </div>
                    </div>

                    <!-- Bottom Stats Card -->
                    <div class="absolute bottom-6 left-6 right-6">
                        <div class="glass-card p-5 rounded-xl flex items-center justify-between">
                            <div class="flex items-center gap-4">
                                <div class="w-12 h-12 rounded-full bg-brand-primary/20 flex items-center justify-center text-brand-accent">
                                    <i data-lucide="trending-up" class="w-6 h-6"></i>
                                </div>
                                <div>
                                    <p class="text-brand-dark font-bold text-sm">Croissance optimisée</p>
                                    <p class="text-brand-dark/60 text-xs">Solutions sur mesure à Casablanca</p>
                                </div>
                            </div>
                            <div class="h-8 w-px bg-brand-dark/10"></div>
                            <div class="flex items-center gap-4">
                                <div class="w-12 h-12 rounded-full bg-brand-primary/20 flex items-center justify-center text-brand-accent">
                                    <i data-lucide="shield-check" class="w-6 h-6"></i>
                                </div>
                                <div>
                                    <p class="text-brand-dark font-bold text-sm">Comptable Agréé</p>
                                    <p class="text-brand-dark/60 text-xs">Membre OPCAM</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Mission Section -->
    <section id="mission" class="py-24 bg-brand-light relative overflow-hidden">
        <!-- Decorative background element -->
        <div class="absolute top-0 left-0 w-full h-full opacity-5 pointer-events-none">
            <svg width="100%" height="100%">
                <pattern id="grid" width="40" height="40" patternUnits="userSpaceOnUse">
                    <path d="M 40 0 L 0 0 0 40" fill="none" stroke="#0EA5E9" stroke-width="1"/>
                </pattern>
                <rect width="100%" height="100%" fill="url(#grid)" />
            </svg>
        </div>

        <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
            <div class="grid lg:grid-cols-12 gap-12 items-center reveal">
                <div class="lg:col-span-5 relative">
                    <div class="absolute -top-4 -left-4 w-32 h-32 bg-brand-primary/10 rounded-full blur-2xl"></div>
                    <div class="relative bg-brand-dark p-8 lg:p-10 rounded-2xl text-white shadow-2xl border border-white/10">
                        <div class="flex items-center gap-3 mb-6">
                            <div class="w-12 h-12 rounded-full bg-brand-primary/20 flex items-center justify-center">
                                <i data-lucide="target" class="w-6 h-6 text-brand-accent"></i>
                            </div>
                            <span class="text-brand-accent font-semibold tracking-wider uppercase text-sm">Notre Mission</span>
                        </div>
                        <h2 class="font-serif text-3xl lg:text-4xl font-bold mb-6 leading-tight">
                            "Créer de la valeur, éclairer vos décisions, construire votre avenir."
                        </h2>
                        <div class="w-16 h-1 bg-brand-primary rounded-full"></div>
                    </div>
                </div>
                <div class="lg:col-span-7 space-y-6">
                    <h3 class="font-serif text-3xl lg:text-4xl font-bold text-brand-dark">
                        Votre partenaire pour une <span class="text-brand-primary">gestion performante</span>.
                    </h3>
                    <p class="text-brand-dark/70 text-lg leading-relaxed">
                        GFC Consulting vous accompagne dans la gestion, la finance et le conseil pour optimiser vos performances, sécuriser vos décisions et soutenir votre croissance. Nous croyons que chaque entreprise mérite une stratégie financière et opérationnelle solide.
                    </p>
                    <div class="grid sm:grid-cols-2 gap-6 pt-4">
                        <div class="flex items-start gap-3 p-4 bg-white rounded-xl shadow-sm border border-gray-100">
                            <div class="w-8 h-8 rounded-full bg-brand-primary/10 flex items-center justify-center flex-shrink-0">
                                <i data-lucide="check-circle" class="w-5 h-5 text-brand-primary"></i>
                            </div>
                            <span class="text-brand-dark font-medium">Conformité aux normes en vigueur</span>
                        </div>
                        <div class="flex items-start gap-3 p-4 bg-white rounded-xl shadow-sm border border-gray-100">
                            <div class="w-8 h-8 rounded-full bg-brand-primary/10 flex items-center justify-center flex-shrink-0">
                                <i data-lucide="check-circle" class="w-5 h-5 text-brand-primary"></i>
                            </div>
                            <span class="text-brand-dark font-medium">Accompagnement personnalisé</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="py-24 bg-brand-light relative overflow-hidden">
        <div class="absolute top-0 right-0 w-1/3 h-full bg-gradient-to-l from-brand-primary/5 to-transparent"></div>
        <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
            <div class="text-center max-w-3xl mx-auto mb-16 reveal">
                <span class="text-brand-primary font-semibold tracking-wider uppercase text-sm">Nos Domaines d'Intervention</span>
                <h2 class="font-serif text-4xl lg:text-5xl font-bold text-brand-dark mt-3 mb-6">Des solutions complètes pour votre entreprise</h2>
                <p class="text-brand-dark/60 text-lg">Nous couvrons l'ensemble de vos besoins en gestion et finance pour vous permettre de vous concentrer sur votre cœur de métier.</p>
            </div>

            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Service 1: GESTION -->
                <div class="glass-card p-8 rounded-2xl hover-lift reveal group border-t-4 border-transparent hover:border-brand-primary transition-all duration-300">
                    <div class="w-14 h-14 rounded-xl bg-brand-primary/10 flex items-center justify-center text-brand-primary mb-6 group-hover:bg-brand-primary group-hover:text-white transition-colors duration-300">
                        <i data-lucide="briefcase" class="w-7 h-7"></i>
                    </div>
                    <h3 class="font-serif text-xl font-bold text-brand-dark mb-3">Gestion</h3>
                    <p class="text-brand-dark/60 leading-relaxed">Organisation, suivi et optimisation de vos processus pour une plus grande efficacité.</p>
                </div>

                <!-- Service 2: FINANCE -->
                <div class="glass-card p-8 rounded-2xl hover-lift reveal group border-t-4 border-transparent hover:border-brand-primary transition-all duration-300" style="transition-delay: 100ms;">
                    <div class="w-14 h-14 rounded-xl bg-brand-primary/10 flex items-center justify-center text-brand-primary mb-6 group-hover:bg-brand-primary group-hover:text-white transition-colors duration-300">
                        <i data-lucide="line-chart" class="w-7 h-7"></i>
                    </div>
                    <h3 class="font-serif text-xl font-bold text-brand-dark mb-3">Finance</h3>
                    <p class="text-brand-dark/60 leading-relaxed">Analyse financière, planification, gestion de trésorerie et recherche de financement.</p>
                </div>

                <!-- Service 3: CONSEIL -->
                <div class="glass-card p-8 rounded-2xl hover-lift reveal group border-t-4 border-transparent hover:border-brand-primary transition-all duration-300" style="transition-delay: 200ms;">
                    <div class="w-14 h-14 rounded-xl bg-brand-primary/10 flex items-center justify-center text-brand-primary mb-6 group-hover:bg-brand-primary group-hover:text-white transition-colors duration-300">
                        <i data-lucide="compass" class="w-7 h-7"></i>
                    </div>
                    <h3 class="font-serif text-xl font-bold text-brand-dark mb-3">Conseil</h3>
                    <p class="text-brand-dark/60 leading-relaxed">Conseils stratégiques et opérationnels pour accompagner vos projets et décisions clés.</p>
                </div>

                <!-- Service 4: COMPTABILITÉ -->
                <div class="glass-card p-8 rounded-2xl hover-lift reveal group border-t-4 border-transparent hover:border-brand-primary transition-all duration-300">
                    <div class="w-14 h-14 rounded-xl bg-brand-primary/10 flex items-center justify-center text-brand-primary mb-6 group-hover:bg-brand-primary group-hover:text-white transition-colors duration-300">
                        <i data-lucide="calculator" class="w-7 h-7"></i>
                    </div>
                    <h3 class="font-serif text-xl font-bold text-brand-dark mb-3">Comptabilité</h3>
                    <p class="text-brand-dark/60 leading-relaxed">Tenue, révision et mise en conformité de votre comptabilité selon les normes en vigueur.</p>
                </div>

                <!-- Service 5: ACCOMPAGNEMENT -->
                <div class="glass-card p-8 rounded-2xl hover-lift reveal group md:col-span-2 lg:col-span-2 border-t-4 border-transparent hover:border-brand-primary transition-all duration-300" style="transition-delay: 100ms;">
                    <div class="w-14 h-14 rounded-xl bg-brand-primary/10 flex items-center justify-center text-brand-primary mb-6 group-hover:bg-brand-primary group-hover:text-white transition-colors duration-300">
                        <i data-lucide="users" class="w-7 h-7"></i>
                    </div>
                    <h3 class="font-serif text-xl font-bold text-brand-dark mb-3">Accompagnement</h3>
                    <p class="text-brand-dark/60 leading-relaxed">Suivi personnalisé et solutions sur mesure adaptées à vos besoins.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Why Choose Us & Credentials -->
    <section id="expertise" class="py-24 bg-brand-dark text-white relative overflow-hidden">
        <div class="absolute inset-0 opacity-10" style="background-image: radial-gradient(#00AEEF 1px, transparent 1px); background-size: 32px 32px;"></div>
        
        <div class="max-w-7xl mx-auto px-6 lg:px-8 relative z-10">
            <div class="grid lg:grid-cols-2 gap-16">
                <!-- Why Choose Us -->
                <div class="reveal">
                    <span class="text-brand-accent font-semibold tracking-wider uppercase text-sm">Pourquoi Nous Choisir ?</span>
                    <h2 class="font-serif text-4xl font-bold mt-3 mb-8">L'excellence au service de votre réussite</h2>
                    
                    <div class="grid sm:grid-cols-2 gap-6">
                        <div class="bg-white/5 border border-white/10 p-6 rounded-2xl backdrop-blur-sm hover:bg-white/10 transition-colors">
                            <div class="w-12 h-12 rounded-full bg-brand-primary/20 flex items-center justify-center mb-4">
                                <i data-lucide="award" class="w-6 h-6 text-brand-accent"></i>
                            </div>
                            <h4 class="font-bold text-lg mb-2 text-white">Expertise</h4>
                            <p class="text-white/60 text-sm">Équipe qualifiée et expérimentée.</p>
                        </div>
                        <div class="bg-white/5 border border-white/10 p-6 rounded-2xl backdrop-blur-sm hover:bg-white/10 transition-colors">
                            <div class="w-12 h-12 rounded-full bg-brand-primary/20 flex items-center justify-center mb-4">
                                <i data-lucide="settings" class="w-6 h-6 text-brand-accent"></i>
                            </div>
                            <h4 class="font-bold text-lg mb-2 text-white">Solutions sur Mesure</h4>
                            <p class="text-white/60 text-sm">Réponses adaptées à chaque besoin.</p>
                        </div>
                        <div class="bg-white/5 border border-white/10 p-6 rounded-2xl backdrop-blur-sm hover:bg-white/10 transition-colors">
                            <div class="w-12 h-12 rounded-full bg-brand-primary/20 flex items-center justify-center mb-4">
                                <i data-lucide="zap" class="w-6 h-6 text-brand-accent"></i>
                            </div>
                            <h4 class="font-bold text-lg mb-2 text-white">Performance</h4>
                            <p class="text-white/60 text-sm">Résultats concrets et mesurables.</p>
                        </div>
                        <div class="bg-white/5 border border-white/10 p-6 rounded-2xl backdrop-blur-sm hover:bg-white/10 transition-colors">
                            <div class="w-12 h-12 rounded-full bg-brand-primary/20 flex items-center justify-center mb-4">
                                <i data-lucide="shield-check" class="w-6 h-6 text-brand-accent"></i>
                            </div>
                            <h4 class="font-bold text-lg mb-2 text-white">Confiance</h4>
                            <p class="text-white/60 text-sm">Engagement, rigueur et confidentialité.</p>
                        </div>
                    </div>
                </div>

                <!-- Credentials -->
                <div class="reveal" style="transition-delay: 200ms;">
                    <span class="text-brand-accent font-semibold tracking-wider uppercase text-sm">Nos Garanties</span>
                    <h2 class="font-serif text-4xl font-bold mt-3 mb-8">Certifications et Affiliations</h2>
                    
                    <div class="space-y-6">
                        <div class="bg-white/5 border border-white/10 p-6 rounded-2xl backdrop-blur-sm">
                            <div class="flex items-center gap-4 mb-3">
                                <i data-lucide="badge-check" class="w-8 h-8 text-brand-accent"></i>
                                <h4 class="font-bold text-xl">Comptable Agréé</h4>
                            </div>
                            <p class="text-white/70">Professionnalisme, rigueur et conformité garantie avec les normes en vigueur.</p>
                        </div>
                        
                        <div class="bg-white/5 border border-white/10 p-6 rounded-2xl backdrop-blur-sm">
                            <div class="flex items-center gap-4 mb-3">
                                <i data-lucide="building-2" class="w-8 h-8 text-brand-accent"></i>
                                <h4 class="font-bold text-xl">Membre OPCAM</h4>
                            </div>
                            <p class="text-white/70 mb-2">Organisation Professionnelle des Comptables Agréés du Maroc.</p>
                            <p class="text-sm text-white/50 italic">المنظمة المهنية للمحاسبين المعتمدين</p>
                        </div>

                        <div class="bg-white/5 border border-white/10 p-6 rounded-2xl backdrop-blur-sm">
                            <div class="flex items-center gap-4 mb-3">
                                <i data-lucide="scale" class="w-8 h-8 text-brand-accent"></i>
                                <h4 class="font-bold text-xl">Déontologie Professionnelle</h4>
                            </div>
                            <p class="text-white/70">Services strictement conformes aux normes professionnelles et éthiques.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-24 bg-white relative">
        <div class="max-w-7xl mx-auto px-6 lg:px-8">
            <div class="grid lg:grid-cols-2 gap-16">
                <div class="reveal">
                    <span class="text-brand-primary font-semibold tracking-wider uppercase text-sm">Contactez-nous</span>
                    <h2 class="font-serif text-4xl lg:text-5xl font-bold text-brand-dark mt-3 mb-6">Discutons de votre projet</h2>
                    <p class="text-brand-dark/60 text-lg mb-10">Notre équipe est à votre disposition pour répondre à toutes vos questions et vous accompagner dans vos démarches.</p>
                    
                    <div class="space-y-6">
                        <div class="flex items-start gap-4">
                            <div class="w-12 h-12 rounded-full bg-brand-primary/10 flex items-center justify-center text-brand-primary flex-shrink-0">
                                <i data-lucide="phone" class="w-5 h-5"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-brand-dark mb-1">Téléphone</h4>
                                <p class="text-brand-dark/70">+212 673 607 197</p>
                                <p class="text-brand-dark/70">+212 660 223 988</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start gap-4">
                            <div class="w-12 h-12 rounded-full bg-brand-primary/10 flex items-center justify-center text-brand-primary flex-shrink-0">
                                <i data-lucide="mail" class="w-5 h-5"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-brand-dark mb-1">Email</h4>
                                <a href="/cdn-cgi/l/email-protection#3a5955544e5b594e145d5c59595554494f564e53545d7a5d575b535614595557" class="text-brand-primary hover:underline"><span class="__cf_email__" data-cfemail="482b27263c292b3c662f2e2b2b27263b3d243c21262f082f25292124662b2725">[email&#160;protected]</span></a>
                            </div>
                        </div>
                        
                        <div class="flex items-start gap-4">
                            <div class="w-12 h-12 rounded-full bg-brand-primary/10 flex items-center justify-center text-brand-primary flex-shrink-0">
                                <i data-lucide="map-pin" class="w-5 h-5"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-brand-dark mb-1">Localisation</h4>
                                <p class="text-brand-dark/70">Casablanca, Maroc</p>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="reveal" style="transition-delay: 200ms;">
                    <form class="bg-brand-light p-8 lg:p-10 rounded-3xl border border-gray-100 shadow-sm space-y-6">
                        <div class="grid sm:grid-cols-2 gap-6">
                            <div>
                                <label class="block text-sm font-semibold text-brand-dark mb-2">Nom complet</label>
                                <input type="text" class="w-full px-4 py-3 rounded-xl border border-gray-200 focus:border-brand-primary focus:ring-2 focus:ring-brand-primary/20 outline-none transition-all bg-white" placeholder="Votre nom">
                            </div>
                            <div>
                                <label class="block text-sm font-semibold text-brand-dark mb-2">Email</label>
                                <input type="email" class="w-full px-4 py-3 rounded-xl border border-gray-200 focus:border-brand-primary focus:ring-2 focus:ring-brand-primary/20 outline-none transition-all bg-white" placeholder="votre@email.com">
                            </div>
                        </div>
                        <div>
                            <label class="block text-sm font-semibold text-brand-dark mb-2">Sujet</label>
                            <select class="w-full px-4 py-3 rounded-xl border border-gray-200 focus:border-brand-primary focus:ring-2 focus:ring-brand-primary/20 outline-none transition-all bg-white text-brand-dark/70">
                                <option>Demande de devis</option>
                                <option>Conseil en gestion</option>
                                <option>Comptabilité</option>
                                <option>Autre</option>
                            </select>
                        </div>
                        <div>
                            <label class="block text-sm font-semibold text-brand-dark mb-2">Message</label>
                            <textarea rows="4" class="w-full px-4 py-3 rounded-xl border border-gray-200 focus:border-brand-primary focus:ring-2 focus:ring-brand-primary/20 outline-none transition-all bg-white resize-none" placeholder="Décrivez votre besoin..."></textarea>
                        </div>
                        <button type="submit" class="w-full py-4 bg-brand-dark text-white font-semibold rounded-xl hover:bg-brand-primary transition-all duration-300 shadow-lg hover:shadow-brand-primary/30 flex items-center justify-center gap-2">
                            Envoyer le message
                            <i data-lucide="send" class="w-4 h-4"></i>
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-brand-dark text-white py-12 border-t border-white/10">
        <div class="max-w-7xl mx-auto px-6 lg:px-8">
            <div class="flex flex-col md:flex-row justify-between items-center gap-6">
                <div class="flex items-center gap-3">
                    <div class="w-8 h-8 bg-brand-primary rounded-lg flex items-center justify-center text-white font-sans font-bold text-xs tracking-tighter">GFC</div>
                    <div class="flex flex-col">
                        <span class="font-sans font-bold text-lg text-white tracking-tight">GFC CONSULTING</span>
                        <span class="text-[9px] uppercase tracking-widest text-brand-accent font-semibold">Gestion, Finance, Conseil</span>
                    </div>
                </div>
                <p class="text-white/50 text-sm text-center md:text-right">
                    GFC CONSULTING, votre réussite, notre engagement.<br>
                    &copy; 2026 Tous droits réservés.
                </p>
            </div>
        </div>
    </footer>

    <!-- Scripts -->
    <script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script><script>
        // Initialize Lucide Icons
        lucide.createIcons();

        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');
        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // Scroll Reveal Animation
        const observerOptions = {
            root: null,
            rootMargin: '0px',
            threshold: 0.1
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('active');
                    observer.unobserve(entry.target);
                }
            });
        }, observerOptions);

        document.querySelectorAll('.reveal').forEach((el) => {
            observer.observe(el);
        });

        // Navbar blur effect on scroll
        const navbar = document.getElementById('navbar');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 50) {
                navbar.classList.add('shadow-sm');
            } else {
                navbar.classList.remove('shadow-sm');
            }
        });
    </script>
<script defer src="https://static.cloudflareinsights.com/beacon.min.js/v833ccba57c9e4d2798f2e76cebdd09a11778172276447" integrity="sha512-57MDmcccJXYtNnH+ZiBwzC4jb2rvgVCEokYN+L/nLlmO8rfYT/gIpW2A569iJ/3b+0UEasghjuZH/ma3wIs/EQ==" data-cf-beacon='{"version":"2024.11.0","token":"75124c326cb447fe934cde04713ae013","r":1,"server_timing":{"name":{"cfCacheStatus":true,"cfEdge":true,"cfExtPri":true,"cfL4":true,"cfOrigin":true,"cfSpeedBrain":true},"location_startswith":null}}' crossorigin="anonymous"></script>
</body>
</html>
