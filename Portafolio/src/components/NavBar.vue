<template>
  <header>
    <div class="perfil">
      <img :src="profileImage" alt="Foto de Gabriel Soria" />
    </div>
    <h1>Gabriel Soria - Técnico en Programación</h1>
    <nav>
      <a href="#sobre-mi" class="nav-btn">
        <img :src="circleUserIcon" alt="icono" /> Sobre mi
      </a>
      <a href="#experiencia" class="nav-btn">
        <img :src="briefcaseIcon" alt="icono" /> Experiencia
      </a>
      <a href="#estudios" class="nav-btn">
        <img :src="universityIcon" alt="icono" /> Estudios
      </a>
      <a href="#proyectos" class="nav-btn">
        <img :src="folderIcon" alt="icono" /> Proyectos
      </a>
      <a href="#contacto" class="nav-btn">
        <img :src="phoneIcon" alt="icono" /> Contacto
      </a>
    </nav>
  </header>
</template>

<script>
// Importar imágenes desde src/assets
import profileImage from '../assets/images/imagen cv.jpg'
import circleUserIcon from '../assets/icons/circle-user-svgrepo-com.svg'
import briefcaseIcon from '../assets/icons/briefcase-alt-svgrepo-com.svg'
import universityIcon from '../assets/icons/university-svgrepo-com.svg'
import folderIcon from '../assets/icons/folder-svgrepo-com.svg'
import phoneIcon from '../assets/icons/phone-svgrepo-com.svg'

export default {
  name: 'NavBar',
  data() {
    return {
      profileImage,
      circleUserIcon,
      briefcaseIcon,
      universityIcon,
      folderIcon,
      phoneIcon
    }
  }
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  flex-wrap: wrap;
  background-color: rgba(46, 61, 31, 0.9);
}

.perfil {
  display: flex;
  align-items: center;
}

.perfil img {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  object-fit: cover;
  border: 2px solid #B4C8B2;
}

header h1 {
  font-size: 1.5rem;
  text-align: center;
  flex-grow: 1;
  margin: 0 1rem;
}

nav {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  justify-content: center;
}

.nav-btn {
  display: flex;
  align-items: center;
  gap: 0.4rem;
  background-color: #B4C8B2;
  color: #2E4E1C;
  padding: 0.5rem 1rem;
  border-radius: 4px;
  text-decoration: none;
  font-weight: 600;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.nav-btn::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
  transition: left 0.5s;
}

.nav-btn:hover {
  background-color: #A0B5A0;
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.nav-btn:hover::before {
  left: 100%;
}

.nav-btn img {
  width: 20px;
  height: 20px;
}

@media (max-width: 768px) {
  header {
    flex-direction: column;
    align-items: center;
    gap: 1rem;
  }
  
  header h1 {
    margin: 0;
    text-align: center;
  }
  
  nav {
    width: 100%;
    justify-content: center;
  }
  
  .nav-btn {
    flex: 1 1 auto;
    justify-content: center;
    min-width: 120px;
  }
}

@media (max-width: 600px) {
  .nav-btn {
    flex: 1 1 100%;
    justify-content: center;
  }
}
</style>