<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Download POS Application</title>
    <!-- Load Tailwind CSS for utility-first styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Custom styles for the Inter font and overall aesthetics */
        body {
            font-family: 'Inter', sans-serif;
        }
    </style>
</head>
<body class="bg-gray-50 flex items-center justify-center min-h-screen p-4">

    <!-- Application Download Card -->
    <div class="w-full max-w-xl bg-white p-8 md:p-12 rounded-xl shadow-2xl text-center border border-gray-100">

        <!-- Header and Logo (Optional) -->
        <h1 class="text-4xl md:text-5xl font-extrabold text-indigo-700 mb-2">
            POS App
        </h1>
        <p class="text-xl text-gray-600 mb-8">
            Point of Sale Application for Android
        </p>

        <!-- Main Call to Action (Download Button) -->
        <!--
            We have updated the href to use the relative path 'kashera.apk'.
            This assumes 'kashera.apk' is in the same folder as this 'index.html' file.
        -->
        <a id="downloadButton"
           href="kashera.apk"
           download
           class="inline-flex items-center justify-center w-full sm:w-auto px-10 py-4 text-xl font-semibold text-white transition-all duration-300
                  bg-green-600 rounded-full shadow-lg hover:bg-green-700 hover:shadow-xl
                  focus:outline-none focus:ring-4 focus:ring-green-500 focus:ring-opacity-50 transform hover:scale-105">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mr-3" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4" />
            </svg>
            Download App (APK)
        </a>

        <!-- Version Information and Instructions -->
        <div class="mt-8 pt-6 border-t border-gray-200">
            <p class="text-sm text-gray-500 mb-2">
                Latest Version: <span class="font-semibold text-gray-700">1.0.0</span>
            </p>
            <p class="text-xs text-red-500 font-medium bg-red-50 p-2 rounded-lg mb-4 inline-block">
                Note: Ensure you have "Install from unknown sources" enabled on your Android device.
            </p>

            <!-- Troubleshooting Note -->
            <div class="text-left bg-blue-50 border-l-4 border-blue-400 p-3 rounded-md mt-4">
                <p class="font-bold text-blue-800 text-sm">Troubleshooting Tip:</p>
                <ul class="text-blue-700 text-xs list-disc pl-5 mt-1 space-y-1">
                    <li>Double-check that your file named <span class="font-mono bg-blue-100 px-1 rounded">kashera.apk</span> is uploaded in the **same folder** as your <span class="font-mono bg-blue-100 px-1 rounded">index.html</span> file.</li>
                    <li>File names on GitHub are **case-sensitive** (e.g., `Kashera.apk` is different from `kashera.apk`).</li>
                </ul>
            </div>
        </div>

    </div>

    

</body>
</html>
