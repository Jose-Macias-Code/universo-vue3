<template>
  <footer class="footer">
    <p>
      <span>Project engineered by</span>
      <strong class="author">
        Jose Macias Mendoza
        <ion-icon name="planet-outline" class="icon planet" />
      </strong>
      <span>—</span>
      <a
        href="https://github.com/Jose-Macias-Code/universo-vue3"
        target="_blank"
        rel="noopener noreferrer"
        class="link"
      >
        <ion-icon name="logo-github" class="icon github" />
        View source on GitHub
      </a>
    </p>
  </footer>
</template>

<script>
export default {
  name: "AppFooter",
};
</script>

<style scoped>
.footer {
  width: 100%;
  text-align: center;
  padding: 1.2rem 1rem;
  font-family: "Courier New", Courier, monospace;
  font-size: 0.95rem;
  color: #e0e0e0;
}

.footer p {
  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.footer strong {
  color: #c58dff;
  font-weight: 600;
}

.icon {
  font-size: 1.1rem;
  vertical-align: middle;
}

.icon.heart {
  color: #ff7bac;
}

.icon.planet {
  color: #6dd5fa;
}

.icon.github {
  color: #6dd5fa;
}

.link {
  color: #6dd5fa;
  text-decoration: none;
  display: inline-flex;
  align-items: center;
  gap: 0.3rem;
  transition: color 0.3s ease;
}

.link:hover {
  color: #ffffff;
}

.author {
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
}

@media (max-width: 600px) {
  .footer {
    padding: 1rem;
    font-size: 0.85rem;
  }

  .footer p {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 0.3rem;
    line-height: 1.4;
  }

  .footer strong {
    font-size: 0.95rem;
    display: flex;
    align-items: center;
    gap: 0.3rem;
  }

  .footer span:nth-of-type(2) {
    display: none;
  }

  .link {
    justify-content: center;
    font-size: 0.9rem;
    gap: 0.4rem;
  }

  .icon {
    font-size: 1rem;
  }
}
</style>
