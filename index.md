<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Download Kashera POS</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
    </style>
</head>
<body class="bg-gray-50 flex items-center justify-center min-h-screen p-0 sm:p-4">

    <div class="w-full sm:max-w-2xl bg-white min-h-screen sm:min-h-0 p-8 md:p-12 sm:rounded-3xl shadow-none sm:shadow-2xl text-center border-0 sm:border border-gray-100 flex flex-col justify-center items-center">

        <div class="mb-6">
            <h1 class="text-5xl md:text-7xl font-extrabold text-indigo-700 tracking-tighter">
                Kashera
            </h1>
            <div class="h-1.5 w-24 bg-green-500 mx-auto mt-2 rounded-full"></div>
        </div>

        <h2 class="text-xl md:text-2xl font-bold text-gray-800 mb-2">
            POS App
        </h2>
        <p class="text-lg text-gray-500 mb-10 max-w-sm mx-auto">
            Professional Point of Sale Application for Android
        </p>

        <div class="w-full flex flex-col items-center space-y-4 px-4">
            <a id="downloadButton"
               href="https://github.com/blackstorey/Kashera/releases/latest/download/Kashera.apk"
               download
               class="inline-flex items-center justify-center w-full sm:w-auto px-12 py-5 text-xl font-bold text-white transition-all duration-300
                     bg-green-600 rounded-2xl shadow-lg hover:bg-green-700 hover:shadow-xl
                     focus:outline-none focus:ring-4 focus:ring-green-500 focus:ring-opacity-50 transform hover:-translate-y-1">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-7 w-7 mr-3" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4" />
                </svg>
                Download App (APK)
            </a>
            
            <div id="downloadStats" class="flex items-center justify-center space-x-2 text-gray-500 font-medium">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-green-500" viewBox="0 0 20 20" fill="currentColor">
                    <path fill-rule="evenodd" d="M3 17a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zm3.293-7.707a1 1 0 011.414 0L9 10.586V3a1 1 0 112 0v7.586l1.293-1.293a1 1 0 111.414 1.414l-3 3a1 1 0 01-1.414 0l-3-3a1 1 0 010-1.414z" clip-rule="evenodd" />
                </svg>
                <span id="countDisplay" class="text-sm md:text-base">870+ active installations</span>
            </div>
        </div>

        <div class="mt-12 pt-8 border-t border-gray-100 w-full px-4">
            <div class="flex items-center justify-center gap-4 mb-6">
                <p class="text-sm text-gray-500">
                    Version <span class="font-bold text-gray-700">1.0.0</span>
                </p>
                <span class="text-gray-300">|</span>
                <p class="text-xs text-red-600 font-semibold uppercase tracking-widest">
                    Android
                </p>
            </div>

            <div class="text-left bg-indigo-50 border-l-4 border-indigo-500 p-6 rounded-r-2xl">
                <p class="font-bold text-indigo-900 text-base mb-2">Kashera Developers Note:</p>
                <ul class="text-indigo-800 text-sm space-y-3">
                    <li class="flex items-start">
                        <span class="mr-2">🚀</span>
                        <span>We built a fast, intuitive UI/UX to make your daily business transactions a breeze.</span>
                    </li>
                    <li class="flex items-start">
                        <span class="mr-2">💪</span>
                        <span>Reliable local data storage ensures stability even without a constant internet connection.</span>
                    </li>
                </ul>
            </div>
            
            <p class="mt-8 text-[10px] text-gray-400 uppercase tracking-widest">
                Secure APK Download • Unknown Sources Required
            </p>
        </div>
    </div>

    <script>
        async function getDownloadCount() {
            const countDisplay = document.getElementById('countDisplay');
            const baseCount = 870; 

            try {
                const response = await fetch('https://api.github.com/repos/blackstorey/Kashera/releases');
                if (!response.ok) throw new Error();
                
                const releases = await response.json();
                let githubDownloads = 0;

                releases.forEach(release => {
                    release.assets.forEach(asset => {
                        if (asset.name.toLowerCase().includes('kashera')) {
                            githubDownloads += asset.download_count;
                        }
                    });
                });

                const total = baseCount + githubDownloads;
                countDisplay.textContent = `${total.toLocaleString()} people have downloaded this app`;
            } catch (error) {
                countDisplay.textContent = `${baseCount.toLocaleString()}+ people have downloaded this app`;
            }
        }
        getDownloadCount();
    </script>
</body>
</html>
