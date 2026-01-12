<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Download POS Application</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
    </style>
</head>
<body class="bg-gray-50 flex items-center justify-center min-h-screen p-0 sm:p-4">

    <div class="w-full sm:max-w-2xl bg-white min-h-screen sm:min-h-0 p-6 md:p-12 sm:rounded-2xl shadow-none sm:shadow-2xl text-center border-0 sm:border border-gray-100 flex flex-col justify-center">

        <h1 class="text-4xl md:text-6xl font-extrabold text-indigo-700 mb-4 tracking-tight">
            POS App
        </h1>
        <p class="text-lg md:text-2xl text-gray-600 mb-10 leading-relaxed px-4">
            Professional Point of Sale Application for Android
        </p>

        <div class="flex flex-col items-center space-y-4 px-4">
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

        <div class="mt-12 pt-8 border-t border-gray-100 px-4">
            <div class="flex flex-col md:flex-row items-center justify-center gap-4 mb-6">
                <p class="text-sm text-gray-500">
                    Latest Version: <span class="px-2 py-1 bg-gray-100 rounded font-mono font-bold text-gray-700">1.0.0</span>
                </p>
                <span class="hidden md:block text-gray-300">|</span>
                <p class="text-xs text-red-600 font-semibold uppercase tracking-wider">
                    Android Only
                </p>
            </div>

            <p class="text-sm text-amber-700 bg-amber-50 p-4 rounded-xl mb-8 border border-amber-100">
                <strong>Note:</strong> Enable "Install from unknown sources" in your security settings to install the APK.
            </p>

            <div class="text-left bg-indigo-50 border-l-4 border-indigo-500 p-6 rounded-r-xl">
                <p class="font-bold text-indigo-900 text-base mb-2">Developer's Note</p>
                <ul class="text-indigo-800 text-sm space-y-3">
                    <li class="flex items-start">
                        <span class="mr-2">🚀</span>
                        <span>Built with a focus on a fast, intuitive UI/UX to make your daily business transactions effortless.</span>
                    </li>
                    <li class="flex items-start">
                        <span class="mr-2">💪</span>
                        <span>Integrated local data storage ensures the app stays responsive even when you're offline.</span>
                    </li>
                </ul>
            </div>
        </div>

    </div>

    <script>
        async function getDownloadCount() {
            const countDisplay = document.getElementById('countDisplay');
            const baseCount = 870; 

            try {
                const response = await fetch('https://api.github.com/repos/blackstorey/Kashera/releases');
                if (!response.ok) throw new Error('API limit');
                
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
