<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Android & AI Developer Portfolio</title>
    <meta name="description" content="Portfolio of an Android and AI Mobile App Developer.">
    
    <!-- Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet">
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <!-- Tailwind Configuration -->
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        display: ['Space Grotesk', 'sans-serif'],
                    },
                    colors: {
                        brand: {
                            50: '#f0fdfa',
                            100: '#ccfbf1',
                            200: '#99f6e4',
                            300: '#5eead4',
                            400: '#2dd4bf',
                            500: '#14b8a6', // Primary Teal
                            600: '#0d9488',
                            700: '#0f766e',
                            800: '#115e59',
                            900: '#134e4a',
                            950: '#042f2e',
                        }
                    },
                    animation: {
                        'float': 'float 6s ease-in-out infinite',
                        'pulse-slow': 'pulse 4s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                    },
                    keyframes: {
                        float: {
                            '0%, 100%': { transform: 'translateY(0)' },
                            '50%': { transform: 'translateY(-20px)' },
                        }
                    }
                }
            }
        }
    </script>

    <style>
        body {
            background-color: #0f172a; /* Slate 900 */
            color: #f8fafc; /* Slate 50 */
        }
        
        .glass-nav {
            background: rgba(15, 23, 42, 0.8);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .glass-card {
            background: rgba(30, 41, 59, 0.5); /* Slate 800 with opacity */
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .glass-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px -10px rgba(20, 184, 166, 0.3); /* Brand glow */
            border-color: rgba(20, 184, 166, 0.3);
        }

        .gradient-text {
            background: linear-gradient(to right, #2dd4bf, #3b82f6);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .bg-grid-pattern {
            background-image: linear-gradient(to right, rgba(255,255,255,0.05) 1px, transparent 1px),
                              linear-gradient(to bottom, rgba(255,255,255,0.05) 1px, transparent 1px);
            background-size: 40px 40px;
        }

        /* Scroll reveal classes */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease-out;
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }
        
        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0f172a; 
        }
        ::-webkit-scrollbar-thumb {
            background: #334155; 
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #475569; 
        }
    </style>
</head>
<body class="antialiased relative overflow-x-hidden selection:bg-brand-500 selection:text-white">

    <!-- Background Decoration -->
    <div class="fixed inset-0 z-[-1] bg-grid-pattern"></div>
    <div class="fixed top-[-20%] left-[-10%] w-[50%] h-[50%] rounded-full bg-brand-500/10 blur-[120px] z-[-1] pointer-events-none"></div>
    <div class="fixed bottom-[-20%] right-[-10%] w-[50%] h-[50%] rounded-full bg-blue-500/10 blur-[120px] z-[-1] pointer-events-none"></div>

    <header class="fixed w-full top-0 z-50 glass-nav transition-all duration-300" id="navbar">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <!-- Logo -->
                <div class="flex-shrink-0 flex items-center gap-2 cursor-pointer" onclick="window.scrollTo(0,0)">
                    <div class="w-10 h-10 rounded-xl bg-gradient-to-br from-brand-400 to-blue-500 flex items-center justify-center font-display font-bold text-xl text-white shadow-lg">
                        AI
                    </div>
                    <span class="font-display font-bold text-xl tracking-tight hidden sm:block">DevPortfolio</span>
                </div>

                <!-- Desktop Menu -->
                <nav class="hidden md:flex space-x-8">
                    <a href="#about" class="text-slate-300 hover:text-brand-400 font-medium transition-colors text-sm uppercase tracking-wider">About</a>
                    <a href="#skills" class="text-slate-300 hover:text-brand-400 font-medium transition-colors text-sm uppercase tracking-wider">Skills</a>
                    <a href="#experience" class="text-slate-300 hover:text-brand-400 font-medium transition-colors text-sm uppercase tracking-wider">Experience</a>
                    <a href="#apps" class="text-slate-300 hover:text-brand-400 font-medium transition-colors text-sm uppercase tracking-wider">My Apps</a>
                    <a href="#contact" class="text-slate-300 hover:text-brand-400 font-medium transition-colors text-sm uppercase tracking-wider">Contact</a>
                </nav>

                <!-- CTA Button -->
                <div class="hidden md:flex">
                    <a href="#contact" class="px-5 py-2.5 rounded-full bg-white/10 hover:bg-white/20 border border-white/10 text-white font-medium transition-all duration-300 hover:shadow-[0_0_15px_rgba(45,212,191,0.3)] flex items-center gap-2">
                        <span>Hire Me</span>
                        <i class="fa-solid fa-arrow-right text-sm"></i>
                    </a>
                </div>

                <!-- Mobile menu button -->
                <div class="md:hidden flex items-center">
                    <button id="mobile-menu-btn" class="text-slate-300 hover:text-white focus:outline-none p-2">
                        <i class="fa-solid fa-bars text-2xl"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden glass-nav border-t border-white/10">
            <div class="px-2 pt-2 pb-6 space-y-1 sm:px-3 flex flex-col items-center">
                <a href="#about" class="mobile-link block px-3 py-3 text-base font-medium text-slate-300 hover:text-brand-400 w-full text-center">About</a>
                <a href="#skills" class="mobile-link block px-3 py-3 text-base font-medium text-slate-300 hover:text-brand-400 w-full text-center">Skills</a>
                <a href="#experience" class="mobile-link block px-3 py-3 text-base font-medium text-slate-300 hover:text-brand-400 w-full text-center">Experience</a>
                <a href="#apps" class="mobile-link block px-3 py-3 text-base font-medium text-slate-300 hover:text-brand-400 w-full text-center">My Apps</a>
                <a href="#contact" class="mobile-link block px-3 py-3 text-base font-medium text-slate-300 hover:text-brand-400 w-full text-center">Contact</a>
                <a href="#contact" class="mt-4 px-6 py-2 rounded-full bg-brand-500 text-white font-medium w-3/4 text-center">Hire Me</a>
            </div>
        </div>
    </header>

    <main>
        <section id="hero" class="relative min-h-screen flex items-center pt-20 pb-12 sm:pt-24 lg:pt-32 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-8 items-center w-full">
                
                <!-- Text Content -->
                <div class="order-2 lg:order-1 text-center lg:text-left z-10 reveal">
                    <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-brand-500/10 border border-brand-500/20 text-brand-400 text-sm font-medium mb-6">
                        <span class="relative flex h-2 w-2">
                          <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-brand-400 opacity-75"></span>
                          <span class="relative inline-flex rounded-full h-2 w-2 bg-brand-500"></span>
                        </span>
                        Available for freelance
                    </div>
                    
                    <h1 class="text-4xl sm:text-5xl lg:text-6xl font-display font-bold leading-tight mb-4">
                        Hi, I'm <span class="text-white">Madhusudan Payra</span>.<br>
                        I build <span class="gradient-text">Smart Android Apps</span> with AI.
                    </h1>
                    
                    <p class="text-lg sm:text-xl text-slate-400 mb-8 max-w-2xl mx-auto lg:mx-0">
                        Bridging the gap between cutting-edge technology and seamless mobile experiences. Specialized in Android Studio, Firebase, and Antigravity to turn complex algorithms into pocket-sized solutions.
                    </p>
                    
                    <div class="flex flex-col sm:flex-row gap-4 justify-center lg:justify-start">
                        <a href="#apps" class="px-8 py-3.5 rounded-full bg-gradient-to-r from-brand-600 to-brand-500 hover:from-brand-500 hover:to-brand-400 text-white font-medium text-lg transition-all duration-300 shadow-[0_0_20px_rgba(20,184,166,0.4)] hover:shadow-[0_0_30px_rgba(20,184,166,0.6)] flex items-center justify-center gap-2">
                            View My Apps <i class="fa-solid fa-mobile-screen"></i>
                        </a>
                        <a href="https://github.com/bullat859" target="_blank" rel="noopener noreferrer" class="px-8 py-3.5 rounded-full bg-transparent border border-slate-600 hover:border-slate-400 text-slate-300 hover:text-white font-medium text-lg transition-colors flex items-center justify-center gap-2">
                            <i class="fa-brands fa-github text-xl"></i> GitHub Profile
                        </a>
                    </div>
                    
                    <!-- Quick Stats -->
                    <div class="mt-12 grid grid-cols-3 gap-4 border-t border-slate-800 pt-8 max-w-lg mx-auto lg:mx-0">
                        <div>
                            <h3 class="text-3xl font-display font-bold text-white">2</h3>
                            <p class="text-sm text-slate-400">Years Exp.</p>
                        </div>
                        <div>
                            <h3 class="text-3xl font-display font-bold text-white">1</h3>
                            <p class="text-sm text-slate-400">App Published</p>
                        </div>
                        <div>
                            <h3 class="text-3xl font-display font-bold text-white">4+</h3>
                            <p class="text-sm text-slate-400">Core Tools</p>
                        </div>
                    </div>
                </div>
                
                <!-- Hero Image / Visual -->
                <div class="order-1 lg:order-2 flex justify-center relative z-10 reveal">
                    <div class="relative w-64 h-64 sm:w-80 sm:h-80 md:w-96 md:h-96">
                        <!-- Decorative circles -->
                        <div class="absolute inset-0 rounded-full border border-slate-700 animate-pulse-slow"></div>
                        <div class="absolute inset-4 rounded-full border border-slate-600"></div>
                        <div class="absolute inset-8 rounded-full border border-brand-500/30"></div>
                        
                        <!-- Floating Badges -->
                        <div class="absolute top-4 -right-4 bg-slate-800 border border-slate-700 p-3 rounded-2xl shadow-xl animate-float" style="animation-delay: 0s;">
                            <i class="fa-brands fa-android text-4xl text-green-500"></i>
                        </div>
                        <div class="absolute bottom-12 -left-8 bg-slate-800 border border-slate-700 p-3 rounded-2xl shadow-xl animate-float" style="animation-delay: 2s;">
                            <i class="fa-solid fa-brain text-4xl text-purple-500"></i>
                        </div>
                        <div class="absolute -bottom-4 right-8 bg-slate-800 border border-slate-700 p-3 rounded-2xl shadow-xl animate-float" style="animation-delay: 1s;">
                            <img src="https://upload.wikimedia.org/wikipedia/commons/2/2d/Tensorflow_logo.svg" alt="TF" class="w-10 h-10 object-contain">
                        </div>

                        <!-- Main Photo Profile -->
                        <div class="absolute inset-4 rounded-full overflow-hidden border-4 border-slate-800 shadow-2xl bg-slate-800">
                            <!-- Replace with your actual photo URL -->
                            <img src="https://placehold.co/400x400/1e293b/cbd5e1?text=Your+Photo" alt="Developer Photo" class="w-full h-full object-cover">
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="experience" class="py-24 relative bg-slate-900/40">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-16 reveal">
                    <h2 class="text-3xl md:text-4xl font-display font-bold mb-4">Professional <span class="gradient-text">Journey</span></h2>
                    <p class="text-slate-400 max-w-2xl mx-auto">My track record of building, optimizing, and scaling intelligent mobile applications.</p>
                    <div class="h-1 w-20 bg-brand-500 mx-auto rounded-full mt-6"></div>
                </div>

                <div class="relative max-w-4xl mx-auto reveal">
                    <!-- Vertical Line -->
                    <div class="absolute left-4 md:left-1/2 transform md:-translate-x-1/2 top-0 bottom-0 w-px bg-gradient-to-b from-brand-500 via-blue-500 to-transparent opacity-30"></div>
                    
                    <!-- Timeline Item 1 -->
                    <div class="relative flex flex-col md:flex-row items-start mb-16 group">
                        <div class="hidden md:flex flex-1 justify-end pr-10 text-right">
                            <div>
                                <h3 class="text-xl font-bold text-white group-hover:text-brand-400 transition-colors">Android Developer</h3>
                                <p class="text-slate-400">Independent / App Development</p>
                                <span class="inline-block mt-2 px-3 py-1 bg-brand-500/10 text-brand-400 rounded-full text-sm border border-brand-500/20">2024 - 2026</span>
                            </div>
                        </div>
                        <div class="absolute left-[11px] md:left-1/2 transform md:-translate-x-1/2 w-4 h-4 rounded-full bg-slate-900 border-2 border-brand-500 z-10 group-hover:bg-brand-500 transition-colors shadow-[0_0_10px_rgba(20,184,166,0.5)] mt-1.5 md:mt-0"></div>
                        
                        <div class="md:hidden mb-4 pl-12 w-full">
                            <h3 class="text-xl font-bold text-white">Android Developer</h3>
                            <p class="text-slate-400">Independent / App Development</p>
                            <span class="inline-block mt-2 px-3 py-1 bg-brand-500/10 text-brand-400 rounded-full text-sm border border-brand-500/20">2024 - 2026</span>
                        </div>

                        <div class="flex-1 pl-12 md:pl-10 w-full">
                            <div class="glass-card p-6 rounded-2xl relative">
                                <!-- Triangle pointer -->
                                <div class="hidden md:block absolute top-4 -left-3 w-0 h-0 border-t-[10px] border-t-transparent border-b-[10px] border-b-transparent border-r-[12px] border-r-[rgba(30,41,59,0.5)] backdrop-blur-md"></div>
                                <ul class="list-disc list-outside ml-4 text-slate-400 space-y-2 text-sm leading-relaxed">
                                    <li>Developed and published the Gesture Control app natively on the Google Play Store.</li>
                                    <li>Utilized Android Studio, Firebase, and Antigravity to build a robust and seamless mobile experience.</li>
                                    <li>Managed the full app lifecycle from conception to deployment via Google Play Console.</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="apps" class="py-24 relative">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-16 reveal">
                    <h2 class="text-3xl md:text-4xl font-display font-bold mb-4">Featured <span class="gradient-text">Applications</span></h2>
                    <p class="text-slate-400 max-w-2xl mx-auto">A showcase of mobile applications I've developed, focusing on clean architecture and intuitive interfaces.</p>
                    <div class="h-1 w-20 bg-brand-500 mx-auto rounded-full mt-6"></div>
                </div>

                <div class="flex justify-center">
                    
                    <!-- App Card 1 -->
                    <div class="glass-card rounded-3xl overflow-hidden reveal group flex flex-col h-full w-full max-w-md">
                        <div class="relative h-48 bg-slate-800 flex items-center justify-center overflow-hidden">
                            <!-- Background gradient for visual appeal -->
                            <div class="absolute inset-0 bg-gradient-to-br from-blue-900/50 to-purple-900/50 group-hover:scale-110 transition-transform duration-500"></div>
                            <!-- Mockup representation -->
                            <div class="relative w-24 h-48 bg-slate-900 rounded-t-xl border-t-[6px] border-x-[6px] border-slate-700 flex flex-col translate-y-4">
                                <div class="w-8 h-1 bg-slate-800 mx-auto rounded-b-lg mb-2"></div>
                                <div class="flex-1 bg-[url('https://placehold.co/200x400/2dd4bf/ffffff?text=App+UI')] bg-cover bg-center rounded-sm mx-1"></div>
                            </div>
                            <div class="absolute top-4 right-4 bg-black/50 backdrop-blur-md text-white text-xs px-2 py-1 rounded">On Play Store</div>
                        </div>
                        <div class="p-6 flex-1 flex flex-col">
                            <div class="flex items-center gap-3 mb-3">
                                <div class="w-10 h-10 rounded-xl bg-gradient-to-br from-cyan-400 to-blue-500 p-2 shadow-lg flex items-center justify-center">
                                    <i class="fa-solid fa-hand-sparkles text-white"></i>
                                </div>
                                <h3 class="text-xl font-bold text-white">Gesture Control App</h3>
                            </div>
                            <p class="text-slate-400 text-sm mb-4 flex-1">
                                An innovative Android application allowing users to control their devices seamlessly using custom gestures. Built from scratch and actively maintained.
                            </p>
                            <div class="flex flex-wrap gap-2 mb-6 justify-center">
                                <span class="text-xs text-brand-300 bg-brand-900/30 px-2 py-1 rounded">Android Studio</span>
                                <span class="text-xs text-brand-300 bg-brand-900/30 px-2 py-1 rounded">Firebase</span>
                                <span class="text-xs text-brand-300 bg-brand-900/30 px-2 py-1 rounded">Antigravity</span>
                            </div>
                            <a href="https://play.google.com/store/apps/details?id=com.m.payra.gesture.control.app" target="_blank" rel="noopener noreferrer" class="w-full py-2.5 rounded-xl bg-white/5 hover:bg-white/10 border border-white/10 text-center text-sm font-medium transition-colors flex items-center justify-center gap-2">
                                <i class="fa-brands fa-google-play"></i> View on Play Store
                            </a>
                        </div>
                    </div>

                </div>
                
                <div class="mt-12 text-center reveal">
                    <a href="https://github.com/bullat859" target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-2 text-slate-300 hover:text-brand-400 transition-colors">
                        View more on Github <i class="fa-solid fa-arrow-right-long"></i>
                    </a>
                </div>
            </div>
        </section>

        <section id="contact" class="py-24 relative border-t border-slate-800/50 bg-slate-900/30">
            <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="glass-card rounded-3xl p-8 sm:p-12 reveal">
                    <div class="text-center mb-10">
                        <h2 class="text-3xl md:text-4xl font-display font-bold mb-4">Let's Build <span class="gradient-text">Something Smart</span></h2>
                        <p class="text-slate-400">Have an app idea? Need an AI feature integrated into your existing Android project? Drop me a message.</p>
                    </div>

                    <form onsubmit="handleFormSubmit(event)" class="space-y-6">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                            <div class="space-y-2">
                                <label for="name" class="text-sm font-medium text-slate-300">Name</label>
                                <input type="text" id="name" required class="w-full bg-slate-950/50 border border-slate-700 rounded-xl px-4 py-3 text-white placeholder-slate-500 focus:outline-none focus:border-brand-500 focus:ring-1 focus:ring-brand-500 transition-colors" placeholder="John Doe">
                            </div>
                            <div class="space-y-2">
                                <label for="email" class="text-sm font-medium text-slate-300">Email</label>
                                <input type="email" id="email" required class="w-full bg-slate-950/50 border border-slate-700 rounded-xl px-4 py-3 text-white placeholder-slate-500 focus:outline-none focus:border-brand-500 focus:ring-1 focus:ring-brand-500 transition-colors" placeholder="john@example.com">
                            </div>
                        </div>
                        <div class="space-y-2">
                            <label for="message" class="text-sm font-medium text-slate-300">Message</label>
                            <textarea id="message" rows="4" required class="w-full bg-slate-950/50 border border-slate-700 rounded-xl px-4 py-3 text-white placeholder-slate-500 focus:outline-none focus:border-brand-500 focus:ring-1 focus:ring-brand-500 transition-colors resize-none" placeholder="Tell me about your project..."></textarea>
                        </div>
                        <button type="submit" class="w-full py-4 rounded-xl bg-gradient-to-r from-brand-600 to-brand-500 hover:from-brand-500 hover:to-brand-400 text-white font-bold text-lg transition-all duration-300 shadow-[0_0_15px_rgba(20,184,166,0.3)]">
                            Send Message <i class="fa-solid fa-paper-plane ml-2"></i>
                        </button>
                        
                        <!-- Success Message Container -->
                        <div id="form-success" class="hidden mt-4 p-4 rounded-xl bg-emerald-500/10 border border-emerald-500/20 text-emerald-400 text-center text-sm">
                            Message sent successfully! I'll get back to you soon.
                        </div>
                    </form>
                </div>
            </div>
        </section>
    </main>

    <footer class="bg-slate-950 border-t border-slate-800 py-12 text-center">
        <div class="max-w-7xl mx-auto px-4 flex flex-col items-center">
            <div class="w-10 h-10 rounded-xl bg-gradient-to-br from-brand-400 to-blue-500 flex items-center justify-center font-display font-bold text-xl text-white shadow-lg mb-6 grayscale hover:grayscale-0 transition-all duration-300">
                AI
            </div>
            <div class="flex gap-6 mb-8">
                <a href="https://github.com/bullat859" target="_blank" rel="noopener noreferrer" class="w-10 h-10 rounded-full bg-slate-800 flex items-center justify-center text-slate-400 hover:bg-brand-500 hover:text-white transition-all duration-300">
                    <i class="fa-brands fa-github text-xl"></i>
                </a>
                <a href="#" class="w-10 h-10 rounded-full bg-slate-800 flex items-center justify-center text-slate-400 hover:bg-[#0A66C2] hover:text-white transition-all duration-300">
                    <i class="fa-brands fa-linkedin-in text-xl"></i>
                </a>
                <a href="#" class="w-10 h-10 rounded-full bg-slate-800 flex items-center justify-center text-slate-400 hover:bg-[#1DA1F2] hover:text-white transition-all duration-300">
                    <i class="fa-brands fa-twitter text-xl"></i>
                </a>
                <a href="#" class="w-10 h-10 rounded-full bg-slate-800 flex items-center justify-center text-slate-400 hover:bg-brand-500 hover:text-white transition-all duration-300">
                    <i class="fa-brands fa-google-play text-xl"></i>
                </a>
            </div>
            <p class="text-slate-500 text-sm">
                &copy; <span id="year"></span> AI DevPortfolio. Designed for modern Android developers. All rights reserved.
            </p>
        </div>
    </footer>

    <!-- Floating AI Chatbot Widget -->
    <div class="fixed bottom-6 right-6 z-50 flex flex-col items-end">
        <!-- Chat Window -->
        <div id="chat-window" class="hidden mb-4 w-72 sm:w-80 glass-card border border-brand-500/30 rounded-2xl overflow-hidden shadow-2xl transform origin-bottom-right transition-all duration-300 scale-95 opacity-0">
            <div class="bg-gradient-to-r from-brand-600 to-blue-600 p-4 flex justify-between items-center shadow-md">
                <div class="flex items-center gap-2 text-white">
                    <i class="fa-solid fa-robot text-lg"></i>
                    <span class="font-bold font-display text-sm">Madhusudan's Assistant</span>
                </div>
                <button id="close-chat" class="text-white/80 hover:text-white focus:outline-none transition-colors">
                    <i class="fa-solid fa-xmark text-lg"></i>
                </button>
            </div>
            
            <div id="chat-messages" class="p-4 h-64 overflow-y-auto flex flex-col gap-3 bg-slate-900/90 custom-scrollbar">
                <!-- Initial Bot Message -->
                <div class="bg-slate-800 border border-slate-700 text-slate-200 text-sm p-3 rounded-xl rounded-tl-none self-start max-w-[85%] shadow-sm">
                    Hi! 👋 I'm an AI assistant built to help you navigate this portfolio. Ask me about Madhusudan's <strong>skills</strong>, <strong>experience</strong>, or how to <strong>contact</strong> him!
                </div>
            </div>
            
            <div class="p-3 bg-slate-900 border-t border-slate-800 flex gap-2">
                <input type="text" id="chat-input" class="flex-1 bg-slate-950 border border-slate-700 rounded-xl px-3 py-2 text-sm text-white focus:outline-none focus:border-brand-500 focus:ring-1 focus:ring-brand-500 transition-all placeholder-slate-500" placeholder="Type a message...">
                <button id="send-chat" class="bg-gradient-to-r from-brand-600 to-brand-500 hover:from-brand-500 hover:to-brand-400 text-white w-10 h-10 rounded-xl flex items-center justify-center transition-colors shadow-lg">
                    <i class="fa-solid fa-paper-plane text-sm ml-[-2px]"></i>
                </button>
            </div>
        </div>
        
        <!-- Chat Toggle Button -->
        <button id="chat-toggle" class="w-14 h-14 rounded-full bg-gradient-to-br from-brand-500 to-blue-600 text-white shadow-[0_0_20px_rgba(20,184,166,0.4)] hover:shadow-[0_0_30px_rgba(20,184,166,0.6)] flex items-center justify-center transition-all duration-300 hover:scale-110 group relative z-50">
            <i class="fa-solid fa-message text-xl group-hover:hidden transition-opacity"></i>
            <i class="fa-solid fa-robot text-2xl hidden group-hover:block transition-opacity"></i>
            
            <!-- Notification ping -->
            <span class="absolute top-0 right-0 flex h-3.5 w-3.5">
              <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-red-400 opacity-75"></span>
              <span class="relative inline-flex rounded-full h-3.5 w-3.5 bg-red-500 border-2 border-slate-900"></span>
            </span>
        </button>
    </div>

    <script>
        // Set current year
        document.getElementById('year').textContent = new Date().getFullYear();

        // Mobile Menu Toggle
        const btn = document.getElementById('mobile-menu-btn');
        const menu = document.getElementById('mobile-menu');
        const mobileLinks = document.querySelectorAll('.mobile-link');

        btn.addEventListener('click', () => {
            menu.classList.toggle('hidden');
        });

        // Close mobile menu when clicking a link
        mobileLinks.forEach(link => {
            link.addEventListener('click', () => {
                menu.classList.add('hidden');
            });
        });

        // Navbar blur effect on scroll
        const navbar = document.getElementById('navbar');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 20) {
                navbar.classList.add('shadow-lg');
                navbar.style.background = 'rgba(15, 23, 42, 0.9)';
            } else {
                navbar.classList.remove('shadow-lg');
                navbar.style.background = 'rgba(15, 23, 42, 0.8)';
            }
        });

        // Scroll Reveal Animation
        function reveal() {
            var reveals = document.querySelectorAll(".reveal");
            for (var i = 0; i < reveals.length; i++) {
                var windowHeight = window.innerHeight;
                var elementTop = reveals[i].getBoundingClientRect().top;
                var elementVisible = 100;
                if (elementTop < windowHeight - elementVisible) {
                    reveals[i].classList.add("active");
                }
            }
        }
        window.addEventListener("scroll", reveal);
        // Trigger once on load
        reveal();

        // Form submission handler (Visual only, no actual backend)
        function handleFormSubmit(e) {
            e.preventDefault();
            const btn = e.target.querySelector('button[type="submit"]');
            const originalText = btn.innerHTML;
            
            // Loading state
            btn.innerHTML = '<i class="fa-solid fa-circle-notch fa-spin"></i> Sending...';
            btn.disabled = true;
            btn.classList.add('opacity-75');
            
            // Simulate network request
            setTimeout(() => {
                btn.innerHTML = originalText;
                btn.disabled = false;
                btn.classList.remove('opacity-75');
                
                // Show success message
                document.getElementById('form-success').classList.remove('hidden');
                e.target.reset(); // clear form
                
                // Hide success message after 5 seconds
                setTimeout(() => {
                    document.getElementById('form-success').classList.add('hidden');
                }, 5000);
                
            }, 1500);
        }
    </script>
</body>
</html>
