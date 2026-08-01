<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AI-Powered Android Apps</title>
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Font Awesome Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <style>
    /* Custom dark gradient background and glow effects */
    body {
      background-color: #080e14;
      color: #e2e8f0;
      font-family: ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
    }
    .glow-cyan {
      box-shadow: 0 0 50px -10px rgba(6, 182, 212, 0.25);
    }
    .card-bg {
      background-color: rgba(15, 23, 42, 0.6);
      border: 1px solid rgba(255, 255, 255, 0.08);
      backdrop-filter: blur(12px);
    }
  </style>
</head>
<body class="min-h-screen flex flex-col justify-between selection:bg-teal-500 selection:text-black">

  <!-- Glow Background Accents -->
  <div class="fixed top-0 left-1/4 w-96 h-96 bg-cyan-500/10 rounded-full blur-3xl pointer-events-none"></div>
  <div class="fixed top-1/3 right-10 w-96 h-96 bg-teal-500/10 rounded-full blur-3xl pointer-events-none"></div>

  <!-- Header / Navigation -->
  <header class="container mx-auto px-6 py-6 flex items-center justify-between relative z-10">
    <div class="text-sm font-semibold tracking-wide">
      <span class="text-gray-300">AI-Powered Android Apps</span><br>
      <span class="text-gray-500 font-normal">by <span class="text-teal-400">[Developer Name]</span></span>
    </div>

    <nav class="hidden md:flex items-center space-x-8 text-sm text-gray-300">
      <a href="#" class="hover:text-teal-400 transition">Home</a>
      <a href="#" class="hover:text-teal-400 transition">Solutions</a>
      <a href="#" class="hover:text-teal-400 transition">Blogs</a>
      <a href="#" class="hover:text-teal-400 transition">Services</a>
      <a href="#" class="hover:text-teal-400 transition">Contact</a>
    </nav>

    <div class="flex items-center space-x-4">
      <a href="#" class="text-sm text-gray-300 hover:text-white transition">Log in</a>
      <a href="#" class="bg-teal-500 hover:bg-teal-400 text-slate-950 px-5 py-2.5 rounded-full font-medium text-sm transition shadow-lg shadow-teal-500/20">
        Start your Project
      </a>
    </div>
  </header>

  <!-- Hero Section -->
  <main class="container mx-auto px-6 py-10 relative z-10 flex-grow">
    <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center my-8">
      
      <!-- Hero Left: Visual Graphic Placeholder -->
      <div class="lg:col-span-6 relative flex justify-center">
        <div class="relative w-full max-w-md aspect-square rounded-3xl card-bg p-6 flex flex-col items-center justify-center border border-teal-500/20 glow-cyan">
          <!-- Animated / Styled Graphic Placeholder -->
          <div class="absolute inset-0 bg-gradient-to-tr from-cyan-500/10 to-teal-500/10 rounded-3xl"></div>
          <div class="relative z-10 text-center">
            <div class="w-48 h-80 mx-auto bg-slate-900 border-4 border-slate-700 rounded-[2.5rem] p-4 flex flex-col justify-between shadow-2xl relative overflow-hidden">
              <div class="w-16 h-4 bg-slate-800 rounded-full mx-auto"></div>
              <div class="my-auto">
                <i class="fa-solid fa-brain text-4xl text-teal-400 mb-2"></i>
                <div class="text-xs font-bold tracking-widest text-teal-300">NEXUS AI</div>
                <div class="w-full h-12 bg-slate-800/80 rounded-lg mt-3 p-1 flex items-end gap-1 justify-center">
                  <div class="w-2 h-4 bg-teal-400 rounded-sm"></div>
                  <div class="w-2 h-8 bg-cyan-400 rounded-sm"></div>
                  <div class="w-2 h-6 bg-teal-500 rounded-sm"></div>
                </div>
              </div>
              <div class="w-full h-8 bg-slate-800 rounded-lg"></div>
            </div>
          </div>
          <!-- Tech Tags -->
          <div class="absolute top-4 left-4 bg-slate-900/90 border border-slate-700 text-xs px-3 py-1.5 rounded-lg flex items-center gap-2">
            <i class="fa-brands fa-python text-yellow-400"></i> Python
          </div>
          <div class="absolute bottom-6 left-6 bg-slate-900/90 border border-slate-700 text-xs px-3 py-1.5 rounded-lg flex items-center gap-2">
            <i class="fa-solid fa-code text-purple-400"></i> Kotlin
          </div>
          <div class="absolute bottom-12 right-4 bg-slate-900/90 border border-slate-700 text-xs px-3 py-1.5 rounded-lg flex items-center gap-2">
            <i class="fa-solid fa-cubes text-orange-400"></i> TensorFlow
          </div>
        </div>
      </div>

      <!-- Hero Right: Content -->
      <div class="lg:col-span-6 space-y-6">
        <span class="text-teal-400 text-xs font-bold tracking-widest uppercase">
          ELEVATE YOUR ANDROID APPS WITH INTELLIGENCE
        </span>
        <h1 class="text-4xl sm:text-5xl font-extrabold text-white leading-tight">
          Custom AI Solutions for Android | Smart, Efficient, Powerful Mobile Applications.
        </h1>
        <p class="text-gray-400 text-base max-w-xl leading-relaxed">
          Expert Android Developer Specializing in Integrating Advanced AI & Machine Learning models into high-performance mobile applications.
        </p>
        <div class="flex flex-wrap items-center gap-4 pt-2">
          <a href="#" class="px-6 py-3 rounded-full border border-slate-700 hover:border-teal-400 text-white font-medium text-sm transition">
            View Portfolio
          </a>
          <a href="#" class="px-6 py-3 rounded-full bg-teal-400 hover:bg-teal-300 text-slate-950 font-semibold text-sm transition shadow-lg shadow-teal-500/20">
            Start your Project
          </a>
        </div>
      </div>
    </div>

    <!-- Bottom Section: Grid -->
    <div class="grid grid-cols-1 md:grid-cols-12 gap-6 mt-12">
      
      <!-- Expertise List -->
      <div class="md:col-span-4 card-bg p-6 rounded-2xl">
        <h3 class="text-lg font-semibold text-white mb-4">My Expertise</h3>
        <ul class="space-y-3 text-sm text-gray-300">
          <li class="flex items-center gap-3">
            <i class="fa-regular fa-circle-check text-teal-400"></i> AI Chatbot Integration
          </li>
          <li class="flex items-center gap-3">
            <i class="fa-regular fa-circle-check text-teal-400"></i> Smart Image Editor
          </li>
          <li class="flex items-center gap-3">
            <i class="fa-regular fa-circle-check text-teal-400"></i> Predictive Text & Search
          </li>
          <li class="flex items-center gap-3">
            <i class="fa-regular fa-circle-check text-teal-400"></i> Voice Recognition AI
          </li>
          <li class="flex items-center gap-3">
            <i class="fa-regular fa-circle-check text-teal-400"></i> Custom ML Pipeline
          </li>
          <li class="flex items-center gap-3">
            <i class="fa-regular fa-circle-check text-teal-400"></i> AI Optimization
          </li>
          <li class="flex items-center gap-3">
            <i class="fa-regular fa-circle-check text-teal-400"></i> On-Device AI Services
          </li>
        </ul>
      </div>

      <!-- Featured Projects -->
      <div class="md:col-span-5 flex flex-col justify-between">
        <div>
          <h3 class="text-lg font-semibold text-white mb-4">Featured Projects</h3>
          <div class="grid grid-cols-3 gap-3">
            <!-- Card 1 -->
            <div class="card-bg p-3 rounded-xl flex flex-col items-center text-center hover:border-teal-500/40 transition">
              <div class="w-full h-20 bg-slate-800 rounded-lg mb-2 flex items-center justify-center text-teal-400">
                <i class="fa-solid fa-robot text-2xl"></i>
              </div>
              <span class="text-xs font-medium text-white">AI Chatbot</span>
              <span class="text-[10px] text-gray-400">Android App</span>
            </div>
            <!-- Card 2 -->
            <div class="card-bg p-3 rounded-xl flex flex-col items-center text-center hover:border-teal-500/40 transition">
              <div class="w-full h-20 bg-slate-800 rounded-lg mb-2 flex items-center justify-center text-cyan-400">
                <i class="fa-solid fa-image text-2xl"></i>
              </div>
              <span class="text-xs font-medium text-white">Smart Image</span>
              <span class="text-[10px] text-gray-400">Editor App</span>
            </div>
            <!-- Card 3 -->
            <div class="card-bg p-3 rounded-xl flex flex-col items-center text-center hover:border-teal-500/40 transition">
              <div class="w-full h-20 bg-slate-800 rounded-lg mb-2 flex items-center justify-center text-indigo-400">
                <i class="fa-solid fa-microchip text-2xl"></i>
              </div>
              <span class="text-xs font-medium text-white">Prediction</span>
              <span class="text-[10px] text-gray-400">AI Engine</span>
            </div>
          </div>
        </div>
      </div>

      <!-- Testimonials / About Me -->
      <div class="md:col-span-3 card-bg p-5 rounded-2xl flex flex-col justify-between">
        <div class="flex items-center justify-between mb-3">
          <span class="text-xs font-semibold text-gray-400">Client Testimonials</span>
          <i class="fa-solid fa-chevron-down text-xs text-gray-500"></i>
        </div>
        
        <div class="bg-slate-800/80 rounded-xl overflow-hidden mb-3">
          <!-- Placeholder Profile Image -->
          <img src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&w=400&q=80" alt="About Me" class="w-full h-28 object-cover">
        </div>

        <div>
          <h4 class="text-sm font-semibold text-white">About Me</h4>
          <p class="text-xs text-gray-400 mt-1 leading-relaxed">
            Providing tailored and modern solutions in Smart Mobile & AI-driven applications.
          </p>
        </div>
      </div>

    </div>
  </main>

</body>
</html>
