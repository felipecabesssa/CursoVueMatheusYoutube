<template>
  <Banner />

  <div class="main-container">
    <h3>Gerenciar pedidos:</h3>
    <Dashboard />
  </div>
</template>

<script>
import Dashboard from '@/components/Dashboard.vue'
import Banner from '@/components/Banner.vue'
export default {
  components: { Dashboard, Banner },
  name: "Pedidos"
}
</script>

<style scoped>
  h3 {
    text-align: center;
    padding-bottom: 10px;
  }
</style>

