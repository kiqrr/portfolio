<template>
  <q-layout view="lHh Lpr lFf">
    <div id="container">
      <canvas id="canvas"></canvas>
    </div>
    <q-page-container>
      <q-header class="cabecalho q-py-md">
        <q-toolbar>
          <q-toolbar-title>{KIQ}</q-toolbar-title>
          <div class="nav-buttons gt-sm">
            <q-btn class="custom-btn" no-caps flat :label="$t('inicio')" href="#inicio" />
            <q-btn class="custom-btn" no-caps flat :label="$t('sobre')" href="#sobre" />
            <q-btn class="custom-btn" no-caps flat :label="$t('habilidades')" href="#habilidades" />
            <q-icon class="q-ml-sm" name="light_mode" @click="toggleDarkMode" size="1.4rem" />
            <q-select
              v-model="locale"
              :options="localeOptions"
              dense
              borderless
              emit-value
              map-options
              options-dense
              style="min-width: 100px"
              class="q-ml-md"
            />
          </div>
          <!-- Menu hamburguer visível apenas em mobile -->
          <q-btn flat dense round icon="menu" class="lt-md" @click="toggleMenu">
            <q-menu>
              <q-list style="min-width: 200px">
                <q-item clickable v-close-popup href="#inicio">
                  <q-item-section>{{ $t('inicio') }}</q-item-section>
                </q-item>

                <q-item clickable v-close-popup href="#sobre">
                  <q-item-section>{{ $t('sobre') }}</q-item-section>
                </q-item>

                <q-item clickable v-close-popup href="#habilidades">
                  <q-item-section>{{ $t('habilidades') }}</q-item-section>
                </q-item>

                <q-separator />

                <q-item>
                  <q-item-section>
                    <q-icon name="light_mode" @click="toggleDarkMode" />
                  </q-item-section>
                </q-item>

                <q-item>
                  <q-item-section>
                    <q-select
                      v-model="locale"
                      :options="localeOptions"
                      dense
                      borderless
                      emit-value
                      map-options
                      options-dense
                      style="min-width: 100px"
                      id="mobileLanguage"
                    />
                  </q-item-section>
                </q-item>
              </q-list>
            </q-menu>
          </q-btn>
        </q-toolbar>
      </q-header>

      <q-separator id="separador" />

      <div class="content-wrapper margin" id="inicio">
        <span style="font-size: 1.4rem" id="gradient">{{ $t('ocupation') }}</span>
        <h1 class="text-bold responsive">Caique Rodrigues.</h1>
        <p class="text-grey-8 frase">
          {{ $t('frase') }}
        </p>
        <div>
          <div class="q-my-md">
            <q-btn no-caps flat target="_blank" href="https://www.linkedin.com/in/caiquerr/">
              <q-img
                src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/linkedin/linkedin-original.svg"
                width="24px"
                style="margin-right: 8px"
              />
              <span>LinkedIn</span>
            </q-btn>
            <q-btn no-caps flat target="_blank" href="https://github.com/kiqrr">
              <q-img
                src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/github/github-original.svg"
                width="24px"
                style="margin-right: 8px"
              />
              <span>Github</span>
            </q-btn>
            <q-btn
              flat
              no-caps
              target="_blank"
              href="mailto:caiquerr99@gmail.com"
              icon="mail"
              label="Email"
            />
          </div>
        </div>
      </div>

      <q-separator id="separador" />
      <div class="apresentacao margin q-mt-xl" id="sobre">
        <div class="texto-apresentacao">
          <div class="saudacao">{{ $t('hello') }}<span class="waving-hand">👋</span></div>

          <p class="descricao q-mt-md">{{ $t('myName') }}</p>

          <p class="experiencia q-mt-md">
            {{ $t('studying') }}
          </p>

          <p class="experiencia q-mt-md">
            {{ $t('aboutMe') }}
          </p>
        </div>

        <div class="avatar-container">
          <q-img
            src="/portfolio/assets/profilepic.png"
            class="avatar"
            width="300px"
            height="300px"
            style="filter: contrast(131.65%)"
          />
        </div>
      </div>
      <q-separator id="separador" />
      <div class="q-pa-md">
        <q-parallax :height="250" :speed="1.0">
          <template v-slot:media>
            <img
              src="https://readme-typing-svg.herokuapp.com?font=Jersey+15&weight=800&size=22&letterSpacing=0.2rem&duration=8000&pause=1000&color=0DA400C3&background=00010000&center=true&vCenter=true&width=1366&height=800&lines=Wake+up%2C+Neo...;The+Matrix+has+you...;Follow+the+white+rabbit.;Knock%2C+knock%2C+Neo."
            />
          </template>

          <h1 class="text-white"></h1>
        </q-parallax>
      </div>
      <q-separator id="separador" />

      <div class="habilidades margin q-py-xl" id="habilidades">
        <span class="text-h4 q-mb-lg">{{ $t('habilidades') }}</span>
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
          <div class="q-mb-md">
            <span class="text-h6 q-mb-md">{{ $t('other') }}</span>
          </div>
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
              >{{ $t('madeWith') }}<a class="anchor" href="https://vuejs.org/">Vue.JS</a> &
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
import { useI18n } from 'vue-i18n'
const { locale } = useI18n({ useScope: 'global' })

const $q = useQuasar()
$q.dark.set(true)
function toggleDarkMode() {
  $q.dark.toggle()
  document.body.style.backgroundColor = $q.dark.isActive ? '#000000' : '#ffffff'
}

import { onMounted } from 'vue'

onMounted(() => {
  const canvas = document.getElementById('canvas')
  const ctx = canvas.getContext('2d')

  // Configuração inicial do canvas
  canvas.width = window.innerWidth
  canvas.height = window.innerHeight

  // Configuração das letras
  const letters =
    'ABCDEFGHIJKLMNOPQRSTUVXYZABCDEFGHIJKLMNOPQRSTUVXYZABCDEFGHIJKLMNOPQRSTUVXYZABCDEFGHIJKLMNOPQRSTUVXYZABCDEFGHIJKLMNOPQRSTUVXYZABCDEFGHIJKLMNOPQRSTUVXYZ'
  const letterArray = letters.split('')

  // Configuração das colunas
  const fontSize = 10
  const columns = canvas.width / fontSize

  // Configuração das gotas
  const drops = new Array(Math.floor(columns)).fill(1)

  // Função de desenho
  function draw() {
    ctx.fillStyle = $q.dark.isActive ? 'rgba(0, 0, 0, 0.1)' : 'rgba(255, 255, 255, 0.1)'
    ctx.fillRect(0, 0, canvas.width, canvas.height)

    ctx.font = fontSize + 'px monospace'
    ctx.fillStyle = '#0f0'

    for (let i = 0; i < drops.length; i++) {
      const text = letterArray[Math.floor(Math.random() * letterArray.length)]
      ctx.fillText(text, i * fontSize, drops[i] * fontSize)
      drops[i]++

      if (drops[i] * fontSize > canvas.height && Math.random() > 0.95) {
        drops[i] = 0
      }
    }
  }

  // Ajuste do canvas para redimensionamento
  function updateDimensions() {
    canvas.width = window.innerWidth
    canvas.height = window.innerHeight
    drops.length = Math.floor(canvas.width / fontSize)
    drops.fill(1)
  }

  window.addEventListener('resize', updateDimensions)

  // Iniciar animação
  setInterval(draw, 33)
})

const localeOptions = [
  { value: 'en-US', label: 'English' },
  { value: 'pt-BR', label: 'Português' },
]
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

#canvas {
  position: fixed;
  left: 0;
  top: 0;
  z-index: -1;
  width: 100%;
  height: 100%;
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
}

/* Ajuste responsivo */
@media (max-width: 768px) {
  .margin,
  .cabecalho {
    margin-inline: 5%;
  }
}

@media (max-width: 1023px) {
  .gt-sm {
    display: none;
  }
}

@media (min-width: 1024px) {
  .lt-md {
    display: none;
  }
}

.q-menu {
  background: var(--q-dark);
  color: #fff !important;
}

/* Força o texto do menu a permanecer branco em ambos os modos */
.q-menu .q-item #mobileLanguage {
  color: #fff !important;
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
  }

  .avatar-container {
    width: auto;
    margin: 0 auto;
  }

  .responsive {
    font-size: 3.3rem;
    line-height: 100%;
  }

  .frase {
    font-size: 1.5rem;
    line-height: 130%;
  }

  .custom-btn {
    font-size: 0.8rem;
    margin-inline: -0.2rem;
    padding: 0.7rem;
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

.frase {
  font-size: 1.8rem;
}
</style>
