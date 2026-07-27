<html lang="en" class="dark scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0">
    <title>Privacy Policy - Dynamic Edge Gesture Control</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Plus Jakarta Sans', 'sans-serif'],
                    },
                    colors: {
                        brand: {
                            50: '#eff6ff',
                            100: '#dbeafe',
                            400: '#60a5fa',
                            500: '#3b82f6',
                            600: '#2563eb',
                            700: '#1d4ed8',
                        }
                    }
                }
            }
        }
    </script>
    <style>
        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: #030712;
            /* Changed from hidden to clip to guarantee position:sticky works flawlessly on all mobile devices */
            overflow-x: clip; 
        }
        .glass-panel {
            background: rgba(17, 24, 39, 0.75);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }
        .glass-card {
            background: rgba(30, 41, 59, 0.35);
            border: 1px solid rgba(255, 255, 255, 0.05);
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .glass-card:hover {
            border-color: rgba(59, 130, 246, 0.35);
            background: rgba(30, 41, 59, 0.65);
            box-shadow: 0 12px 30px -10px rgba(59, 130, 246, 0.15);
        }
        .glow-bg {
            position: fixed;
            width: 100vw;
            height: 100vh;
            top: 0;
            left: 0;
            pointer-events: none;
            z-index: -1;
            background: 
                radial-gradient(circle at 15% 15%, rgba(59, 130, 246, 0.12) 0%, transparent 40%),
                radial-gradient(circle at 85% 75%, rgba(139, 92, 246, 0.12) 0%, transparent 40%),
                radial-gradient(circle at 50% 50%, rgba(3, 7, 18, 1) 0%, rgba(3, 7, 18, 1) 100%);
        }
        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 6px;
            height: 6px;
        }
        ::-webkit-scrollbar-track {
            background: #030712;
        }
        ::-webkit-scrollbar-thumb {
            background: #1e293b;
            border-radius: 9999px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #3b82f6;
        }
        
        /* Hide scrollbar for quick links but allow scrolling */
        .hide-scrollbar::-webkit-scrollbar {
            display: none;
        }
        .hide-scrollbar {
            -ms-overflow-style: none;
            scrollbar-width: none;
        }
    </style>
</head>
<body class="bg-slate-950 text-slate-100 min-h-screen selection:bg-blue-500 selection:text-white relative antialiased">
    
    <!-- Reading Progress Bar -->
    <div class="fixed top-0 left-0 w-full h-1 z-50 bg-slate-900">
        <div id="progressBar" class="h-full bg-gradient-to-r from-blue-400 via-indigo-500 to-amber-500 w-0 transition-all duration-150 ease-out"></div>
    </div>

    <div class="glow-bg"></div>

    <!-- COMPACT & WIDE STICKY NAVBAR -->
    <div class="sticky top-0 z-40 w-full mb-6 sm:mb-8 pt-1 sm:pt-2 px-2 sm:px-4 lg:px-6 max-w-[98%] md:max-w-6xl xl:max-w-7xl mx-auto">
        <div class="glass-panel px-3 sm:px-6 py-2.5 sm:py-3 rounded-2xl sm:rounded-full shadow-lg shadow-black/60 flex flex-row items-center justify-center gap-3 border border-slate-700/50 transition-all w-full">
            
            <!-- App Logo & Name -->
            <div class="flex items-center justify-center gap-2.5 sm:gap-3 w-full">
                <div class="w-7 h-7 sm:w-8 sm:h-8 rounded-lg overflow-hidden shadow-sm shadow-blue-500/20 shrink-0 border border-white/10">
                    <svg viewBox="0 0 100 100" class="w-full h-full" xmlns="http://www.w3.org/2000/svg">
                        <defs>
                            <linearGradient id="bgGradHero" x1="0%" y1="0%" x2="100%" y2="100%">
                                <stop offset="0%" stop-color="#4c1d95"/>
                                <stop offset="50%" stop-color="#1e1b4b"/>
                                <stop offset="100%" stop-color="#b45309"/>
                            </linearGradient>
                            <linearGradient id="neonGradHero" x1="0%" y1="0%" x2="100%" y2="100%">
                                <stop offset="0%" stop-color="#38bdf8"/>
                                <stop offset="50%" stop-color="#a855f7"/>
                                <stop offset="100%" stop-color="#f97316"/>
                            </linearGradient>
                        </defs>
                        <rect width="100" height="100" fill="url(#bgGradHero)"/>
                        <path d="M 20 22 C 20 18 24 14 28 14 L 38 14 C 40 14 42 16 43 18 L 45 22 C 46 24 48 25 50 25 C 52 25 54 24 55 22 L 57 18 C 58 16 60 14 62 14 L 72 14 C 76 14 80 18 80 22 L 80 78 C 80 82 76 86 72 86 L 28 86 C 24 86 20 82 20 78 Z" fill="none" stroke="url(#neonGradHero)" stroke-width="3.5" stroke-linecap="round" stroke-linejoin="round"/>
                        <circle cx="47" cy="18" r="2" fill="#38bdf8"/>
                        <circle cx="53" cy="18" r="1.5" fill="#a855f7"/>
                        <path d="M 28 42 C 28 68 45 74 52 56 C 54 50 50 42 45 42 C 40 42 38 48 42 54" fill="none" stroke="#38bdf8" stroke-width="4" stroke-linecap="round"/>
                        <path d="M 62 30 A 28 28 0 0 1 78 44 L 70 47 A 18 18 0 0 0 59 37 Z" fill="#f97316" opacity="0.9"/>
                        <path d="M 79 47 A 28 28 0 0 1 79 63 L 71 60 A 18 18 0 0 0 71 50 Z" fill="#fb923c" opacity="0.9"/>
                        <path d="M 77 66 A 28 28 0 0 1 63 78 L 58 70 A 18 18 0 0 0 68 61 Z" fill="#ef4444" opacity="0.9"/>
                        <circle cx="50" cy="50" r="4" fill="#ffffff"/>
                        <path d="M 50 43 L 50 57 M 43 50 L 57 50 M 45 45 L 55 55 M 45 55 L 55 45" stroke="#ffffff" stroke-width="2" stroke-linecap="round"/>
                    </svg>
                </div>
                <!-- Full name centered and always in one horizontal line -->
                <span class="text-[13px] sm:text-[16px] font-bold text-slate-100 truncate whitespace-nowrap">
                    Dynamic Edge Gesture Control
                </span>
            </div>
        </div>
    </div>

    <!-- Main Content Container -->
    <div class="max-w-4xl mx-auto px-3 sm:px-6 lg:px-8 pb-8 sm:pb-16 relative">
        
        <!-- Big Hero Title (Non-Sticky, Scrolls away normally) -->
        <div class="text-center mb-8 sm:mb-12 mt-2 sm:mt-6">
            <h1 class="text-3xl sm:text-5xl md:text-6xl font-extrabold tracking-tight bg-gradient-to-r from-white via-slate-200 to-blue-400 bg-clip-text text-transparent mb-4 leading-tight">
                Privacy Policy
            </h1>
            <p class="text-slate-400 text-sm sm:text-base max-w-2xl mx-auto mb-6">
                Complete transparency regarding how we handle your data, permissions, and local features.
            </p>

            <!-- Google Play Store Button -->
            <div class="flex justify-center">
                <a href="https://play.google.com/store/apps/details?id=com.m.payra.gesture.control.app" target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-2.5 px-4 sm:px-5 py-2.5 rounded-xl bg-slate-900 border border-slate-700 hover:border-blue-500/50 text-slate-200 text-xs sm:text-sm font-semibold transition-all hover:bg-slate-800 shadow-md transform hover:-translate-y-0.5">
                    <svg class="w-4 h-4 sm:w-5 sm:h-5 text-emerald-400 shrink-0" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M3,20.5V3.5C3,2.91 3.34,2.39 3.84,2.15L13.69,12L3.84,21.85C3.34,21.6 3,21.09 3,20.5M16.81,15.12L18.81,13.12C19.86,12.55 19.86,11.45 18.81,10.88L16.81,8.88L14.81,10.88L14.81,13.12L16.81,15.12M13.69,12L15.39,8.81L13.69,12M13.69,12L15.39,15.19L3.84,21.85L13.69,12Z"/>
                    </svg>
                    <span>Get it on Google Play</span>
                    <svg class="w-3 h-3 sm:w-3.5 sm:h-3.5 text-slate-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"/></svg>
                </a>
            </div>
        </div>

        <!-- Quick Policy Highlights Grid -->
        <section id="overview" class="grid grid-cols-1 sm:grid-cols-2 gap-3.5 sm:gap-4 mb-8 sm:mb-10">
            <div class="glass-panel p-4 sm:p-5 rounded-2xl border border-slate-800">
                <div class="w-9 h-9 sm:w-10 sm:h-10 rounded-xl bg-blue-500/10 text-blue-400 flex items-center justify-center text-lg sm:text-xl mb-2.5 sm:mb-3 border border-blue-500/20">
                    🛡️
                </div>
                <h3 class="text-sm sm:text-base font-semibold text-slate-100 mb-1">Analytics vs. Personal Data</h3>
                <p class="text-slate-400 text-xs leading-relaxed">We collect essential usage and crash analytics to improve our app. However, your personal photos, videos, audio recordings, and custom notes are stored locally and are never uploaded to our servers.</p>
            </div>

            <div class="glass-panel p-4 sm:p-5 rounded-2xl border border-slate-800">
                <div class="w-9 h-9 sm:w-10 sm:h-10 rounded-xl bg-amber-500/10 text-amber-400 flex items-center justify-center text-lg sm:text-xl mb-2.5 sm:mb-3 border border-amber-500/20">
                    🔥
                </div>
                <h3 class="text-sm sm:text-base font-semibold text-slate-100 mb-1">Firebase & AdMob Integration</h3>
                <p class="text-slate-400 text-xs leading-relaxed">Firebase securely handles our diagnostic crash reporting, while Google AdMob serves optional rewarded ad features.</p>
            </div>
        </section>

        <!-- SECONDARY STICKY HEADER: Search Bar & Navigation Filter -->
        <!-- Sticks directly underneath the main header when scrolling -->
        <div class="sticky top-[58px] sm:top-[76px] z-30 pt-2 pb-3 mb-8 sm:mb-10 bg-[#030712]/90 backdrop-blur-xl border-b border-white/5 shadow-lg shadow-black/20 mx-[-12px] px-[12px] sm:mx-0 sm:px-4 sm:rounded-2xl transition-all">
            <div class="glass-panel p-2.5 sm:p-3 rounded-2xl flex items-center gap-2.5 mb-2.5">
                <svg class="w-4 h-4 sm:w-5 sm:h-5 text-slate-400 ml-1.5 shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"/></svg>
                <input type="text" id="policySearch" onkeyup="filterSections()" placeholder="Search terms (e.g. Notifications, Notes, Camera)..." class="w-full bg-transparent text-xs sm:text-sm text-slate-200 placeholder-slate-500 focus:outline-none py-1">
            </div>
            
            <!-- Quick Links -->
            <div class="flex overflow-x-auto hide-scrollbar gap-2 pb-1">
                <a href="#intro" class="whitespace-nowrap px-3 py-1.5 rounded-lg bg-slate-800/50 border border-slate-700 text-xs text-slate-300 hover:bg-blue-500/20 hover:text-blue-300 hover:border-blue-500/30 transition-colors">Intro</a>
                <a href="#permissions" class="whitespace-nowrap px-3 py-1.5 rounded-lg bg-slate-800/50 border border-slate-700 text-xs text-slate-300 hover:bg-blue-500/20 hover:text-blue-300 hover:border-blue-500/30 transition-colors">Permissions</a>
                <a href="#firebase" class="whitespace-nowrap px-3 py-1.5 rounded-lg bg-slate-800/50 border border-slate-700 text-xs text-slate-300 hover:bg-amber-500/20 hover:text-amber-300 hover:border-amber-500/30 transition-colors">Firebase</a>
                <a href="#admob" class="whitespace-nowrap px-3 py-1.5 rounded-lg bg-slate-800/50 border border-slate-700 text-xs text-slate-300 hover:bg-blue-500/20 hover:text-blue-300 hover:border-blue-500/30 transition-colors">AdMob</a>
                <a href="#security" class="whitespace-nowrap px-3 py-1.5 rounded-lg bg-slate-800/50 border border-slate-700 text-xs text-slate-300 hover:bg-blue-500/20 hover:text-blue-300 hover:border-blue-500/30 transition-colors">Security</a>
                <a href="#contact" class="whitespace-nowrap px-3 py-1.5 rounded-lg bg-slate-800/50 border border-slate-700 text-xs text-slate-300 hover:bg-blue-500/20 hover:text-blue-300 hover:border-blue-500/30 transition-colors">Contact</a>
            </div>
        </div>

        <!-- Main Document Body -->
        <main class="space-y-6 sm:space-y-8">

            <!-- Section 1: Introduction -->
            <!-- Adjusted padding to offset the sticky headers gracefully -->
            <section id="intro" class="policy-section glass-panel rounded-2xl sm:rounded-3xl p-5 sm:p-8 md:p-10 shadow-xl relative overflow-hidden pt-20 sm:pt-24 mt-[-4rem] sm:mt-[-5rem]">
                <div class="absolute top-0 left-0 w-1 sm:w-1.5 h-full bg-gradient-to-b from-blue-500 to-indigo-500"></div>
                <h2 class="text-lg sm:text-2xl font-bold text-slate-100 mb-3 sm:mb-4 flex items-center gap-2.5">
                    <span class="text-blue-400 text-xs sm:text-sm font-extrabold uppercase tracking-widest bg-blue-500/10 px-2 py-0.5 sm:py-1 rounded-md border border-blue-500/20">01</span>
                    Introduction & Architecture
                </h2>
                <div class="space-y-3 sm:space-y-4 text-slate-300 text-sm sm:text-base leading-relaxed">
                    <p>
                        Welcome to <strong>Dynamic Edge Gesture Control</strong>. We value your trust and are committed to complete transparency regarding our data processing practices.
                    </p>
                    <p>
                        Our application provides deep system customization and gesture automation. While primary gesture detection, touch listening, and screen overlays function offline directly on your device, our app does connect to secure cloud services (specifically Google Firebase). We use these services to collect essential usage telemetry, diagnose software crashes, and monitor app performance. We also use Google AdMob to serve rewarded video ads.
                    </p>
                    <p class="text-xs sm:text-sm bg-slate-900/80 border border-slate-800 p-3.5 sm:p-4 rounded-xl text-slate-400">
                        By installing, accessing, or using Dynamic Edge Gesture Control, you acknowledge and agree to the data collection and usage practices described in this Privacy Policy.
                    </p>
                </div>
            </section>

            <!-- Section 2: Android Permissions Required -->
            <section id="permissions" class="policy-section glass-panel rounded-2xl sm:rounded-3xl p-5 sm:p-8 md:p-10 shadow-xl relative overflow-hidden pt-20 sm:pt-24 mt-[-4rem] sm:mt-[-5rem]">
                <div class="absolute top-0 left-0 w-1 sm:w-1.5 h-full bg-gradient-to-b from-blue-500 to-indigo-500"></div>
                <h2 class="text-lg sm:text-2xl font-bold text-slate-100 mb-3 sm:mb-4 flex items-center gap-2.5">
                    <span class="text-blue-400 text-xs sm:text-sm font-extrabold uppercase tracking-widest bg-blue-500/10 px-2 py-0.5 sm:py-1 rounded-md border border-blue-500/20">02</span>
                    Android Permissions & Local Features
                </h2>
                <p class="text-slate-300 text-sm sm:text-base leading-relaxed mb-6 sm:mb-8">
                    To deliver system-wide gesture controls, our app requests explicit permissions on your Android device. Each permission is used strictly for local automation and the features you trigger:
                </p>
                
                <div class="space-y-4 sm:space-y-6">
                    <!-- Accessibility Service -->
                    <div class="glass-card rounded-xl sm:rounded-2xl p-4 sm:p-6">
                        <div class="flex items-center justify-between mb-2.5 sm:mb-3 flex-wrap gap-2">
                            <h3 class="text-base sm:text-xl font-semibold text-blue-300 flex items-center gap-2">
                                <span class="p-1.5 rounded-lg bg-blue-500/10 border border-blue-500/20 text-blue-400 text-sm sm:text-base">🛠️</span>
                                Accessibility Service API
                            </h3>
                            <span class="text-[10px] sm:text-xs px-2 py-0.5 sm:py-1 rounded-full bg-red-500/10 text-red-400 border border-red-500/20 font-semibold">Core Required Permission</span>
                        </div>
                        <p class="text-slate-300 text-xs sm:text-base leading-relaxed mb-3">
                            The Accessibility Service API is the foundational engine of Dynamic Edge Gesture Control. It is strictly utilized to:
                        </p>
                        <ul class="space-y-2 my-3 text-slate-300 text-xs sm:text-sm list-none pl-0">
                            <li class="relative pl-5 before:absolute before:left-0 before:text-blue-400 before:content-['✦']">Draw touch-sensitive gesture overlay handles (edge sliders, notches, dynamic islands, and pie menus) on top of active screens.</li>
                            <li class="relative pl-5 before:absolute before:left-0 before:text-blue-400 before:content-['✦']">Detect your swipe, tap, long-press, and drag gestures specifically within these configured edge handle zones.</li>
                            <li class="relative pl-5 before:absolute before:left-0 before:text-blue-400 before:content-['✦']">Execute global Android system actions assigned to your gestures (e.g., Back, Home, Recent Apps, Quick Settings, Split Screen, and Power Menu).</li>
                        </ul>
                        <div class="bg-red-500/10 border-l-2 sm:border-l-4 border-red-500 p-3 sm:p-4 rounded-r-xl mt-3 text-red-200 text-xs sm:text-sm leading-relaxed">
                            <strong class="font-bold text-red-400 block mb-1">Strict Accessibility Privacy Guarantee:</strong>
                            We do NOT use the Accessibility Service API to read screen content, inspect keystrokes, intercept passwords, log personal messages, or track your interactions within other third-party apps.
                        </div>
                    </div>

                    <!-- Notifications -->
                    <div class="glass-card rounded-xl sm:rounded-2xl p-4 sm:p-6">
                        <h3 class="text-base sm:text-xl font-semibold text-blue-300 mb-2 sm:mb-3 flex items-center gap-2">
                            <span class="p-1.5 rounded-lg bg-blue-500/10 border border-blue-500/20 text-blue-400 text-sm sm:text-base">🔔</span>
                            Notifications
                        </h3>
                        <p class="text-slate-300 text-xs sm:text-base leading-relaxed">
                            Requested to run essential background foreground services. This ensures that the gesture engine continues to run reliably in the background without being killed by the Android system. It is also used to display media controls or quick settings directly in your notification panel.
                        </p>
                    </div>

                    <!-- Location -->
                    <div class="glass-card rounded-xl sm:rounded-2xl p-4 sm:p-6">
                        <h3 class="text-base sm:text-xl font-semibold text-blue-300 mb-2 sm:mb-3 flex items-center gap-2">
                            <span class="p-1.5 rounded-lg bg-blue-500/10 border border-blue-500/20 text-blue-400 text-sm sm:text-base">📍</span>
                            Location Access
                        </h3>
                        <p class="text-slate-300 text-xs sm:text-base leading-relaxed">
                            Used exclusively for <strong>Situational Location Triggers</strong>. If you opt to set up geofenced gestures, background location monitors when you enter or exit your chosen boundary. Coordinates are never sold or uploaded.
                        </p>
                    </div>
                    
                    <!-- Usage Access -->
                    <div class="glass-card rounded-xl sm:rounded-2xl p-4 sm:p-6">
                        <h3 class="text-base sm:text-xl font-semibold text-blue-300 mb-2 sm:mb-3 flex items-center gap-2">
                            <span class="p-1.5 rounded-lg bg-blue-500/10 border border-blue-500/20 text-blue-400 text-sm sm:text-base">📊</span>
                            Usage Access (Package Usage Stats)
                        </h3>
                        <p class="text-slate-300 text-xs sm:text-base leading-relaxed">
                            Allows the app to identify which foreground application is currently active. This enables "App-Specific Gesture Profiles," automatically hiding or switching gestures for specific apps.
                        </p>
                    </div>

                    <!-- Modify System Settings -->
                    <div class="glass-card rounded-xl sm:rounded-2xl p-4 sm:p-6">
                        <h3 class="text-base sm:text-xl font-semibold text-blue-300 mb-2 sm:mb-3 flex items-center gap-2">
                            <span class="p-1.5 rounded-lg bg-blue-500/10 border border-blue-500/20 text-blue-400 text-sm sm:text-base">⚙️</span>
                            Modify System Settings
                        </h3>
                        <p class="text-slate-300 text-xs sm:text-base leading-relaxed">
                            Empowers your gestures to directly toggle hardware and system parameters—such as Screen Brightness, Auto-Rotate lock, Volume levels, and Screen Timeout.
                        </p>
                    </div>

                    <!-- Storage, Music & Audio Access -->
                    <div class="glass-card rounded-xl sm:rounded-2xl p-4 sm:p-6">
                        <h3 class="text-base sm:text-xl font-semibold text-blue-300 mb-2 sm:mb-3 flex items-center gap-2">
                            <span class="p-1.5 rounded-lg bg-blue-500/10 border border-blue-500/20 text-blue-400 text-sm sm:text-base">🎵</span>
                            Music & Audio / Storage Access
                        </h3>
                        <p class="text-slate-300 text-xs sm:text-base leading-relaxed">
                            Required for local features such as the <strong>Offline Music Controller</strong>, playing media audio files, importing custom icons, and saving/restoring gesture backups.
                        </p>
                    </div>

                    <!-- Notes Feature -->
                    <div class="glass-card rounded-xl sm:rounded-2xl p-4 sm:p-6">
                        <h3 class="text-base sm:text-xl font-semibold text-blue-300 mb-2 sm:mb-3 flex items-center gap-2">
                            <span class="p-1.5 rounded-lg bg-blue-500/10 border border-blue-500/20 text-blue-400 text-sm sm:text-base">📝</span>
                            In-App Notes Feature
                        </h3>
                        <p class="text-slate-300 text-xs sm:text-base leading-relaxed mb-3">
                            Our application includes a local feature allowing you to create and save custom text notes for quick reference or task management.
                        </p>
                        <div class="bg-emerald-500/10 border-l-2 sm:border-l-4 border-emerald-500 p-3 sm:p-4 rounded-r-xl mt-3 text-emerald-200 text-xs sm:text-sm leading-relaxed">
                            <strong class="font-bold text-emerald-400 block mb-1">Total Privacy Guarantee:</strong>
                            Any text, notes, or personal information you type into the notes feature are <strong>stored strictly offline on your device</strong>. We do not read, collect, or transmit your note data to any external cloud server.
                        </div>
                    </div>

                    <!-- Camera (Silent Photo & Silent Video) -->
                    <div class="glass-card rounded-xl sm:rounded-2xl p-4 sm:p-6">
                        <h3 class="text-base sm:text-xl font-semibold text-blue-300 mb-2 sm:mb-3 flex items-center gap-2">
                            <span class="p-1.5 rounded-lg bg-blue-500/10 border border-blue-500/20 text-blue-400 text-sm sm:text-base">📸</span>
                            Camera (Silent Photo & Silent Video)
                        </h3>
                        <p class="text-slate-300 text-xs sm:text-base leading-relaxed mb-3">
                            Requested strictly on-demand when mapping gestures to toggle the device flashlight, or to utilize the app's <strong>silent photo and video recording</strong> functions.
                        </p>
                        <div class="bg-emerald-500/10 border-l-2 sm:border-l-4 border-emerald-500 p-3 sm:p-4 rounded-r-xl mt-3 text-emerald-200 text-xs sm:text-sm leading-relaxed">
                            <strong class="font-bold text-emerald-400 block mb-1">Total Privacy Guarantee:</strong>
                            All photos and videos captured using the silent recording feature are saved <strong>exclusively to your local device storage</strong>. We do not collect, upload, or transmit your personal media files to any cloud server.
                        </div>
                    </div>

                    <!-- Microphone (Audio Memos) -->
                    <div class="glass-card rounded-xl sm:rounded-2xl p-4 sm:p-6">
                        <h3 class="text-base sm:text-xl font-semibold text-blue-300 mb-2 sm:mb-3 flex items-center gap-2">
                            <span class="p-1.5 rounded-lg bg-blue-500/10 border border-blue-500/20 text-blue-400 text-sm sm:text-base">🎙️</span>
                            Microphone (Silent Audio & Video)
                        </h3>
                        <p class="text-slate-300 text-xs sm:text-base leading-relaxed mb-3">
                            Requested strictly on-demand when mapping gestures to record Audio Memos or capturing video with sound. The microphone is only activated when explicitly triggered by your gesture.
                        </p>
                        <div class="bg-emerald-500/10 border-l-2 sm:border-l-4 border-emerald-500 p-3 sm:p-4 rounded-r-xl mt-3 text-emerald-200 text-xs sm:text-sm leading-relaxed">
                            <strong class="font-bold text-emerald-400 block mb-1">Total Privacy Guarantee:</strong>
                            Similar to the camera functionality, all audio recordings are <strong>saved entirely on your device's local storage</strong>. We never collect or monitor your voice or background audio.
                        </div>
                    </div>

                    <!-- Nearby Devices (Bluetooth) -->
                    <div class="glass-card rounded-xl sm:rounded-2xl p-4 sm:p-6">
                        <h3 class="text-base sm:text-xl font-semibold text-blue-300 mb-2 sm:mb-3 flex items-center gap-2">
                            <span class="p-1.5 rounded-lg bg-blue-500/10 border border-blue-500/20 text-blue-400 text-sm sm:text-base">📶</span>
                            Nearby Devices (Bluetooth)
                        </h3>
                        <p class="text-slate-300 text-xs sm:text-base leading-relaxed">
                            Requested strictly on-demand when mapping gestures to toggle your device's Bluetooth connection state and search for or connect to nearby devices.
                        </p>
                    </div>

                    <!-- Contacts & Phone -->
                    <div class="glass-card rounded-xl sm:rounded-2xl p-4 sm:p-6">
                        <h3 class="text-base sm:text-xl font-semibold text-blue-300 mb-2 sm:mb-3 flex items-center gap-2">
                            <span class="p-1.5 rounded-lg bg-blue-500/10 border border-blue-500/20 text-blue-400 text-sm sm:text-base">📞</span>
                            Contacts & Phone
                        </h3>
                        <p class="text-slate-300 text-xs sm:text-base leading-relaxed">
                            Requested strictly on-demand when mapping gestures to initiate Direct Calling. We do not store, upload, or share your contact list data.
                        </p>
                    </div>
                </div>
            </section>

            <!-- Section 3: Firebase Services & Direct Links -->
            <section id="firebase" class="policy-section glass-panel rounded-2xl sm:rounded-3xl p-5 sm:p-8 md:p-10 shadow-xl relative overflow-hidden pt-20 sm:pt-24 mt-[-4rem] sm:mt-[-5rem]">
                <div class="absolute top-0 left-0 w-1 sm:w-1.5 h-full bg-gradient-to-b from-amber-500 to-orange-500"></div>
                <h2 class="text-lg sm:text-2xl font-bold text-slate-100 mb-3 sm:mb-4 flex items-center gap-2.5">
                    <span class="text-amber-400 text-xs sm:text-sm font-extrabold uppercase tracking-widest bg-amber-500/10 px-2 py-0.5 sm:py-1 rounded-md border border-amber-500/20">03</span>
                    Firebase Integration
                </h2>
                <p class="text-slate-300 text-sm sm:text-base leading-relaxed mb-6">
                    Dynamic Edge Gesture Control utilizes <strong>Google Firebase</strong> to securely collect and process app data for diagnostic monitoring and performance tracking.
                </p>

                <div class="grid grid-cols-1 sm:grid-cols-2 gap-3.5 sm:gap-4 mb-6">
                    <div class="glass-card p-4 rounded-xl border border-slate-800">
                        <div class="flex items-center gap-2 mb-1.5 text-amber-300 text-xs sm:text-sm font-semibold">
                            <span>📈</span> Firebase Analytics
                        </div>
                        <p class="text-[11px] sm:text-xs text-slate-300 leading-relaxed">
                            Collects telemetry data such as app launch frequency, screen views, and feature usage to help us optimize the user interface and app performance.
                        </p>
                    </div>

                    <div class="glass-card p-4 rounded-xl border border-slate-800">
                        <div class="flex items-center gap-2 mb-1.5 text-amber-300 text-xs sm:text-sm font-semibold">
                            <span>🛠️</span> Firebase Crashlytics
                        </div>
                        <p class="text-[11px] sm:text-xs text-slate-300 leading-relaxed">
                            Automatically captures and transmits stack traces and device state during application crashes to allow us to issue rapid software bug fixes.
                        </p>
                    </div>

                    <div class="glass-card p-4 rounded-xl border border-slate-800">
                        <div class="flex items-center gap-2 mb-1.5 text-amber-300 text-xs sm:text-sm font-semibold">
                            <span>⚡</span> Performance Monitoring
                        </div>
                        <p class="text-[11px] sm:text-xs text-slate-300 leading-relaxed">
                            Measures startup timings and background memory footprint to ensure light battery usage across different devices.
                        </p>
                    </div>

                    <div class="glass-card p-4 rounded-xl border border-slate-800">
                        <div class="flex items-center gap-2 mb-1.5 text-amber-300 text-xs sm:text-sm font-semibold">
                            <span>🗄️</span> Realtime Database
                        </div>
                        <p class="text-[11px] sm:text-xs text-slate-300 leading-relaxed">
                            Stores essential edge configuration data locally and securely linked to an anonymous installation ID.
                        </p>
                    </div>
                </div>

                <!-- Direct Firebase Privacy Links Box -->
                <div class="p-4 sm:p-5 rounded-xl sm:rounded-2xl bg-amber-500/10 border border-amber-500/20 text-amber-200">
                    <h4 class="font-bold text-amber-300 text-xs sm:text-sm mb-2 flex items-center gap-2">
                        <span>🔗</span> Google Firebase Privacy Links:
                    </h4>
                    <div class="flex flex-wrap gap-2.5 text-xs font-medium">
                        <a href="https://firebase.google.com/support/privacy" target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-1.5 px-3 py-2 rounded-lg bg-amber-500/20 text-amber-300 border border-amber-500/30 hover:bg-amber-500 hover:text-slate-950 transition-all text-[11px] sm:text-xs">
                            <span>Firebase Privacy Info</span>
                            <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"/></svg>
                        </a>
                        <a href="https://policies.google.com/privacy" target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-1.5 px-3 py-2 rounded-lg bg-amber-500/20 text-amber-300 border border-amber-500/30 hover:bg-amber-500 hover:text-slate-950 transition-all text-[11px] sm:text-xs">
                            <span>Google Privacy Policy</span>
                            <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"/></svg>
                        </a>
                    </div>
                </div>
            </section>

            <!-- Section 4: Google AdMob Privacy Policy & Links -->
            <section id="admob" class="policy-section glass-panel rounded-2xl sm:rounded-3xl p-5 sm:p-8 md:p-10 shadow-xl relative overflow-hidden pt-20 sm:pt-24 mt-[-4rem] sm:mt-[-5rem]">
                <div class="absolute top-0 left-0 w-1 sm:w-1.5 h-full bg-gradient-to-b from-blue-500 to-indigo-500"></div>
                <h2 class="text-lg sm:text-2xl font-bold text-slate-100 mb-3 sm:mb-4 flex items-center gap-2.5">
                    <span class="text-blue-400 text-xs sm:text-sm font-extrabold uppercase tracking-widest bg-blue-500/10 px-2 py-0.5 sm:py-1 rounded-md border border-blue-500/20">04</span>
                    Monetization & Advertising
                </h2>
                <div class="space-y-3 sm:space-y-4 text-slate-300 text-sm sm:text-base leading-relaxed mb-6">
                    <p>
                        To support ongoing development while offering free core features, Dynamic Edge Gesture Control integrates <strong>Google AdMob</strong> to display Rewarded Video Ads and Banner Ads.
                    </p>
                    <ul class="space-y-2 list-disc list-inside text-xs sm:text-sm text-slate-300">
                        <li><strong>Advertising Identifiers:</strong> AdMob may collect device Advertising ID (GAID) and IP addresses to serve contextual advertisements.</li>
                        <li><strong>Opt-Out:</strong> Reset or opt out of ad tracking on Android under <code>Settings -> Google -> Ads</code>.</li>
                    </ul>
                </div>

                <!-- Direct AdMob Privacy Links Box -->
                <div class="p-4 sm:p-5 rounded-xl sm:rounded-2xl bg-blue-500/10 border border-blue-500/20 text-blue-200">
                    <h4 class="font-bold text-blue-300 text-xs sm:text-sm mb-2 flex items-center gap-2">
                        <span>📢</span> Google AdMob Policy Links:
                    </h4>
                    <div class="flex flex-wrap gap-2.5 text-xs font-medium">
                        <a href="https://policies.google.com/technologies/ads" target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-1.5 px-3 py-2 rounded-lg bg-blue-500/20 text-blue-300 border border-blue-500/30 hover:bg-blue-600 hover:text-white transition-all text-[11px] sm:text-xs">
                            <span>Google Ad Policies</span>
                            <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"/></svg>
                        </a>
                        <a href="https://support.google.com/admob/answer/6128543" target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-1.5 px-3 py-2 rounded-lg bg-blue-500/20 text-blue-300 border border-blue-500/30 hover:bg-blue-600 hover:text-white transition-all text-[11px] sm:text-xs">
                            <span>AdMob Help Center</span>
                            <svg class="w-3 h-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"/></svg>
                        </a>
                    </div>
                </div>
            </section>

            <!-- Section 5: Data Security & Retention -->
            <section id="security" class="policy-section glass-panel rounded-2xl sm:rounded-3xl p-5 sm:p-8 md:p-10 shadow-xl relative overflow-hidden pt-20 sm:pt-24 mt-[-4rem] sm:mt-[-5rem]">
                <div class="absolute top-0 left-0 w-1 sm:w-1.5 h-full bg-gradient-to-b from-blue-500 to-indigo-500"></div>
                <h2 class="text-lg sm:text-2xl font-bold text-slate-100 mb-3 sm:mb-4 flex items-center gap-2.5">
                    <span class="text-blue-400 text-xs sm:text-sm font-extrabold uppercase tracking-widest bg-blue-500/10 px-2 py-0.5 sm:py-1 rounded-md border border-blue-500/20">05</span>
                    Security & Retention
                </h2>
                <div class="space-y-3 sm:space-y-4 text-slate-300 text-sm sm:text-base leading-relaxed">
                    <p>
                        <strong>Encryption in Transit:</strong> All network communications with Firebase servers use Transport Layer Security (TLS/HTTPS).
                    </p>
                    <p>
                        <strong>Data Retention:</strong> Gesture profile configurations, user-generated media files, and personal text notes are stored locally on your device hardware. No personal account logins are required.
                    </p>
                    <p>
                        <strong>Data Deletion:</strong> Uninstalling the application permanently removes all local settings, saved media and notes generated by the app, and profile data from your device.
                    </p>
                </div>
            </section>

            <!-- Section 6: Children's Privacy -->
            <section class="policy-section glass-panel rounded-2xl sm:rounded-3xl p-5 sm:p-8 md:p-10 shadow-xl relative overflow-hidden pt-20 sm:pt-24 mt-[-4rem] sm:mt-[-5rem]">
                <div class="absolute top-0 left-0 w-1 sm:w-1.5 h-full bg-gradient-to-b from-blue-500 to-indigo-500"></div>
                <h2 class="text-lg sm:text-2xl font-bold text-slate-100 mb-3 sm:mb-4 flex items-center gap-2.5">
                    <span class="text-blue-400 text-xs sm:text-sm font-extrabold uppercase tracking-widest bg-blue-500/10 px-2 py-0.5 sm:py-1 rounded-md border border-blue-500/20">06</span>
                    Children's Privacy (COPPA / GDPR)
                </h2>
                <p class="text-slate-300 text-sm sm:text-base leading-relaxed">
                    Our application is intended for general audiences and does not knowingly collect personal identifiable information from children under 13 (or 16 in the European Union).
                </p>
            </section>

            <!-- Section 7: Contact & Support -->
            <section id="contact" class="policy-section glass-panel rounded-2xl sm:rounded-3xl p-5 sm:p-8 md:p-10 shadow-xl relative overflow-hidden border-2 border-blue-500/30 pt-20 sm:pt-24 mt-[-4rem] sm:mt-[-5rem]">
                <div class="absolute top-0 left-0 w-1 sm:w-1.5 h-full bg-gradient-to-b from-blue-500 to-indigo-500"></div>
                <h2 class="text-lg sm:text-2xl font-bold text-slate-100 mb-3 sm:mb-4 flex items-center gap-2.5">
                    <span class="text-blue-400 text-xs sm:text-sm font-extrabold uppercase tracking-widest bg-blue-500/10 px-2 py-0.5 sm:py-1 rounded-md border border-blue-500/20">07</span>
                    Contact Us & Support
                </h2>
                <p class="text-slate-300 text-sm sm:text-base leading-relaxed mb-6">
                    If you have questions, feedback, or concerns regarding this Privacy Policy or third-party integrations, please contact support:
                </p>
                
                <div class="flex flex-col sm:flex-row items-stretch sm:items-center gap-3 sm:gap-4">
                    <a href="mailto:m.payra859appsupport@gmail.com" class="inline-flex items-center justify-center gap-2.5 px-6 py-3.5 rounded-xl sm:rounded-2xl bg-gradient-to-r from-blue-600 to-indigo-600 hover:from-blue-500 hover:to-indigo-500 text-white font-semibold text-xs sm:text-base shadow-lg shadow-blue-500/25 transition-all text-center">
                        <svg class="w-4 h-4 sm:w-5 sm:h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"/></svg>
                        <span>Contact Support</span>
                    </a>
                    
                    <button onclick="copyEmail()" class="inline-flex items-center justify-center gap-2 px-5 py-3.5 rounded-xl sm:rounded-2xl bg-slate-900 border border-slate-700 text-slate-300 font-medium hover:bg-slate-800 transition-all text-xs sm:text-sm text-center">
                        <span id="copyBtnText">Copy Email Address</span>
                    </button>
                </div>
            </section>
        </main>

        <!-- Footer -->
        <footer class="text-center mt-12 sm:mt-16 pt-6 sm:pt-8 border-t border-slate-800/80 text-slate-500 text-xs sm:text-sm flex flex-col items-center gap-3">
            
            <!-- Last Updated Badge Moved to Footer -->
            <div class="inline-flex items-center gap-1.5 px-3 py-1.5 rounded-full bg-slate-800/60 border border-slate-700/50 text-[10px] sm:text-xs text-slate-400 mb-2">
                <svg class="w-3 h-3 text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"/></svg>
                <span>Last Updated: July 27, 2026</span>
            </div>

            <p>&copy; 2026 <a href="https://play.google.com/store/apps/details?id=com.m.payra.gesture.control.app" target="_blank" rel="noopener noreferrer" class="text-slate-400 hover:text-blue-400 underline decoration-slate-700 underline-offset-4">Dynamic Edge Gesture Control</a>. All rights reserved.</p>
            <p class="text-[11px] sm:text-xs text-slate-600 max-w-md mx-auto">Android, Google Play, Firebase, and AdMob are registered trademarks of Google LLC.</p>
            <p class="text-xs sm:text-sm text-slate-400 font-medium flex items-center justify-center gap-1.5 pt-1">
                <span>❤️</span> from Madhusudan Payra
            </p>
        </footer>
    </div>
    
    <!-- Scroll to Top Button -->
    <button id="scrollTopBtn" onclick="window.scrollTo({top: 0, behavior: 'smooth'})" class="fixed bottom-6 right-6 p-3 rounded-full bg-blue-600/90 text-white shadow-lg shadow-blue-500/30 border border-blue-400/30 opacity-0 translate-y-10 pointer-events-none transition-all duration-300 z-50 hover:bg-blue-500">
        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M5 15l7-7 7 7"/></svg>
    </button>

    <!-- JavaScript for Search Filtering & Interactivity -->
    <script>
        function filterSections() {
            const query = document.getElementById('policySearch').value.toLowerCase();
            const sections = document.querySelectorAll('.policy-section');
            
            sections.forEach(section => {
                const text = section.innerText.toLowerCase();
                if (text.includes(query)) {
                    section.style.display = 'block';
                } else {
                    section.style.display = 'none';
                }
            });
        }

        function copyEmail() {
            const email = "m.payra859appsupport@gmail.com";
            const btnText = document.getElementById('copyBtnText');
            
            const tempInput = document.createElement('input');
            tempInput.value = email;
            document.body.appendChild(tempInput);
            tempInput.select();
            document.execCommand('copy');
            document.body.removeChild(tempInput);

            btnText.innerText = "Copied! ✓";
            setTimeout(() => {
                btnText.innerText = "Copy Email Address";
            }, 3000);
        }
        
        // Scroll Event Listener for Progress Bar and Scroll-To-Top button
        window.addEventListener('scroll', () => {
            // Calculate scroll progress
            const winScroll = document.body.scrollTop || document.documentElement.scrollTop;
            const height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
            const scrolled = (winScroll / height) * 100;
            document.getElementById('progressBar').style.width = scrolled + '%';
            
            // Show/Hide Scroll to Top button
            const scrollTopBtn = document.getElementById('scrollTopBtn');
            if (winScroll > 300) {
                scrollTopBtn.classList.remove('opacity-0', 'translate-y-10', 'pointer-events-none');
                scrollTopBtn.classList.add('opacity-100', 'translate-y-0');
            } else {
                scrollTopBtn.classList.add('opacity-0', 'translate-y-10', 'pointer-events-none');
                scrollTopBtn.classList.remove('opacity-100', 'translate-y-0');
            }
        });
    </script>
</body>
</html>


