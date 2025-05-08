<template>
  <div class="planeta">
    <h2>🪐 Planeta: {{ $route.params.id }}</h2>
    <router-link to="/">← Volver al Home</router-link>
  </div>
</template>

<script>
export default {
  name: "PlanetaView",
};
</script>
