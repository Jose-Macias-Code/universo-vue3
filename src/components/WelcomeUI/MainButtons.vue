<template>
  <div class="main-buttons fade-in">
    <button class="action-button" @click="goTo('#')">
      <img
        src="../../assets/images/book-home.webp"
        alt="Book"
        class="img-icon"
      />
      <div class="text-group">
        <span class="label">
          <ion-icon name="book-outline" class="inline-icon"></ion-icon>
          Documentation
        </span>
        <p>Explore the Knowledge Nebula</p>
      </div>
    </button>

    <button class="action-button" @click="goTo('#')">
      <img
        src="../../assets/images/rocket-home.webp"
        alt="Rocket"
        class="img-icon"
      />
      <div class="text-group">
        <span class="label">
          <ion-icon name="rocket-outline" class="inline-icon"></ion-icon>
          Missions
        </span>
        <p>Practical challenges to master Vue</p>
      </div>
    </button>

    <button class="action-button" @click="goTo('#')">
      <img
        src="../../assets/images/telescope-home.webp"
        alt="Telescope"
        class="img-icon"
      />
      <div class="text-group">
        <span class="label">
          <ion-icon name="telescope-outline" class="inline-icon"></ion-icon>
          Observatory
        </span>
        <p>Resources and tools for your cosmic journey</p>
      </div>
    </button>
  </div>
</template>

<script>
export default {
  name: "MainButtons",
  methods: {
    goTo(path) {
      this.$router.push(path);
    },
  },
};
</script>

<style scoped>
.main-buttons {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  align-items: flex-end;
  justify-content: center;
  width: 100%;
  padding-right: 4rem;
}

.action-button {
  display: flex;
  align-items: center;
  background: linear-gradient(
    145deg,
    rgba(255, 255, 255, 0.05),
    rgba(255, 255, 255, 0.1)
  );
  border: 2px solid rgba(255, 255, 255, 0.15);
  backdrop-filter: blur(12px);
  color: white;
  padding: 1.2rem 1.6rem;
  border-radius: 1rem;
  max-width: 460px;
  width: 100%;
  cursor: pointer;
  transition: transform 0.3s ease, box-shadow 0.3s ease, border-color 0.3s ease;
  box-shadow: 0 0 8px rgba(144, 104, 255, 0.2);
}

.action-button:hover {
  transform: translateY(-3px);
  border-color: rgba(255, 255, 255, 0.3);
  box-shadow: 0 12px 25px rgba(171, 101, 255, 0.25),
    0 0 20px rgba(120, 80, 220, 0.2);
}

.img-icon {
  width: 44px;
  height: 44px;
  margin-right: 1rem;
  filter: drop-shadow(0 0 4px rgba(255, 255, 255, 0.15));
  transition: transform 0.3s ease;
}

.action-button:hover .img-icon {
  transform: scale(1.05);
}

.inline-icon {
  font-size: 1rem;
  margin-right: 0.5rem;
  vertical-align: middle;
  color: #c58dff;
}

.text-group {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.label {
  font-size: 1rem;
  font-weight: 600;
  margin-bottom: 0.25rem;
  display: flex;
  align-items: center;
  letter-spacing: 0.3px;
}

.text-group p {
  margin: 0;
  font-size: 0.9rem;
  line-height: 1.3;
  opacity: 0.85;
  color: #e0e0e0;
}

.fade-in {
  animation: fadeSlideIn 0.8s ease-out forwards;
  opacity: 0;
}

.fade-in {
  animation: fadeSlideZoomIn 1s ease-out forwards;
  opacity: 0;
  transform: translateY(20px) scale(0.98);
}

.fade-in {
  animation: fadeSlideElegant 0.8s cubic-bezier(0.25, 0.8, 0.25, 1) forwards;
  opacity: 0;
  transform: translateY(20px);
}

@keyframes fadeSlideElegant {
  0% {
    opacity: 0;
    transform: translateY(20px);
    filter: blur(1px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
    filter: blur(0);
  }
}

@media (max-width: 768px) {
  .main-buttons {
    align-items: center;
    padding: 0 1rem;
    gap: 1.5rem;
    width: 90%;
  }

  .action-button {
    display: grid;
    grid-template-columns: auto 1fr;
    align-items: center;
    justify-content: start;
    width: 100%;
    max-width: 100%;
    padding: 1rem 1.25rem;
    border-radius: 0.75rem;
    gap: 1rem;
  }

  .img-icon {
    width: 36px;
    height: 36px;
    justify-self: start;
    align-self: center;
    margin-right: 0rem;
    flex-shrink: 0;
  }

  .text-group {
    display: flex;
    flex-direction: column;
    gap: 0.25rem;
    align-items: flex-start;
  }

  .label {
    font-size: 0.95rem;
    font-weight: 600;
    line-height: 1.2;
    color: #ffffff;
  }

  .text-group p {
    font-size: 0.85rem;
    text-align: left;
    line-height: 1.5;
    opacity: 0.9;
    color: #e0e0e0;
  }
}
</style>
