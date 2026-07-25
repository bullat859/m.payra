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
            overflow-x: hidden;
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
        /* Hide horizontal scrollbar for mobile navigation */
        .no-scrollbar::-webkit-scrollbar {
            display: none;
        }
        .no-scrollbar {
            -ms-overflow-style: none;
            scrollbar-width: none;
        }
    </style>
</head>
<body class="bg-slate-950 text-slate-100 min-h-screen selection:bg-blue-500 selection:text-white relative antialiased">
    <div class="glow-bg"></div>

    <!-- Top Sticky Navigation Bar -->
    <header class="sticky top-0 z-50 glass-panel border-b border-slate-800/80 bg-slate-950/85 backdrop-blur-lg">
        <div class="max-w-6xl mx-auto px-3 sm:px-6 lg:px-8 h-16 flex items-center justify-between gap-2">
            <a href="https://play.google.com/store/apps/details?id=com.m.payra.gesture.control.app" target="_blank" rel="noopener noreferrer" class="flex items-center gap-2.5 hover:opacity-90 transition-opacity shrink-0">
                <!-- Dynamic Edge Gesture Control Logo (Vector SVG) -->
                <div class="w-9 h-9 sm:w-10 sm:h-10 rounded-xl overflow-hidden shadow-lg shadow-blue-500/20 shrink-0 border border-white/10">
                    <svg viewBox="0 0 100 100" class="w-full h-full" xmlns="http://www.w3.org/2000/svg">
                        <defs>
                            <linearGradient id="bgGrad" x1="0%" y1="0%" x2="100%" y2="100%">
                                <stop offset="0%" stop-color="#4c1d95"/>
                                <stop offset="50%" stop-color="#1e1b4b"/>
                                <stop offset="100%" stop-color="#b45309"/>
                            </linearGradient>
                            <linearGradient id="neonGrad" x1="0%" y1="0%" x2="100%" y2="100%">
                                <stop offset="0%" stop-color="#38bdf8"/>
                                <stop offset="50%" stop-color="#a855f7"/>
                                <stop offset="100%" stop-color="#f97316"/>
                            </linearGradient>
                        </defs>
                        <rect width="100" height="100" fill="url(#bgGrad)"/>
                        <path d="M 20 22 C 20 18 24 14 28 14 L 38 14 C 40 14 42 16 43 18 L 45 22 C 46 24 48 25 50 25 C 52 25 54 24 55 22 L 57 18 C 58 16 60 14 62 14 L 72 14 C 76 14 80 18 80 22 L 80 78 C 80 82 76 86 72 86 L 28 86 C 24 86 20 82 20 78 Z" fill="none" stroke="url(#neonGrad)" stroke-width="3.5" stroke-linecap="round" stroke-linejoin="round"/>
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

                <span class="font-bold text-slate-100 text-sm sm:text-base tracking-tight hidden md:inline-block">Dynamic Edge Gesture Control</span>
                <span class="font-bold text-slate-100 text-sm sm:text-base tracking-tight md:hidden">Edge Control</span>
            </a>
            
            <nav class="flex items-center gap-1 sm:gap-3 text-xs sm:text-sm font-medium overflow-x-auto no-scrollbar py-1 shrink">
                <a href="#overview" class="text-slate-400 hover:text-blue-400 transition-colors px-2 py-1.5 rounded-lg hover:bg-slate-800/50 whitespace-nowrap">Overview</a>
                <a href="#permissions" class="text-slate-400 hover:text-blue-400 transition-colors px-2 py-1.5 rounded-lg hover:bg-slate-800/50 whitespace-nowrap">Permissions</a>
                <a href="#firebase" class="text-slate-400 hover:text-blue-400 transition-colors px-2 py-1.5 rounded-lg hover:bg-slate-800/50 whitespace-nowrap">Firebase</a>
                <a href="#admob" class="text-slate-400 hover:text-blue-400 transition-colors px-2 py-1.5 rounded-lg hover:bg-slate-800/50 whitespace-nowrap">AdMob</a>
                <a href="#contact" class="px-2.5 py-1.5 rounded-lg bg-blue-600/20 text-blue-400 border border-blue-500/30 hover:bg-blue-600 hover:text-white transition-all whitespace-nowrap">Support</a>
            </nav>
        </div>
    </header>

    <div class="max-w-4xl mx-auto px-3 sm:px-6 lg:px-8 py-8 sm:py-16">
        
        <!-- Hero Title Section -->
        <div class="text-center mb-8 sm:mb-12 relative">
            <div class="inline-flex items-center gap-2 px-3 py-1.5 rounded-full bg-blue-500/10 border border-blue-500/20 text-blue-400 text-[11px] sm:text-xs font-semibold tracking-wider uppercase mb-4 sm:mb-6 shadow-sm">
                <span class="w-2 h-2 rounded-full bg-blue-400 animate-pulse"></span>
                Official Legal Transparency Notice
            </div>
            <h1 class="text-2xl sm:text-4xl md:text-5xl font-extrabold tracking-tight bg-gradient-to-r from-white via-slate-200 to-blue-400 bg-clip-text text-transparent mb-3 leading-tight">
                Privacy Policy
            </h1>
            <p class="text-base sm:text-xl text-slate-300 font-medium">
                Dynamic Edge Gesture Control
            </p>

            <!-- Google Play Store Button -->
            <div class="mt-5 sm:mt-6 flex justify-center">
                <a href="https://play.google.com/store/apps/details?id=com.m.payra.gesture.control.app" target="_blank" rel="noopener noreferrer" class="inline-flex items-center gap-2.5 px-4 sm:px-5 py-2.5 rounded-xl bg-slate-900 border border-slate-700 hover:border-blue-500/50 text-slate-200 text-xs sm:text-sm font-semibold transition-all hover:bg-slate-800 shadow-md transform hover:-translate-y-0.5">
                    <svg class="w-4 h-4 sm:w-5 sm:h-5 text-emerald-400 shrink-0" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M3,20.5V3.5C3,2.91 3.34,2.39 3.84,2.15L13.69,12L3.84,21.85C3.34,21.6 3,21.09 3,20.5M16.81,15.12L18.81,13.12C19.86,12.55 19.86,11.45 18.81,10.88L16.81,8.88L14.81,10.88L14.81,13.12L16.81,15.12M13.69,12L3.84,2.15L15.39,8.81L13.69,12M13.69,12L15.39,15.19L3.84,21.85L13.69,12Z"/>
                    </svg>
                    <span>Get it on Google Play</span>
                    <svg class="w-3 h-3 sm:w-3.5 sm:h-3.5 text-slate-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"/></svg>
                </a>
            </div>
        </div>

        <!-- Quick Policy Highlights Grid -->
        <section id="overview" class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-3.5 sm:gap-4 mb-8 sm:mb-10">
            <div class="glass-panel p-4 sm:p-5 rounded-2xl border border-slate-800">
                <div class="w-9 h-9 sm:w-10 sm:h-10 rounded-xl bg-blue-500/10 text-blue-400 flex items-center justify-center text-lg sm:text-xl mb-2.5 sm:mb-3 border border-blue-500/20">
                    🛡️
                </div>
                <h3 class="text-sm sm:text-base font-semibold text-slate-100 mb-1">No Personal Data Sold</h3>
                <p class="text-slate-400 text-xs leading-relaxed">We never sell, rent, or trade your personal information, gesture configurations, or contact lists to third parties.</p>
            </div>

            <div class="glass-panel p-4 sm:p-5 rounded-2xl border border-slate-800">
                <div class="w-9 h-9 sm:w-10 sm:h-10 rounded-xl bg-emerald-500/10 text-emerald-400 flex items-center justify-center text-lg sm:text-xl mb-2.5 sm:mb-3 border border-emerald-500/20">
                    ⚙️
                </div>
                <h3 class="text-sm sm:text-base font-semibold text-slate-100 mb-1">Local Processing</h3>
                <p class="text-slate-400 text-xs leading-relaxed">Gesture handling, touch triggers, and screen overlays are processed 100% locally on your device for maximum speed.</p>
            </div>

            <div class="glass-panel p-4 sm:p-5 rounded-2xl border border-slate-800 sm:col-span-2 md:col-span-1">
                <div class="w-9 h-9 sm:w-10 sm:h-10 rounded-xl bg-amber-500/10 text-amber-400 flex items-center justify-center text-lg sm:text-xl mb-2.5 sm:mb-3 border border-amber-500/20">
                    🔥
                </div>
                <h3 class="text-sm sm:text-base font-semibold text-slate-100 mb-1">Firebase & AdMob</h3>
                <p class="text-slate-400 text-xs leading-relaxed">Firebase handles diagnostic crash reports and database syncing, while AdMob serves optional rewarded ad features.</p>
            </div>
        </section>

        <!-- Search Bar Filter -->
        <div class="mb-8 sm:mb-10 glass-panel p-2.5 sm:p-3 rounded-2xl flex items-center gap-2.5">
            <svg class="w-4 h-4 sm:w-5 sm:h-5 text-slate-400 ml-1.5 shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"/></svg>
            <input type="text" id="policySearch" onkeyup="filterSections()" placeholder="Search terms (e.g. Firebase, Accessibility, Location)..." class="w-full bg-transparent text-xs sm:text-sm text-slate-200 placeholder-slate-500 focus:outline-none py-1">
        </div>

        <!-- Main Document Body -->
        <main class="space-y-6 sm:space-y-8">

            <!-- Section 1: Introduction -->
            <section class="policy-section glass-panel rounded-2xl sm:rounded-3xl p-5 sm:p-8 md:p-10 shadow-xl relative overflow-hidden">
                <div class="absolute top-0 left-0 w-1 sm:w-1.5 h-full bg-gradient-to-b from-blue-500 to-indigo-500"></div>
                <h2 class="text-lg sm:text-2xl font-bold text-slate-100 mb-3 sm:mb-4 flex items-center gap-2.5">
                    <span class="text-blue-400 text-xs sm:text-sm font-extrabold uppercase tracking-widest bg-blue-500/10 px-2 py-0.5 sm:py-1 rounded-md border border-blue-500/20">01</span>
                    Introduction & Architecture
                </h2>
                <div class="space-y-3 sm:space-y-4 text-slate-300 text-sm sm:text-base leading-relaxed">
                    <p>
                        Welcome to <strong>Dynamic Edge Gesture Control</strong>. We respect your privacy and are committed to protecting it through complete transparency regarding our data processing practices.
                    </p>
                    <p>
                        Our application provides deep system customization and gesture automation. While primary gesture detection, touch listening, and screen overlays function offline directly on your device, our app connects to secure cloud services (specifically Google Firebase) to sync online configurations, diagnose software crashes, monitor app performance, and serve rewarded video ads via Google AdMob.
                    </p>
                    <p class="text-xs sm:text-sm bg-slate-900/80 border border-slate-800 p-3.5 sm:p-4 rounded-xl text-slate-400">
                        By installing, accessing, or using Dynamic Edge Gesture Control, you acknowledge and agree to the data collection and usage practices described in this Privacy Policy.
                    </p>
                </div>
            </section>

            <!-- Section 2: Android Permissions Required -->
            <section id="permissions" class="policy-section glass-panel rounded-2xl sm:rounded-3xl p-5 sm:p-8 md:p-10 shadow-xl relative overflow-hidden">
                <div class="absolute top-0 left-0 w-1 sm:w-1.5 h-full bg-gradient-to-b from-blue-500 to-indigo-500"></div>
                <h2 class="text-lg sm:text-2xl font-bold text-slate-100 mb-3 sm:mb-4 flex items-center gap-2.5">
                    <span class="text-blue-400 text-xs sm:text-sm font-extrabold uppercase tracking-widest bg-blue-500/10 px-2 py-0.5 sm:py-1 rounded-md border border-blue-500/20">02</span>
                    Android Permissions
                </h2>
                <p class="text-slate-300 text-sm sm:text-base leading-relaxed mb-6 sm:mb-8">
                    To deliver system-wide gesture controls, our app requests explicit permissions on your Android device. Each permission is used strictly for local automation:
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

                    <!-- Storage -->
                    <div class="glass-card rounded-xl sm:rounded-2xl p-4 sm:p-6">
                        <h3 class="text-base sm:text-xl font-semibold text-blue-300 mb-2 sm:mb-3 flex items-center gap-2">
                            <span class="p-1.5 rounded-lg bg-blue-500/10 border border-blue-500/20 text-blue-400 text-sm sm:text-base">💾</span>
                            Storage & Media Access
                        </h3>
                        <p class="text-slate-300 text-xs sm:text-base leading-relaxed">
                            Required for local features such as the <strong>Offline Music Controller</strong>, importing custom icons, and saving/restoring gesture backups.
                        </p>
                    </div>

                    <!-- Hardware Actions -->
                    <div class="glass-card rounded-xl sm:rounded-2xl p-4 sm:p-6">
                        <h3 class="text-base sm:text-xl font-semibold text-blue-300 mb-2 sm:mb-3 flex items-center gap-2">
                            <span class="p-1.5 rounded-lg bg-blue-500/10 border border-blue-500/20 text-blue-400 text-sm sm:text-base">🎙️</span>
                            Hardware Actions
                        </h3>
                        <p class="text-slate-300 text-xs sm:text-base leading-relaxed">
                            Requested strictly on-demand when mapping gestures to Flashlight (Camera), Audio Memos (Microphone), Bluetooth toggles, or Direct Calling (Contacts & Phone).
                        </p>
                    </div>
                </div>
            </section>

            <!-- Section 3: Firebase Services & Direct Links -->
            <section id="firebase" class="policy-section glass-panel rounded-2xl sm:rounded-3xl p-5 sm:p-8 md:p-10 shadow-xl relative overflow-hidden">
                <div class="absolute top-0 left-0 w-1 sm:w-1.5 h-full bg-gradient-to-b from-amber-500 to-orange-500"></div>
                <h2 class="text-lg sm:text-2xl font-bold text-slate-100 mb-3 sm:mb-4 flex items-center gap-2.5">
                    <span class="text-amber-400 text-xs sm:text-sm font-extrabold uppercase tracking-widest bg-amber-500/10 px-2 py-0.5 sm:py-1 rounded-md border border-amber-500/20">03</span>
                    Firebase Integration
                </h2>
                <p class="text-slate-300 text-sm sm:text-base leading-relaxed mb-6">
                    Dynamic Edge Gesture Control utilizes <strong>Google Firebase</strong> for diagnostic monitoring, performance tracking, remote configurations, and cloud database synchronization.
                </p>

                <div class="grid grid-cols-1 sm:grid-cols-2 gap-3.5 sm:gap-4 mb-6">
                    <div class="glass-card p-4 rounded-xl border border-slate-800">
                        <div class="flex items-center gap-2 mb-1.5 text-amber-300 text-xs sm:text-sm font-semibold">
                            <span>📈</span> Firebase Analytics
                        </div>
                        <p class="text-[11px] sm:text-xs text-slate-300 leading-relaxed">
                            Collects anonymized telemetry such as app launch frequency and feature usage to optimize UI performance.
                        </p>
                    </div>

                    <div class="glass-card p-4 rounded-xl border border-slate-800">
                        <div class="flex items-center gap-2 mb-1.5 text-amber-300 text-xs sm:text-sm font-semibold">
                            <span>🛠️</span> Firebase Crashlytics
                        </div>
                        <p class="text-[11px] sm:text-xs text-slate-300 leading-relaxed">
                            Captures stack traces and state during application crashes to allow rapid software bug fixes.
                        </p>
                    </div>

                    <div class="glass-card p-4 rounded-xl border border-slate-800">
                        <div class="flex items-center gap-2 mb-1.5 text-amber-300 text-xs sm:text-sm font-semibold">
                            <span>⚡</span> Performance Monitoring
                        </div>
                        <p class="text-[11px] sm:text-xs text-slate-300 leading-relaxed">
                            Measures startup timings and background memory footprint to ensure light battery usage.
                        </p>
                    </div>

                    <div class="glass-card p-4 rounded-xl border border-slate-800">
                        <div class="flex items-center gap-2 mb-1.5 text-amber-300 text-xs sm:text-sm font-semibold">
                            <span>🗄️</span> Realtime Database
                        </div>
                        <p class="text-[11px] sm:text-xs text-slate-300 leading-relaxed">
                            Stores user-backed custom edge configurations linked to an anonymous installation ID.
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
            <section id="admob" class="policy-section glass-panel rounded-2xl sm:rounded-3xl p-5 sm:p-8 md:p-10 shadow-xl relative overflow-hidden">
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
            <section class="policy-section glass-panel rounded-2xl sm:rounded-3xl p-5 sm:p-8 md:p-10 shadow-xl relative overflow-hidden">
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
                        <strong>Data Retention:</strong> Gesture profile configurations are stored locally on your device hardware. No personal account logins are required.
                    </p>
                    <p>
                        <strong>Data Deletion:</strong> Uninstalling the application permanently removes all local settings and profile data.
                    </p>
                </div>
            </section>

            <!-- Section 6: Children's Privacy -->
            <section class="policy-section glass-panel rounded-2xl sm:rounded-3xl p-5 sm:p-8 md:p-10 shadow-xl relative overflow-hidden">
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
            <section id="contact" class="policy-section glass-panel rounded-2xl sm:rounded-3xl p-5 sm:p-8 md:p-10 shadow-xl relative overflow-hidden border-2 border-blue-500/30">
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
                        <svg class="w-4 h-4 sm:w-5 sm:h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 002-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/></svg>
                        <span>Contact Support</span>
                    </a>
                    
                    <button onclick="copyEmail()" class="inline-flex items-center justify-center gap-2 px-5 py-3.5 rounded-xl sm:rounded-2xl bg-slate-900 border border-slate-700 text-slate-300 font-medium hover:bg-slate-800 transition-all text-xs sm:text-sm text-center">
                        <span id="copyBtnText">Copy Email Address</span>
                    </button>
                </div>
            </section>
        </main>

        <!-- Footer -->
        <footer class="text-center mt-12 sm:mt-16 pt-6 sm:pt-8 border-t border-slate-800/80 text-slate-500 text-xs sm:text-sm flex flex-col items-center gap-2.5">
            <p>&copy; 2026 <a href="https://play.google.com/store/apps/details?id=com.m.payra.gesture.control.app" target="_blank" rel="noopener noreferrer" class="text-slate-400 hover:text-blue-400 underline decoration-slate-700 underline-offset-4">Dynamic Edge Gesture Control</a>. All rights reserved.</p>
            <p class="text-[11px] sm:text-xs text-slate-600 max-w-md">Android, Google Play, Firebase, and AdMob are registered trademarks of Google LLC.</p>
            <p class="text-xs sm:text-sm text-slate-400 font-medium flex items-center gap-1.5 mt-1">
                <span>❤️</span> from Madhusudan Payra
            </p>
        </footer>
    </div>

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

            btnText.innerText = "Copied to Clipboard! ✓";
            setTimeout(() => {
                btnText.innerText = "Copy Email Address";
            }, 3000);
        }
    </script>
</body>
</html>
