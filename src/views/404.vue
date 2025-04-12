<template>
    <div class="flex flex-col items-center justify-center min-h-screen bg-gray-900 text-white">
      <div class="text-center">
        <h1 class="text-6xl font-bold mb-4">404</h1>
        <p class="text-2xl mb-6">Oops! The page you're looking for doesn't exist.</p>
        <p class="mb-8">It seems like you've followed a broken link or entered a URL that doesn't exist.</p>
        <router-link to="/" class="bg-primary text-white py-2 px-4 rounded-lg text-lg transition duration-300 ease-in-out hover:bg-primary-dark">
          Go Back to Homepage
        </router-link>
      </div>
    </div>
  </template>
  
  <style scoped>
  .bg-primary {
    background-color: #3498db;
  }
  
  .bg-primary-dark {
    background-color: #2980b9;
  }
  </style>
  