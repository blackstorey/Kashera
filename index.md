<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Download POS Application</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Custom styles for the Inter font and overall aesthetics */
        /*
           To use the Inter font, you should link to it (e.g., from Google Fonts).
           Without a link, 'Inter' might not be available, and it will fall back to sans-serif.
           The link to Google Fonts has been added below.
        */
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@100..900&display=swap');
        
        body {
            font-family: 'Inter', sans-serif;
        }
    </style>
</head>
<body class="bg-gray-50 flex items-center justify-center min-h-screen p-4">

    <div class="w-full max-w-xl bg-white p-8 md:p-12 rounded-xl shadow-2xl text-center border border-gray-100">

        <h1 class="text-4xl md:text-5xl font-extrabold text-indigo-700 mb-2">
            POS App
        </h1>
        <p class="text-xl text-gray-600 mb-8">
            Point of Sale Application for Android
        </p>

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

        <div class="mt-8 pt-6 border-t border-gray-200">
            <p class="text-sm text-gray-500 mb-2">
                Latest Version: <span class="font-semibold text-gray-700">1.0.0</span>
            </p>
            <p class="text-xs text-red-500 font-medium bg-red-50 p-2 rounded-lg mb-4 inline-block">
                Note: Ensure you have "Install from unknown sources" enabled on your Android device.
            </p>
        </div> </div> <script>
        console.log("POS App Download Page Initialized.");
    </script>

</body>
</html>
