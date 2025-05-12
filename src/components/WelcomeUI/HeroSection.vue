<template>
  <div class="hero">
    <img
      src="../../assets/images/hero-title.webp"
      alt="Welcome to the Universe Vue 3"
      class="hero-image"
    />
  </div>
</template>

<script>
export default {
  name: "HeroSection",
};
</script>

<style scoped>
.hero {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  width: 100%;
  height: 100%;
  padding-left: 2rem;
  box-sizing: border-box;
}

.hero-image {
  width: 100%;
  max-width: 500px;
  height: auto;
  object-fit: contain;
  animation-delay: 0.4s, 1s;
  filter: drop-shadow(0 0 6px rgba(109, 213, 250, 0.3))
    drop-shadow(0 0 12px rgba(41, 128, 185, 0.25));
  transition: transform 0.3s ease, opacity 0.3s ease;
}

@keyframes galacticGlow {
  0% {
    filter: drop-shadow(0 0 4px rgba(109, 213, 250, 0.2))
      drop-shadow(0 0 8px rgba(41, 128, 185, 0.15));
  }
  100% {
    filter: drop-shadow(0 0 10px rgba(109, 213, 250, 0.35))
      drop-shadow(0 0 24px rgba(41, 128, 185, 0.3));
  }
}

@media (max-width: 768px) {
  .hero {
    justify-content: center;
    padding-left: 0;
  }

  .hero-image {
    max-width: 200px;
  }
}
</style>
