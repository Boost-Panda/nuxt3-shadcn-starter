<template>
  <div>

    <head>
      <meta charset="UTF-8" />
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>What the Food</title>
    </head>

    <body class="space-y-6 px-4 border-t-4 border-gray-700 min-h-screen">

      <div class="max-w-7xl mx-auto">
        <div class="flex justify-center">
          <img src="@/assets/images/whatthefood.webp" alt="Logo" class="h-16 w-full object-contain md:h-24" />
        </div>
        <h1 class="scroll-m-20 text-4xl font-extrabold tracking-tight lg:text-5xl text-center mt-6">
          Analyze what you eat
        </h1>
      </div>
      <div class="max-w-7xl mx-auto">
        <NuxtPage />
      </div>


      <div class="max-w-7xl mx-auto sticky top-[100vh] text-center">
        <p class="py-2 text-xs">Built with ❤️ by <a href="https://aliirz.com" target="_blank">aliirz</a></p>
      </div>
    </body>
  </div>
</template>