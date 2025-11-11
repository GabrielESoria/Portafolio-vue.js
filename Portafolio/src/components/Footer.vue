<template>
  <footer>
    <div class="footer-social">
      <a href="https://github.com/GabrielESoria" target="_blank">
        <img :src="githubIcon" alt="GitHub"> GitHub
      </a>
      <a href="https://www.linkedin.com/in/gabriel-soria-845ba8269/" target="_blank">
        <img :src="linkedinIcon" alt="LinkedIn"> LinkedIn
      </a>
    </div>
    <div class="footer-legal">
      © 2025 Gabriel Soria — Todos los derechos reservados.
    </div>
  </footer>
</template>

<script>
import githubIcon from '../assets/icons/github-142-svgrepo-com.svg'
import linkedinIcon from '../assets/icons/linkedin-rounded-svgrepo-com.svg'

export default {
  name: 'Footer',
  data() {
    return {
      githubIcon,
      linkedinIcon
    }
  }
}
</script>

<style scoped>
.footer-social {
  background-color: #2E3D1F;
  padding: 1rem;
  display: flex;
  justify-content: center;
  gap: 2rem;
  flex-wrap: wrap;
}

.footer-social a {
  color: #fff;
  display: flex;
  align-items: center;
  text-decoration: none;
  gap: 0.5rem;
  font-weight: 600;
  transition: all 0.3s ease;
}

.footer-social a:hover {
  transform: scale(1.1);
}

.footer-social img {
  width: 22px;
  height: 22px;
}

.footer-legal {
  background-color: #1D2612;
  text-align: center;
  padding: 1rem;
  font-size: 0.9rem;
}

@media (max-width: 768px) {
  .footer-social {
    flex-direction: column;
    gap: 1rem;
    align-items: center;
  }
}
</style>