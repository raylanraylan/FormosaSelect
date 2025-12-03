<script setup lang="ts">
const products = ref([{
  name:'多功能貓跳台',
  vendor:'台灣毛孩',
  descriptions:'結合貓抓柱、跳台、貓窩等多功能設計，採用天然劍麻繩與環保木材，為您家的毛小孩打造一個專屬的玩樂與休息空間。',
  id:1
}, {
  name: '智能寵物餵食器',
  vendor: '台灣毛孩',
  descriptions: '定時定量，遠端遙控，讓您的毛小孩飲食規律又健康。支援手機APP操作，隨時隨地都能關心您的寵物。',
  id:2
}, {
  name: '寵物專用空氣清淨機',
  vendor: '台灣毛孩',
  descriptions: '有效過濾寵物毛髮、異味與過敏原，提供您與毛小孩一個清新舒適的居住環境。超靜音設計，不打擾寵物休息。',
  id:3
}, {
  name: '天然貓草玩具組',
  vendor: '台灣毛孩',
  descriptions: '內含多種造型的貓草填充玩具，採用100%天然貓草，能有效紓解貓咪壓力，增加活動量，是貓咪的最佳玩伴。',
  id:4
}]);
</script>
<template>
  <h1>邊做邊學Nuxt</h1>
  <div class="flex" v-for="product in products" :key="product.id">
    <NuxtLink :to="{ name:'stores-id',params: { id: product.id} }">
      <div>
        <!-- <NuxtImg :src="`/products/${product.id}.jpg`" :alt="product.name" width="300" height="300" /> -->
      </div>
        <h2>{{ product.name }}</h2>
        <h3>{{ product.vendor }}</h3>
        <p>{{ product.descriptions }}</p>
    </NuxtLink>
  </div>
</template>