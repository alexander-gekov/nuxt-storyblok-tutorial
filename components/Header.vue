<template>
    <header class="w-full h-24 bg-[#f7f6fd]">
      <div class="container h-full mx-auto flex items-center justify-between">
        <NuxtLink to="/">
          <h1 class="text-gray-800 text-3xl font-bold">My Blog</h1>
        </NuxtLink>
        <nav>
          <ul class="flex space-x-8 text-lg font-bold">
            <li>
              <NuxtLink to="/blog" class="hover:text-gray-800">Blog</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/about" class="hover:text-gray-800">About Me</NuxtLink>
            </li>
          </ul>
        </nav>
      </div>
    </header>
  </template>