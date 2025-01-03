<template>
  <q-layout view="lHh Lpr lFf" class="grid-background">
    <q-page-container>
      <q-header class="cabecalho q-py-md">
        <q-toolbar>
          <q-toolbar-title>{KIQ}</q-toolbar-title>
          <div class="nav-buttons">
            <q-btn class="custom-btn" flat label="Inicio" href="#inicio" />
            <q-btn class="custom-btn" flat label="Sobre" href="#sobre" />
            <q-btn class="custom-btn" flat label="Habilidades" href="#habilidades" />
            <q-icon name="light_mode" @click="toggleDarkMode" size="1.4rem" />
          </div>
        </q-toolbar>
      </q-header>

      <q-separator id="separador" />

      <div class="content-wrapper margin" id="inicio">
        <span class="text-subtitle1 text-green" id="gradient">Desenvolvedor Full Stack</span>
        <h1 class="text-bold">Caique Rodrigues.</h1>
        <p class="text-h4 text-grey-8">
          Criando e otimizando código de alto desempenho, com foco em metodologias ágeis.
        </p>
      </div>

      <q-separator id="separador" />
      <div class="apresentacao margin q-mt-xl" id="sobre">
        <div class="texto-apresentacao">
          <div class="saudacao">Olá <span class="waving-hand">👋</span></div>

          <p class="descricao q-mt-md">Meu nome é Caique Rodrigues, tenho 25 anos. 🇧🇷</p>

          <p class="experiencia q-mt-md">
            Atualmente estou cursando Desenvolvimento de Sistemas no Senai.
          </p>

          <p class="experiencia q-mt-md">
            Sou apaixonado por tecnologia desde criança e atualmente tenho me dedicado a me tornar
            um programador cada vez mais experiente e capacitado para atender as demandas do mercado
            com maestria, para isso estou sempre me atualizando fazendo cursos de programação e
            pesquisando assuntos relacionadas a tecnologia em paralelo.
          </p>

          <p class="chamada q-mt-xl text-grey-6">My name is Caique Rodrigues, I'm 25 years old.</p>

          <p class="chamada q-mt-md text-grey-6">
            I'm currently studying Systems Development at Senai São Paulo.
          </p>

          <p class="chamada q-mt-md text-grey-6">
            I have been passionate about technology since I was a child and currently I have
            dedicated myself to becoming an increasingly programmer experienced and qualified to
            meet market demands with mastery, so I am always updating myself taking programming
            courses and researching technology-related subjects in parallel.
          </p>
        </div>

        <div class="avatar-container">
          <q-img src="src/assets/profilepic.png" class="avatar" width="300px" height="300px" />
        </div>
      </div>
      <q-separator id="separador" />

      <div class="habilidades margin q-py-xl" id="habilidades">
        <h2 class="text-h4 q-mb-lg">HABILIDADES</h2>

        <!-- Backend Section -->
        <div class="categoria q-mb-xl">
          <h3 class="text-h6 q-mb-md">Backend</h3>
          <div class="skills-grid">
            <q-card flat bordered class="skill-card">
              <q-card-section class="flex items-center">
                <img
                  src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg"
                  alt="Python"
                  class="skill-icon"
                />
                <span class="q-ml-sm">Python</span>
              </q-card-section>
            </q-card>

            <q-card flat bordered class="skill-card">
              <q-card-section class="flex items-center">
                <img
                  src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/django/django-plain.svg"
                  alt="Django"
                  class="skill-icon"
                />
                <span class="q-ml-sm">Django</span>
              </q-card-section>
            </q-card>

            <q-card flat bordered class="skill-card">
              <q-card-section class="flex items-center">
                <img
                  src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg"
                  alt="Node.js"
                  class="skill-icon"
                />
                <span class="q-ml-sm">Node.js</span>
              </q-card-section>
            </q-card>

            <q-card flat bordered class="skill-card">
              <q-card-section class="flex items-center">
                <img
                  src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg"
                  alt="MySQL"
                  class="skill-icon"
                />
                <span class="q-ml-sm">MySQL</span>
              </q-card-section>
            </q-card>
          </div>
          <div class="skills-grid q-mt-md">
            <q-card flat bordered class="skill-card">
              <q-card-section class="flex items-center">
                <img
                  src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/lua/lua-original.svg"
                  alt="Lua"
                  class="skill-icon"
                />
                <span class="q-ml-sm">Lua</span>
              </q-card-section>
            </q-card>
          </div>
        </div>

        <!-- Frontend Section -->
        <div class="categoria q-mb-xl">
          <h3 class="text-h6 q-mb-md">Frontend</h3>
          <div class="skills-grid">
            <q-card flat bordered class="skill-card">
              <q-card-section class="flex items-center">
                <img
                  src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg"
                  alt="JavaScript"
                  class="skill-icon"
                />
                <span class="q-ml-sm">JavaScript</span>
              </q-card-section>
            </q-card>

            <q-card flat bordered class="skill-card">
              <q-card-section class="flex items-center">
                <img
                  src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg"
                  alt="Vue.js"
                  class="skill-icon"
                />
                <span class="q-ml-sm">Vue.js</span>
              </q-card-section>
            </q-card>

            <q-card flat bordered class="skill-card">
              <q-card-section class="flex items-center">
                <img
                  src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/quasar/quasar-original.svg"
                  alt="Quasar"
                  class="skill-icon"
                />
                <span class="q-ml-sm">Quasar</span>
              </q-card-section>
            </q-card>
            <q-card flat bordered class="skill-card">
              <q-card-section class="flex items-center">
                <img
                  src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg"
                  alt="HTML5"
                  class="skill-icon"
                />
                <span class="q-ml-sm">HTML5</span>
              </q-card-section>
            </q-card>
          </div>
          <div class="skills-grid q-mt-md">
            <q-card flat bordered class="skill-card">
              <q-card-section class="flex items-center">
                <img
                  src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg"
                  alt="CSS3"
                  class="skill-icon"
                />
                <span class="q-ml-sm">CSS3</span>
              </q-card-section>
            </q-card>
          </div>
        </div>
        <!-- Frontend Section -->
        <div class="categoria q-mb-xl">
          <h3 class="text-h6 q-mb-md">Outros</h3>
          <div class="skills-grid">
            <q-card flat bordered class="skill-card">
              <q-card-section class="flex items-center">
                <img
                  src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg"
                  alt="Docker"
                  class="skill-icon"
                />
                <span class="q-ml-sm">Docker</span>
              </q-card-section>
            </q-card>

            <q-card flat bordered class="skill-card">
              <q-card-section class="flex items-center">
                <img
                  src="https://static.thenounproject.com/png/7329229-512.png"
                  alt="Kanban"
                  class="skill-icon"
                />
                <span class="q-ml-sm">Kanban</span>
              </q-card-section>
            </q-card>

            <q-card flat bordered class="skill-card">
              <q-card-section class="flex items-center">
                <img
                  src="https://static.thenounproject.com/png/376069-512.png"
                  alt="Scrum"
                  class="skill-icon"
                />
                <span class="q-ml-sm">Scrum</span>
              </q-card-section>
            </q-card>

            <q-card flat bordered class="skill-card">
              <q-card-section class="flex items-center">
                <img
                  src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg"
                  alt="Github"
                  class="skill-icon"
                />
                <span class="q-ml-sm">Github</span>
              </q-card-section>
            </q-card>
          </div>
          <div class="skills-grid q-mt-md">
            <q-card flat bordered class="skill-card">
              <q-card-section class="flex items-center">
                <img
                  src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg"
                  alt="Figma"
                  class="skill-icon"
                />
                <span class="q-ml-sm">Figma</span>
              </q-card-section>
            </q-card>
          </div>
        </div>
      </div>
      <q-separator id="separador" />
      <div>
        <q-footer class="cabecalho q-py-md">
          <q-toolbar>
            <q-toolbar-title style="font-size: smaller">© 2025 Caique Rodrigues</q-toolbar-title>
            <span style="font-size: smaller"
              >Feito com <a class="anchor" href="https://vuejs.org/">Vue.JS</a> e
              <a class="anchor" href="https://quasar.dev/">Quasar.dev</a></span
            >
          </q-toolbar>
        </q-footer>
      </div>
    </q-page-container>
  </q-layout>
</template>

<script setup>
import { useQuasar } from 'quasar'

const $q = useQuasar()
function toggleDarkMode() {
  $q.dark.toggle()
}
</script>

<style>
.margin {
  margin-inline: 20%;
}
.cabecalho {
  background-color: rgba(255, 255, 255, 0);
  margin-inline: 20%;
  position: absolute;
}

/* Controle do grid em modo claro/escuro */
.grid-background:before {
  background-image: url(src/assets/grid.svg);
  background-repeat: repeat;
  content: '';
  height: 100%;
  inset: 0;
  pointer-events: none;
  position: absolute;
  width: 100%;
  z-index: -1;
}

/* Modo claro */
.body--light .grid-background:before {
  opacity: 0.4;
  filter: invert(100%);
}

/* Modo escuro */
.body--dark .grid-background:before {
  opacity: 0.2;
}

/* Controle das cores dos botões */
.body--light .custom-btn {
  color: #000;
}

.body--dark .custom-btn {
  color: #fff;
}

/* Controle das cores dos botões */
.body--light .cabecalho {
  color: #000;
}

.content-wrapper {
  display: flex;
  flex-direction: column;
  gap: 0.1rem;
  padding: 2rem 0;
}

#gradient {
  background: linear-gradient(90deg, #00ff62, #00eeff, #00c3ff, #006eff, #0000ff, #4b0082, #8b00ff);
  background-size: 100%;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-size: 2.5rem;
  font-weight: bold;
  margin: 0; /* Remove margin-top excessiva */
}

.nav-buttons {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.text-subtitle1 {
  margin: 0;
  line-height: 1.5;
}

/* Ajuste responsivo */
@media (max-width: 768px) {
  .margin,
  .cabecalho {
    margin-inline: 5%;
  }
}

#separador {
  margin-inline: 20%;
}
</style>

<style scoped>
.apresentacao {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 2rem;
  padding: 2rem 0;
}

.texto-apresentacao {
  flex: 1;
}

.saudacao {
  font-size: 2rem;
  font-weight: bold;
}

.waving-hand {
  display: inline-block;
  animation: wave 2.5s infinite;
  transform-origin: 70% 70%;
}

.avatar-container {
  flex-shrink: 0;
}

.avatar {
  border-radius: 50%;
  background: linear-gradient(145deg, #1a1a1a, #2a2a2a);
}

@keyframes wave {
  0% {
    transform: rotate(0deg);
  }
  10% {
    transform: rotate(14deg);
  }
  20% {
    transform: rotate(-8deg);
  }
  30% {
    transform: rotate(14deg);
  }
  40% {
    transform: rotate(-4deg);
  }
  50% {
    transform: rotate(10deg);
  }
  60% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(0deg);
  }
}

@media (max-width: 768px) {
  .apresentacao {
    flex-direction: column-reverse;
    text-align: center;
  }

  .avatar-container {
    width: 200px;
    margin: 0 auto;
  }
}
</style>

<style scoped>
.habilidades {
  color: inherit;
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1rem;
}

.skill-card {
  background: rgba(255, 255, 255, 0.05);
  transition: all 0.3s ease;
}

.skill-card:hover {
  transform: translateY(-5px);
  background: rgba(255, 255, 255, 0.1);
}

.skill-icon {
  width: 24px;
  height: 24px;
}

@media (max-width: 768px) {
  .skills-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 480px) {
  .skills-grid {
    grid-template-columns: 1fr;
  }
}

.anchor {
  color: #00ff62;
  text-decoration: none;
}
</style>
