<script setup lang="ts">
import { useCartStore } from './stores/cart';
import { onMounted } from "vue"


const cart = useCartStore()

onMounted(() => {
  cart.loadFromStorage()
})

</script>

<template>
  Panier : {{cart.items.length}} élément(s)
  <router-view />
</template>

