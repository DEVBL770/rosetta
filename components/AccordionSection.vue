<template>
  <div class="border-b border-[#ddd] py-4">
    <button
      @click="open = !open"
      class="w-full text-left flex justify-between items-center font-semibold text-xl text-[#1b3b34] hover:text-[#a16c4f] transition"
    >
      {{ title }}
      <span class="text-2xl transition" :class="{ 'rotate-180': open }">⌄</span>
    </button>

    <transition name="fade">
      <div v-if="open" class="mt-4 space-y-6">
        <MenuItem
          v-for="(item, i) in items"
          :key="i"
          :name="item.name"
          :description="item.description"
          :price="item.price"
        />
        <div v-if="addons?.length" class="mt-4 pl-4 text-sm text-[#555] border-t border-dashed pt-2">
          <p class="font-semibold text-center text-[#1b3b34] mb-2">Suppléments :</p>
          <ul class="space-y-1">
            <li
              v-for="(addon, j) in addons"
              :key="j"
              class="flex justify-between text-[#777]"
            >
              <span>- {{ addon.name }}</span>
              <span class="text-[#a16c4f] font-medium">{{ addon.price }}</span>
            </li>
          </ul>
        </div>
      </div>
    </transition>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import MenuItem from './MenuItem.vue'

defineProps(['title', 'items', 'addons'])
const open = ref(false)
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: all 0.3s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
  transform: translateY(-5px);
}
</style>
