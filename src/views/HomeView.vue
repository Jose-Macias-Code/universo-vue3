<template>
  <div class="home">
    <video autoplay muted loop playsinline class="video-background">
      <source src="../assets/videos/space-background.mp4" type="video/mp4" />
    </video>
    <div class="overlay"></div>
    <div class="content">
      <div class="main">
        <HeroSection />
        <MainButtons />
      </div>
      <Footer />
    </div>
  </div>
</template>

<script>
import HeroSection from "../components/WelcomeUI/HeroSection.vue";
import MainButtons from "../components/WelcomeUI/MainButtons.vue";
import Footer from "../components/WelcomeUI/AppFooter.vue";

export default {
  name: "HomeView",
  components: {
    HeroSection,
    MainButtons,
    Footer,
  },
};
</script>

<style>
html,
body,
#app {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
}

.home {
  position: relative;
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
}

.video-background {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  object-fit: cover;
  z-index: -2;
}

.overlay {
  position: fixed;
  inset: 0;
  background: rgba(0, 0, 0, 0.5);
  z-index: -1;
}

.content {
  position: relative;
  z-index: 1;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  width: 100%;
  height: 100%;
  padding: 1rem;
  box-sizing: border-box;
}

.main {
  flex: 1;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  gap: 2rem;
}

@media (max-width: 650px) {
  .main {
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    gap: 2rem;
    padding-top: 1.5rem;
    flex: 0 0 auto;
  }

  .content {
    padding-top: 1rem;
    padding-bottom: 2rem;
    height: auto;
    min-height: 100vh;
  }
}
</style>
