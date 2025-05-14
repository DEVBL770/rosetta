<template>
  <section class="mb-12">
    <h2 class="text-2xl font-semibold mb-6 text-[#264c44] border-b border-[#c4b9b3] pb-2">{{ title }}</h2>

    <div class="space-y-6">
      <MenuItem
        v-for="(item, index) in items"
        :key="index"
        :name="item.name"
        :description="item.description"
        :price="item.price"
      />

      <!-- Suppléments (s'ils existent) -->
      <div v-if="addons?.length" class="mt-6 text-sm text-[#555]">
        <p class="font-semibold text-[#1b3b34] mb-2">Suppléments :</p>
        <ul class="space-y-1">
          <li v-for="(addon, i) in addons" :key="i" class="flex justify-between border-b border-dashed border-[#e1dad5] pb-1">
            <span>- {{ addon.name }}</span>
            <span class="text-[#a16c4f] font-medium">{{ addon.price }}+</span>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script setup>
import MenuItem from './MenuItem.vue'
defineProps(['title', 'items', 'addons'])
</script>
