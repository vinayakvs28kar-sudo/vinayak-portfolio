# vinayak-portfolio
🚀 Creative Developer Portfolio | CS Student | Master Video Editor &amp; Content Creator | Full-stack Web Dev | Featured Project: Library Management System.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vinayak Satapute | Portfolio</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body { background-color: #050505; color: #e5e7eb; scroll-behavior: smooth; }
        .glass { background: rgba(255, 255, 255, 0.03); backdrop-filter: blur(12px); border: 1px solid rgba(255, 255, 255, 0.1); }
        .hero-glow { position: absolute; top: 20%; left: 50%; transform: translate(-50%, -50%); width: 300px; height: 300px; background: #3b82f6; filter: blur(120px); opacity: 0.2; z-index: -1; }
    </style>
</head>
<body>

    <nav class="fixed top-0 w-full z-50 px-6 py-4 flex justify-between items-center glass">
        <span class="font-bold tracking-tighter text-xl">VS.</span>
        <button id="musicToggle" class="bg-white/10 hover:bg-white/20 px-4 py-2 rounded-full text-sm transition flex items-center gap-2">
            <span id="musicIcon">▶️</span> <span id="musicStatus">Play "Believer" (Classical)</span>
        </button>
    </nav>

    <div id="player" class="hidden"></div>

    <main class="relative">
        <div class="hero-glow"></div>
        
        <section class="pt-32 pb-20 px-6 text-center">
            <div class="relative inline-block mb-8">
                <img src="20260130_142633(1).jpg" alt="Vinayak" class="w-48 h-48 rounded-2xl object-cover shadow-2xl border border-white/10">
                <div class="absolute -bottom-4 -right-4 bg-blue-600 px-4 py-1 rounded-lg text-xs font-bold uppercase tracking-widest">Available for Hire</div>
            </div>
            <h1 class="text-6xl font-black mb-4 tracking-tight">VINAYAK <span class="text-blue-500">SATAPUTE</span></h1>
            <p class="text-gray-400 text-lg max-w-xl mx-auto mb-8 italic">
                "No one wants to see you in success; only you can see."
            </p>
            <div class="flex flex-wrap justify-center gap-4">
                <span class="glass px-4 py-2 rounded-lg text-sm">🎬 Video Editing Expert</span>
                <span class="glass px-4 py-2 rounded-lg text-sm">💻 Web Developer</span>
                <span class="glass px-4 py-2 rounded-lg text-sm">🚀 LeetCode Solver</span>
            </div>
        </section>

        <section class="py-20 px-6 max-w-5xl mx-auto">
            <h2 class="text-3xl font-bold mb-10">Top Projects</h2>
            <div class="glass p-8 rounded-3xl grid md:grid-cols-2 gap-10">
                <div>
                    <h3 class="text-2xl font-bold text-blue-400 mb-2">Library Management System</h3>
                    <p class="text-gray-400 leading-relaxed mb-4">
                        A robust CS project built to handle book tracking, user memberships, and digital cataloging with a clean UI.
                    </p>
                    <div class="flex gap-2">
                        <span class="text-xs bg-white/10 px-2 py-1 rounded">Java/Python</span>
                        <span class="text-xs bg-white/10 px-2 py-1 rounded">SQL</span>
                    </div>
                </div>
                <div class="bg-black/40 rounded-xl flex items-center justify-center border border-white/5">
                    <span class="text-gray-600">Project Screenshot</span>
                </div>
            </div>
        </section>

        <section class="py-20 px-6 max-w-xl mx-auto text-center">
            <h2 class="text-4xl font-bold mb-8">Let's Create.</h2>
            <form class="space-y-4">
                <input type="text" placeholder="Your Name" class="w-full glass p-4 rounded-xl outline-none focus:border-blue-500">
                <input type="email" placeholder="Your Email" class="w-full glass p-4 rounded-xl outline-none focus:border-blue-500">
                <textarea placeholder="Tell me about your project..." rows="4" class="w-full glass p-4 rounded-xl outline-none focus:border-blue-500"></textarea>
                <button type="button" class="w-full bg-blue-600 hover:bg-blue-700 py-4 rounded-xl font-bold transition">Send Message</button>
            </form>
        </section>
    </main>

    <script>
        // YouTube API Integration
        var tag = document.createElement('script');
        tag.src = "https://www.youtube.com/iframe_api";
        var firstScriptTag = document.getElementsByTagName('script')[0];
        firstScriptTag.parentNode.insertBefore(tag, firstScriptTag);

        var player;
        function onYouTubeIframeAPIReady() {
            player = new YT.Player('player', {
                height: '0', width: '0',
                videoId: 'EUg4al8zLy0', // Your classical music choice
                events: { 'onReady': onPlayerReady }
            });
        }

        function onPlayerReady() {
            const btn = document.getElementById('musicToggle');
            const icon = document.getElementById('musicIcon');
            const status = document.getElementById('musicStatus');
            
            btn.addEventListener('click', () => {
                if (player.getPlayerState() == 1) {
                    player.pauseVideo();
                    icon.innerText = "▶️";
                    status.innerText = "Play Music";
                } else {
                    player.playVideo();
                    icon.innerText = "⏸️";
                    status.innerText = "Music Playing...";
                }
            });
        }
    </script>
</body>
</html>
