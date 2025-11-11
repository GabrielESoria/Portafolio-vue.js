<template>
  <div id="app">
    <NavBar />
    <main>
      <section id="sobre-mi">
        <h2><img :src="circleUserIcon" alt="icono">Sobre mi</h2>
        <p>Soy Gabriel Soria, estudiante de Tecnicatura en Programación en la Facultad Regional San Rafael de la UTN. Inicié mi formación académica en la Tecnicatura en Higiene y Seguridad, donde desarrollé una fuerte capacidad analítica y una mirada crítica sobre los sistemas y procesos. Esa base despertó mi interés por la programación, impulsándome a reconvertirme profesionalmente hacia el desarrollo de software.</p>
      </section>

      <section id="experiencia">
        <h2><img :src="briefcaseIcon" alt="icono">Experiencia</h2>
        <ul>
          <li>Desarrollo de sistemas de reservas con PSeInt</li>
        </ul>
      </section>

      <section id="estudios">
        <h2><img :src="universityIcon" alt="icono">Estudios</h2>
        <ul>
          <li>Tecnicatura Superior en Higiene y Seguridad Laboral</li>
          <li>Cursando 1er año de Tecnicatura en Programación</li>
        </ul>
      </section>

      <section id="proyectos">
        <h2><img :src="folderIcon" alt="icono">Proyectos</h2>
        <ul>
          <li>Simulador de compra de entradas para cine</li>
        </ul>
      </section>

      <section id="contacto">
        <h2><img :src="phoneIcon" alt="icono">Contacto</h2>
        <p>Podes contactarme a <strong>gabrieledgardosoria26@gmail.com</strong> o conectarte vía LinkedIn.</p>
      </section>
    </main>
    <Footer />
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import Footer from './components/Footer.vue'

// Importar iconos desde src/assets/icons
import circleUserIcon from './assets/icons/circle-user-svgrepo-com.svg'
import briefcaseIcon from './assets/icons/briefcase-alt-svgrepo-com.svg'
import universityIcon from './assets/icons/university-svgrepo-com.svg'
import folderIcon from './assets/icons/folder-svgrepo-com.svg'
import phoneIcon from './assets/icons/phone-svgrepo-com.svg'

export default {
  name: 'App',
  components: {
    NavBar,
    Footer
  },
  data() {
    return {
      circleUserIcon,
      briefcaseIcon,
      universityIcon,
      folderIcon,
      phoneIcon
    }
  }
}
</script>

<style>
/* Estilos generales */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html, body {
  scroll-behavior: smooth;
}

body {
  font-family: 'Quicksand', sans-serif;
  background-color: #3B5323; 
  color: #fff;
  line-height: 1.6;
}

#app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

main {
  max-width: 900px;
  margin: 2rem auto;
  padding: 0 1rem;
  flex-grow: 1;
}

section {
  margin-bottom: 3rem;
  padding: 1.5rem;
  background: rgba(255, 255, 255, 0.05);
  border-radius: 8px;
  transition: transform 0.3s ease;
}

section:hover {
  transform: translateY(-5px);
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

section h2 {
  font-size: 1.6rem;
  margin-bottom: 1rem;
  display: flex;
  align-items: center;
  gap: 0.5rem;
  color: #B4C8B2;
}

section h2 img {
  width: 26px;
  height: 26px;
}

section p, section ul {
  padding: 1rem;
  border-radius: 4px;
}

ul {
  list-style: disc inside;
}

@media (max-width: 600px) {
  section {
    padding: 1rem;
  }
}
</style>