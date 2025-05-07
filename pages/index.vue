<template>
  <div>
    <!-- Loader -->
    <div v-if="loading" class="fixed inset-0 flex items-center justify-center bg-white z-50">
      <div class="flex flex-col items-center animate-fade-in">
        <img
          src="https://img.freepik.com/vecteurs-libre/lettre-coloree-creation-logo-degrade_474888-2309.jpg"
          alt="Logo"
          class="w-28 h-28 object-contain mb-4"
        />
        <div class="w-40 h-1 bg-pink-200 rounded-full overflow-hidden">
          <div class="h-full bg-pink-500 animate-loading-bar"></div>
        </div>
      </div>
    </div>

    <!-- Site -->
    <div
      v-else
      class="min-h-screen bg-pink-50 px-4 py-8 transition-opacity duration-500 ease-out"
      style="background: linear-gradient(to bottom right, #ffe4e6, #fff1f2);"
    >
      <div class="backdrop-blur-md bg-white/80 rounded-3xl max-w-4xl mx-auto p-6 shadow-2xl space-y-8 border border-white/30">
        <Header />
        <MenuSection title="Entrées" :items="menu.entrees" />
        <MenuSection title="Plats" :items="menu.plats" />
        <MenuSection title="Desserts" :items="menu.desserts" />
        <Footer />
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import Header from '@/components/Header.vue'
import MenuSection from '@/components/MenuSection.vue'
import Footer from '@/components/Footer.vue'

const loading = ref(true)

onMounted(() => {
  setTimeout(() => {
    loading.value = false
  }, 3000)
})

const menu = {
  entrees: [
    {
      name: 'Assiette Sushi',
      description: 'Sushis variés avec gingembre et wasabi',
      price: 12,
      image: 'https://img.freepik.com/photos-gratuite/assiette-gros-plan-sushi_23-2148631177.jpg?semt=ais_hybrid&w=740'
    },
    {
      name: 'Sushi Set Deluxe',
      description: 'Assortiment de sashimis et makis',
      price: 18,
      image: 'https://st4.depositphotos.com/19157714/31390/i/450/depositphotos_313903296-stock-photo-close-view-delicious-sushi-set.jpg'
    }
  ],
  plats: [
    {
      name: 'Gunkan Crevettes',
      description: 'Gunkan maki crevettes et concombre',
      price: 14,
      image: 'https://miyakosushi.fr/wp-content/uploads/2024/05/MENU-SUSHI-UNE.png'
    },
    {
      name: 'Nigiri Classiques',
      description: 'Sushis nigiri thon, saumon, daurade',
      price: 15,
      image: 'https://www.academiedugout.fr/images/50789/1200-686/10023-nigiri-sushi.jpg?poix=50&poiy=50'
    },
    {
      name: 'Plateau Mix Lady',
      description: 'Signature Bozen - makis & rolls modernes',
      price: 22,
      image: 'https://lady-sushi.fr/app/uploads/2023/09/image-scaled-1-960x646.jpg'
    },
    {
      name: 'Menu Sushi Une',
      description: 'Présentation esthétique et raffinée',
      price: 18,
      image: 'https://miyakosushi.fr/wp-content/uploads/2024/05/MENU-SUSHI-UNE.png'
    }
  ],
  desserts: [
    {
      name: 'Menu Premium Bozen',
      description: 'Mix de sushis avec accompagnement',
      price: 25,
      image: 'https://files.gandi.ws/gandi43264/image/m11.jpg'
    },
    {
      name: 'Saumon Signature',
      description: 'Saumon fondant sauce sucrée',
      price: 17,
      image: 'https://sushishop.com/wp-content/uploads/2024/12/SS24_UEATS_CHU_SALMON.jpg'
    }
  ]
}
</script>

<style scoped>
@keyframes loading-bar {
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(100%);
  }
}

.animate-loading-bar {
  animation: loading-bar 1.5s infinite ease-in-out;
}

.animate-fade-in {
  animation: fadeIn 0.6s ease-in-out forwards;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: scale(0.98);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}
</style>
