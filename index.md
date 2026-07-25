<!DOCTYPE html>
<html lang="en" class="dark scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
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
        }
        .glass-panel {
            background: rgba(17, 24, 39, 0.7);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.07);
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
            width: 8px;
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
    </style>
</head>
<body class="bg-slate-950 text-slate-100 min-h-screen selection:bg-blue-500 selection:text-white relative">
    <div class="glow-bg"></div>

    <!-- Top Sticky Navigation Bar -->
    <header class="sticky top-0 z-50 glass-panel border-b border-slate-800/80 bg-slate-950/80 backdrop-blur-lg">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
            <div class="flex items-center gap-3">
                <div class="w-9 h-9 rounded-xl bg-gradient-to-tr from-blue-600 to-indigo-500 flex items-center justify-center shadow-lg shadow-blue-500/20 font-bold text-white text-lg">
                    ⚡
                </div>
                <span class="font-bold text-slate-100 text-sm sm:text-base tracking-tight hidden sm:inline-block">Dynamic Edge Gesture Control</span>
                <span class="font-bold text-slate-100 text-sm sm:text-base tracking-tight sm:hidden">Edge Control</span>
            </div>
            
            <nav class="flex items-center gap-2 sm:gap-4 text-xs sm:text-sm font-medium">
                <a href="#overview" class="text-slate-400 hover:text-blue-400 transition-colors px-2.5 py-1.5 rounded-lg hover:bg-slate-800/50">Overview</a>
                <a href="#permissions" class="text-slate-400 hover:text-blue-400 transition-colors px-2.5 py-1.5 rounded-lg hover:bg-slate-800/50">Permissions</a>
                <a href="#firebase" class="text-slate-400 hover:text-blue-400 transition-colors px-2.5 py-1.5 rounded-lg hover:bg-slate-800/50">Firebase Services</a>
                <a href="#contact" class="px-3 py-1.5 rounded-lg bg-blue-600/20 text-blue-400 border border-blue-500/30 hover:bg-blue-600 hover:text-white transition-all">Support</a>
            </nav>
        </div>
    </header>

    <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-12 sm:py-20">
        
        <!-- Hero Title Section -->
        <div class="text-center mb-12 relative">
            <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full bg-blue-500/10 border border-blue-500/20 text-blue-400 text-xs font-semibold tracking-wider uppercase mb-6 shadow-sm">
                <span class="w-2 h-2 rounded-full bg-blue-400 animate-pulse"></span>
                Official Legal Transparency Notice
            </div>
            <h1 class="text-3xl sm:text-5xl font-extrabold tracking-tight bg-gradient-to-r from-white via-slate-200 to-blue-400 bg-clip-text text-transparent mb-4 leading-tight">
                Privacy Policy
            </h1>
            <p class="text-lg sm:text-xl text-slate-300 font-medium">
                Dynamic Edge Gesture Control
            </p>
            <p class="text-slate-400 font-medium text-xs sm:text-sm tracking-wide uppercase mt-3">
                Effective Date: July 20, 2026 &nbsp;•&nbsp; Document Version 2.4
            </p>
        </div>

        <!-- Quick Policy Highlights Grid -->
        <section id="overview" class="grid grid-cols-1 md:grid-cols-3 gap-4 mb-10">
            <div class="glass-panel p-5 rounded-2xl border border-slate-800">
                <div class="w-10 h-10 rounded-xl bg-blue-500/10 text-blue-400 flex items-center justify-center text-xl mb-3 border border-blue-500/20">
                    🛡️
                </div>
                <h3 class="text-base font-semibold text-slate-100 mb-1">No Personal Data Sold</h3>
                <p class="text-slate-400 text-xs leading-relaxed">We never sell, rent, or trade your personal information, gesture configurations, or contact lists to advertisers.</p>
            </div>

            <div class="glass-panel p-5 rounded-2xl border border-slate-800">
                <div class="w-10 h-10 rounded-xl bg-emerald-500/10 text-emerald-400 flex items-center justify-center text-xl mb-3 border border-emerald-500/20">
                    ⚙️
                </div>
                <h3 class="text-base font-semibold text-slate-100 mb-1">Local Processing First</h3>
                <p class="text-slate-400 text-xs leading-relaxed">Gesture handling, touch triggers, and screen overlays are processed 100% locally on your device for real-time speed.</p>
            </div>

            <div class="glass-panel p-5 rounded-2xl border border-slate-800">
                <div class="w-10 h-10 rounded-xl bg-purple-500/10 text-purple-400 flex items-center justify-center text-xl mb-3 border border-purple-500/20">
                    🔥
                </div>
                <h3 class="text-base font-semibold text-slate-100 mb-1">Firebase Telemetry</h3>
                <p class="text-slate-400 text-xs leading-relaxed">Online diagnostics (Firebase Analytics & Crashlytics) monitor crashes and app performance to ensure stability.</p>
            </div>
        </section>

        <!-- Search Bar Filter for fast navigation -->
        <div class="mb-10 glass-panel p-3 rounded-2xl flex items-center gap-3">
            <svg class="w-5 h-5 text-slate-400 ml-2 shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"/></svg>
            <input type="text" id="policySearch" onkeyup="filterSections()" placeholder="Search terms (e.g. Firebase, Accessibility, Location, Crashlytics)..." class="w-full bg-transparent text-sm text-slate-200 placeholder-slate-500 focus:outline-none">
        </div>

        <!-- Main Document Body -->
        <main class="space-y-8">

            <!-- Section 1: Introduction -->
            <section class="policy-section glass-panel rounded-3xl p-6 sm:p-10 shadow-2xl relative overflow-hidden">
                <div class="absolute top-0 left-0 w-1.5 h-full bg-gradient-to-b from-blue-500 to-indigo-500"></div>
                <h2 class="text-xl sm:text-2xl font-bold text-slate-100 mb-4 flex items-center gap-3">
                    <span class="text-blue-400 text-sm font-extrabold uppercase tracking-widest bg-blue-500/10 px-2.5 py-1 rounded-md border border-blue-500/20">01</span>
                    Introduction & Architecture Overview
                </h2>
                <div class="space-y-4 text-slate-300 text-base sm:text-lg leading-relaxed">
                    <p>
                        Welcome to <strong>Dynamic Edge Gesture Control</strong> ("we," "our," or "us"). We respect your privacy and are committed to protecting it through complete transparency regarding our data processing practices.
                    </p>
                    <p>
                        Our application provides deep system customization and gesture automation. While primary gesture detection, touch listening, and screen overlays function offline directly on your device, our app connects to secure cloud services (primarily Google Firebase) to sync online configurations, diagnose software crashes, monitor app performance, and serve rewarded ad features.
                    </p>
                    <p class="text-sm bg-slate-900/80 border border-slate-800 p-4 rounded-xl text-slate-400">
                        By installing, accessing, or using Dynamic Edge Gesture Control, you acknowledge and agree to the data collection and usage practices described in this Privacy Policy.
                    </p>
                </div>
            </section>

            <!-- Section 2: Android Permissions Required -->
            <section id="permissions" class="policy-section glass-panel rounded-3xl p-6 sm:p-10 shadow-2xl relative overflow-hidden">
                <div class="absolute top-0 left-0 w-1.5 h-full bg-gradient-to-b from-blue-500 to-indigo-500"></div>
                <h2 class="text-xl sm:text-2xl font-bold text-slate-100 mb-4 flex items-center gap-3">
                    <span class="text-blue-400 text-sm font-extrabold uppercase tracking-widest bg-blue-500/10 px-2.5 py-1 rounded-md border border-blue-500/20">02</span>
                    Android Permissions & Local Functionality
                </h2>
                <p class="text-slate-300 text-base sm:text-lg leading-relaxed mb-8">
                    To deliver system-wide gesture controls, our app requests explicit permissions on your Android device. Each permission is used strictly for local automation:
                </p>
                
                <div class="space-y-6">
                    <!-- Accessibility Service -->
                    <div class="glass-card rounded-2xl p-5 sm:p-6">
                        <div class="flex items-center justify-between mb-3 flex-wrap gap-2">
                            <h3 class="text-lg sm:text-xl font-semibold text-blue-300 flex items-center gap-2.5">
                                <span class="p-2 rounded-xl bg-blue-500/10 border border-blue-500/20 text-blue-400 text-base">🛠️</span>
                                Accessibility Service API
                            </h3>
                            <span class="text-xs px-2.5 py-1 rounded-full bg-red-500/10 text-red-400 border border-red-500/20 font-semibold">Core Required Permission</span>
                        </div>
                        <p class="text-slate-300 text-base leading-relaxed mb-4">
                            The Accessibility Service API is the foundational engine of Dynamic Edge Gesture Control. It is strictly utilized to:
                        </p>
                        <ul class="space-y-2.5 my-4 text-slate-300 list-none pl-0">
                            <li class="relative pl-6 before:absolute before:left-0 before:text-blue-400 before:content-['✦']">Draw touch-sensitive gesture overlay handles (edge sliders, notches, dynamic islands, and pie menus) on top of active screens.</li>
                            <li class="relative pl-6 before:absolute before:left-0 before:text-blue-400 before:content-['✦']">Detect your swipe, tap, long-press, and drag gestures specifically within these configured edge handle zones.</li>
                            <li class="relative pl-6 before:absolute before:left-0 before:text-blue-400 before:content-['✦']">Execute global Android system actions assigned to your gestures (e.g., Back, Home, Recent Apps, Quick Settings, Split Screen, and Power Menu).</li>
                        </ul>
                        <div class="bg-red-500/10 border-l-4 border-red-500 p-4 rounded-r-xl mt-4 text-red-200 text-sm leading-relaxed">
                            <strong class="font-bold text-red-400 block mb-1">Strict Accessibility Privacy Guarantee:</strong>
                            We do NOT use the Accessibility Service API to read screen content, inspect keystrokes, intercept passwords, log personal messages, or track your interactions within other third-party apps. Its operation is strictly confined to rendering edge UI and sending standard system navigation callbacks.
                        </div>
                    </div>

                    <!-- Location -->
                    <div class="glass-card rounded-2xl p-5 sm:p-6">
                        <h3 class="text-lg sm:text-xl font-semibold text-blue-300 mb-3 flex items-center gap-2.5">
                            <span class="p-2 rounded-xl bg-blue-500/10 border border-blue-500/20 text-blue-400 text-base">📍</span>
                            Location Access (Foreground & Background)
                        </h3>
                        <p class="text-slate-300 text-base leading-relaxed">
                            Used exclusively for <strong>Situational Location Triggers</strong>. If you opt to set up geofenced gestures (e.g., auto-switching edge profiles when arriving home or at work), background location monitors when you enter or exit your chosen geofence boundary. Location coordinates are never sold or uploaded to public tracking networks.
                        </p>
                    </div>
                    
                    <!-- Usage Access -->
                    <div class="glass-card rounded-2xl p-5 sm:p-6">
                        <h3 class="text-lg sm:text-xl font-semibold text-blue-300 mb-3 flex items-center gap-2.5">
                            <span class="p-2 rounded-xl bg-blue-500/10 border border-blue-500/20 text-blue-400 text-base">📊</span>
                            Usage Access (Package Usage Stats)
                        </h3>
                        <p class="text-slate-300 text-base leading-relaxed">
                            Allows the app to identify which foreground application is currently active on your screen. This enables "App-Specific Gesture Profiles," automatically hiding edge handles or switching gesture shortcuts when specific apps (e.g., full-screen games or camera) are opened.
                        </p>
                    </div>

                    <!-- Modify System Settings -->
                    <div class="glass-card rounded-2xl p-5 sm:p-6">
                        <h3 class="text-lg sm:text-xl font-semibold text-blue-300 mb-3 flex items-center gap-2.5">
                            <span class="p-2 rounded-xl bg-blue-500/10 border border-blue-500/20 text-blue-400 text-base">⚙️</span>
                            Modify System Settings (Write Settings)
                        </h3>
                        <p class="text-slate-300 text-base leading-relaxed">
                            Empowers your gestures to directly toggle hardware and system parameters—such as Screen Brightness, Auto-Rotate lock, Volume levels, and Screen Timeout—without opening the Android Settings app.
                        </p>
                    </div>

                    <!-- Storage -->
                    <div class="glass-card rounded-2xl p-5 sm:p-6">
                        <h3 class="text-lg sm:text-xl font-semibold text-blue-300 mb-3 flex items-center gap-2.5">
                            <span class="p-2 rounded-xl bg-blue-500/10 border border-blue-500/20 text-blue-400 text-base">💾</span>
                            Storage & Media Access
                        </h3>
                        <p class="text-slate-300 text-base leading-relaxed">
                            Required to support local features such as the <strong>Offline Music Controller</strong> (browsing and playing local MP3 audio files), importing custom gesture icons, and saving or restoring local profile backup files (`.json`/`.xml`).
                        </p>
                    </div>

                    <!-- Camera, Microphone, Bluetooth & Contacts -->
                    <div class="glass-card rounded-2xl p-5 sm:p-6">
                        <h3 class="text-lg sm:text-xl font-semibold text-blue-300 mb-3 flex items-center gap-2.5">
                            <span class="p-2 rounded-xl bg-blue-500/10 border border-blue-500/20 text-blue-400 text-base">🎙️</span>
                            Hardware Actions (Camera, Mic, Bluetooth, Contacts)
                        </h3>
                        <p class="text-slate-300 text-base leading-relaxed">
                            These permissions are requested strictly on-demand when you map a gesture to specific quick actions:
                        </p>
                        <ul class="list-disc list-inside text-slate-300 text-sm mt-2 space-y-1">
                            <li><strong>Camera:</strong> Toggling the LED Flashlight on/off.</li>
                            <li><strong>Microphone:</strong> Triggering quick audio memo recordings.</li>
                            <li><strong>Bluetooth:</strong> Toggling Bluetooth radio state or connecting to paired devices.</li>
                            <li><strong>Contacts & Phone:</strong> Triggering "Direct Call" or "Quick Contact" actions from a gesture swipe.</li>
                        </ul>
                    </div>
                </div>
            </section>

            <!-- Section 3: Firebase Services & Cloud Data Collection -->
            <section id="firebase" class="policy-section glass-panel rounded-3xl p-6 sm:p-10 shadow-2xl relative overflow-hidden">
                <div class="absolute top-0 left-0 w-1.5 h-full bg-gradient-to-b from-amber-500 to-orange-500"></div>
                <h2 class="text-xl sm:text-2xl font-bold text-slate-100 mb-4 flex items-center gap-3">
                    <span class="text-amber-400 text-sm font-extrabold uppercase tracking-widest bg-amber-500/10 px-2.5 py-1 rounded-md border border-amber-500/20">03</span>
                    Firebase Cloud Integration & Online Analytics
                </h2>
                <p class="text-slate-300 text-base sm:text-lg leading-relaxed mb-6">
                    Although our gesture control engine operates locally, Dynamic Edge Gesture Control utilizes <strong>Google Firebase</strong> (a cloud backend provided by Google LLC) to monitor stability, improve features, manage cloud configurations, and prevent software bugs.
                </p>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                    <!-- Firebase Analytics -->
                    <div class="glass-card p-5 rounded-2xl border border-slate-800">
                        <div class="flex items-center gap-2 mb-2 text-amber-300 font-semibold">
                            <span>📈</span> Firebase Analytics
                        </div>
                        <p class="text-xs text-slate-300 leading-relaxed">
                            Collects anonymized telemetry such as app launch frequency, feature engagement (e.g., which gesture styles are most popular), screen views, mobile device model, Android OS version, and coarse country-level location. Used strictly to optimize UI/UX.
                        </p>
                    </div>

                    <!-- Firebase Crashlytics -->
                    <div class="glass-card p-5 rounded-2xl border border-slate-800">
                        <div class="flex items-center gap-2 mb-2 text-amber-300 font-semibold">
                            <span>🛠️</span> Firebase Crashlytics
                        </div>
                        <p class="text-xs text-slate-300 leading-relaxed">
                            In the event of an app crash or memory fault, Crashlytics automatically captures stack traces, active device states, memory usage at time of crash, and OS information. This allows our engineering team to swiftly issue bug fixes.
                        </p>
                    </div>

                    <!-- Firebase Performance Monitoring -->
                    <div class="glass-card p-5 rounded-2xl border border-slate-800">
                        <div class="flex items-center gap-2 mb-2 text-amber-300 font-semibold">
                            <span>⚡</span> Firebase Performance Monitoring
                        </div>
                        <p class="text-xs text-slate-300 leading-relaxed">
                            Measures network request latencies, app startup timings, and background memory footprint to ensure that gesture overlays render at high frame rates without draining battery life.
                        </p>
                    </div>

                    <!-- Firebase Database & Firestore -->
                    <div class="glass-card p-5 rounded-2xl border border-slate-800">
                        <div class="flex items-center gap-2 mb-2 text-amber-300 font-semibold">
                            <span>🗄️</span> Firebase Realtime Database / Firestore
                        </div>
                        <p class="text-xs text-slate-300 leading-relaxed">
                            Used if you choose to back up your custom edge configurations or download cloud-hosted gesture theme presets. Your configurations are tied to a unique, non-identifiable installation ID.
                        </p>
                    </div>

                    <!-- Firebase Remote Config -->
                    <div class="glass-card p-5 rounded-2xl border border-slate-800">
                        <div class="flex items-center gap-2 mb-2 text-amber-300 font-semibold">
                            <span>🎛️</span> Firebase Remote Config
                        </div>
                        <p class="text-xs text-slate-300 leading-relaxed">
                            Allows us to dynamically update default gesture parameters, introduce seasonal themes, or toggle feature availability without requiring a full app store update.
                        </p>
                    </div>

                    <!-- Firebase App Distribution -->
                    <div class="glass-card p-5 rounded-2xl border border-slate-800">
                        <div class="flex items-center gap-2 mb-2 text-amber-300 font-semibold">
                            <span>🚀</span> Firebase App Distribution
                        </div>
                        <p class="text-xs text-slate-300 leading-relaxed">
                            Utilized during beta testing releases to securely deliver early test builds to registered beta testers and aggregate early feedback logs.
                        </p>
                    </div>
                </div>

                <div class="mt-6 p-4 rounded-xl bg-slate-900/90 border border-slate-800 text-xs text-slate-400">
                    💡 For more details on how Google processes Firebase data, please consult Google's official privacy documentation: 
                    <a href="https://policies.google.com/privacy" target="_blank" rel="noopener text-blue-400 hover:underline">Google Privacy & Terms</a> and 
                    <a href="https://firebase.google.com/support/privacy" target="_blank" rel="noopener text-blue-400 hover:underline">How Firebase guards user privacy</a>.
                </div>
            </section>

            <!-- Section 4: Advertising & Third-Party Services -->
            <section class="policy-section glass-panel rounded-3xl p-6 sm:p-10 shadow-2xl relative overflow-hidden">
                <div class="absolute top-0 left-0 w-1.5 h-full bg-gradient-to-b from-blue-500 to-indigo-500"></div>
                <h2 class="text-xl sm:text-2xl font-bold text-slate-100 mb-4 flex items-center gap-3">
                    <span class="text-blue-400 text-sm font-extrabold uppercase tracking-widest bg-blue-500/10 px-2.5 py-1 rounded-md border border-blue-500/20">04</span>
                    Monetization & Advertising (Google AdMob)
                </h2>
                <div class="space-y-4 text-slate-300 text-base leading-relaxed">
                    <p>
                        To support ongoing development while offering core features for free, Dynamic Edge Gesture Control integrates <strong>Google AdMob</strong> to display Rewarded Video Ads and Banner Ads.
                    </p>
                    <ul class="space-y-2 list-disc list-inside text-sm text-slate-300">
                        <li><strong>Advertising Identifiers:</strong> AdMob may collect and use your device’s Google Advertising ID (GAID) and IP address to deliver personalized or contextual advertisements.</li>
                        <li><strong>Ad Personalization Controls:</strong> You can reset or opt out of personalized ad tracking directly in your device settings under <code>Settings -> Google -> Ads</code>.</li>
                    </ul>
                </div>
            </section>

            <!-- Section 5: Data Security & Retention -->
            <section class="policy-section glass-panel rounded-3xl p-6 sm:p-10 shadow-2xl relative overflow-hidden">
                <div class="absolute top-0 left-0 w-1.5 h-full bg-gradient-to-b from-blue-500 to-indigo-500"></div>
                <h2 class="text-xl sm:text-2xl font-bold text-slate-100 mb-4 flex items-center gap-3">
                    <span class="text-blue-400 text-sm font-extrabold uppercase tracking-widest bg-blue-500/10 px-2.5 py-1 rounded-md border border-blue-500/20">05</span>
                    Data Storage, Encryption & Security
                </h2>
                <div class="space-y-4 text-slate-300 text-base leading-relaxed">
                    <p>
                        <strong>Encryption in Transit:</strong> All communication between Dynamic Edge Gesture Control and Firebase cloud servers uses industry-standard Transport Layer Security (TLS/HTTPS) encryption.
                    </p>
                    <p>
                        <strong>Data Retention & Accountless System:</strong> We do not require you to create an account with an email address or password. Because local configurations reside on your device, you hold complete ownership over your data.
                    </p>
                    <p>
                        <strong>Data Deletion:</strong> Uninstalling the application immediately and permanently removes all local settings, gesture mappings, and cached media stored on your hardware. Firebase analytical logs are automatically purged on a standard 14-month rolling retention schedule set by Google analytics standards.
                    </p>
                </div>
            </section>

            <!-- Section 6: Children's Privacy -->
            <section class="policy-section glass-panel rounded-3xl p-6 sm:p-10 shadow-2xl relative overflow-hidden">
                <div class="absolute top-0 left-0 w-1.5 h-full bg-gradient-to-b from-blue-500 to-indigo-500"></div>
                <h2 class="text-xl sm:text-2xl font-bold text-slate-100 mb-4 flex items-center gap-3">
                    <span class="text-blue-400 text-sm font-extrabold uppercase tracking-widest bg-blue-500/10 px-2.5 py-1 rounded-md border border-blue-500/20">06</span>
                    Children's Privacy Protection (COPPA / GDPR)
                </h2>
                <p class="text-slate-300 text-base sm:text-lg leading-relaxed">
                    Our app is designed for general audiences and is not directed towards children under the age of 13 (or 16 in the European Economic Area). We do not knowingly collect personal identifiable information from children. If you become aware that a child has provided us with personal data, please contact us immediately so we can take steps to remove such information from our records.
                </p>
            </section>

            <!-- Section 7: User Privacy Rights (GDPR / CCPA) -->
            <section class="policy-section glass-panel rounded-3xl p-6 sm:p-10 shadow-2xl relative overflow-hidden">
                <div class="absolute top-0 left-0 w-1.5 h-full bg-gradient-to-b from-blue-500 to-indigo-500"></div>
                <h2 class="text-xl sm:text-2xl font-bold text-slate-100 mb-4 flex items-center gap-3">
                    <span class="text-blue-400 text-sm font-extrabold uppercase tracking-widest bg-blue-500/10 px-2.5 py-1 rounded-md border border-blue-500/20">07</span>
                    Your Legal Privacy Rights
                </h2>
                <div class="space-y-4 text-slate-300 text-base leading-relaxed">
                    <p>Depending on your jurisdiction (e.g., California CCPA/CPRA, European Union GDPR), you possess specific legal rights concerning your data:</p>
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-3 text-sm">
                        <div class="p-3 bg-slate-900/60 rounded-xl border border-slate-800">
                            <strong class="text-blue-300 block mb-1">Right to Opt-Out</strong>
                            You can opt out of analytics data collection within the in-app Settings menu.
                        </div>
                        <div class="p-3 bg-slate-900/60 rounded-xl border border-slate-800">
                            <strong class="text-blue-300 block mb-1">Right to Access / Portability</strong>
                            You can export your gesture profile configuration files at any time.
                        </div>
                    </div>
                </div>
            </section>

            <!-- Section 8: Contact & Support -->
            <section id="contact" class="policy-section glass-panel rounded-3xl p-6 sm:p-10 shadow-2xl relative overflow-hidden border-2 border-blue-500/30">
                <div class="absolute top-0 left-0 w-1.5 h-full bg-gradient-to-b from-blue-500 to-indigo-500"></div>
                <h2 class="text-xl sm:text-2xl font-bold text-slate-100 mb-4 flex items-center gap-3">
                    <span class="text-blue-400 text-sm font-extrabold uppercase tracking-widest bg-blue-500/10 px-2.5 py-1 rounded-md border border-blue-500/20">08</span>
                    Contact Us & Privacy Support
                </h2>
                <p class="text-slate-300 text-base sm:text-lg leading-relaxed mb-6">
                    If you have questions, feedback, or concerns regarding this Privacy Policy or our Firebase data practices, please reach out directly to our support desk:
                </p>
                
                <div class="flex flex-col sm:flex-row items-start sm:items-center gap-4">
                    <a href="mailto:m.payra859appsupport@gmail.com" class="inline-flex items-center gap-3 px-8 py-4 rounded-2xl bg-gradient-to-r from-blue-600 to-indigo-600 hover:from-blue-500 hover:to-indigo-500 text-white font-semibold shadow-lg shadow-blue-500/25 transition-all duration-300 transform hover:-translate-y-0.5">
                        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 002-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/></svg>
                        <span>Contact Official Support</span>
                    </a>
                    
                    <button onclick="copyEmail()" class="inline-flex items-center gap-2 px-5 py-4 rounded-2xl bg-slate-900 border border-slate-700 text-slate-300 font-medium hover:bg-slate-800 transition-all text-sm">
                        <span id="copyBtnText">Copy Email Address</span>
                    </button>
                </div>
            </section>
        </main>

        <!-- Footer -->
        <footer class="text-center mt-16 pt-8 border-t border-slate-800/80 text-slate-500 text-sm flex flex-col items-center gap-3">
            <p>&copy; 2026 Dynamic Edge Gesture Control. All rights reserved.</p>
            <p class="text-xs text-slate-600">Android, Google Play, Firebase, and AdMob are registered trademarks of Google LLC.</p>
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
            
            // Clipboard copy with fallback
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

