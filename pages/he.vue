<template>
    <div class="bg-[#fdfaf4] min-h-screen text-gray-800 text-right direction-rtl font-serif">
      <header class="text-center py-6 border-b border-gray-300">
        <h1 class="text-4xl title-font text-gray-900">ריסטורנטה אלגנסה</h1>
        <p class="text-sm text-gray-600 italic">מסעדה איטלקית - פריז</p>
        <div class="mt-2">
          <NuxtLink to="/" class="text-sm underline text-blue-600 hover:text-blue-800">🇫🇷 Français</NuxtLink>
        </div>
      </header>
  
      <main class="max-w-2xl mx-auto py-10 px-4">
        <section class="mb-10">
          <h2 class="text-2xl mb-4 font-bold title-font">מנות פתיחה</h2>
          <MenuItemHe v-for="(item, index) in entrees" :key="index" v-bind="item" />
        </section>
  
        <section class="mb-10">
          <h2 class="text-2xl mb-4 font-bold title-font">עיקריות</h2>
          <MenuItemHe v-for="(item, index) in plats" :key="index" v-bind="item" />
        </section>
  
        <section>
          <h2 class="text-2xl mb-4 font-bold title-font">קינוחים</h2>
          <MenuItemHe v-for="(item, index) in desserts" :key="index" v-bind="item" />
        </section>
      </main>
  
      <Footer />
    </div>
  </template>
  
  <script setup lang="ts">
  import Footer from '@/components/Footer.vue'
  import MenuItemHe from '@/components/MenuItemHe.vue'
  
  const entrees = [
    { name: 'ברוסקטה', description: 'עגבניות שרי, שום, בזיליקום טרי', price: 8 },
    { name: 'קרפצ’יו בקר', description: 'רוקט, פרמזן', price: 12 }
  ]
  
  const plats = [
    { name: 'ספגטי קרבונרה', description: 'פנצ’טה, ביצה, פקורינו', price: 15 },
    { name: 'ריזוטו פטריות', description: 'קרם כמהין', price: 17 }
  ]
  
  const desserts = [
    { name: 'טירמיסו', description: 'איטלקי קלאסי עם מסקרפונה', price: 7 },
    { name: 'פנה קוטה', description: 'רוטב פירות יער', price: 6 }
  ]
  </script>
  