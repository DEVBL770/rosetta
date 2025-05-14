<template>
  <footer class="bg-white text-[#1b3b34] py-8">
    <div class="container mx-auto px-4 text-center">
      
      <b><p class="text-sm mb-5">Rosetta Halavi 17e</p></b>
      <div class="mb-6">
        <!-- Logo Instagram en noir et blanc -->
        <a href="https://www.instagram.com/grupporosetta" target="_blank" class="inline-block">
          <img src="https://img.icons8.com/ios/50/instagram-new--v1.png" alt="Instagram Rosetta 17" class="w-6 h-6 mx-auto" />
        </a>
        <!-- Logo Facebook en noir et blanc -->
         <a href="https://www.instagram.com/grupporosetta" target="_blank" class="inline-block">
          <img src="https://img.icons8.com/ios-filled/50/facebook-new.png" alt="Facebook Rosetta 17" class="w-6 h-6 mx-auto" />
        </a>
      </div>
      <p class="text-sm mb-2">73 Rue de Prony, 75017 Paris</p>
      <p class="text-sm mb-2">01 45 74 54 74</p>
      
      <p class="text-xs text-[#555]">&copy; Groupe Rosetta</p>
    </div>
  </footer>
</template>

<script setup>
// Pas de logique JavaScript nécessaire pour ce footer statique
</script>

<style scoped>
/* Styles spécifiques au footer */
footer {
  background-color: #ffffff;
  color: #1b3b34;
}

footer a {
  color: #1b3b34;
  text-decoration: none;
}

footer a:hover {
  text-decoration: underline;
}

footer .text-xs {
  color: #555;
}
</style>
