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
            <q-btn
              class="custom-btn"
              no-caps
              flat
              :label="$t('certificados')"
              href="#certificados"
            />
            <q-btn class="custom-btn" no-caps flat :label="$t('projetos')" href="#projetos" />
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
                src="https://www.svgrepo.com/show/475654/github-color.svg"
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
            <q-btn
              no-caps
              flat
              target="_blank"
              href="https://www.credly.com/users/caique-rodrigues.aa2822e2"
            >
              <q-img
                src="https://www.svgrepo.com/show/331358/credly.svg"
                width="24px"
                style="margin-right: 8px"
              />
              <span>Credly</span>
            </q-btn>
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
                  src="https://www.svgrepo.com/show/475654/github-color.svg"
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

      <div class="certificados margin q-py-xl" id="certificados">
        <span class="text-h4 q-mb-lg">{{ $t('certificados') }}</span>
        <div class="certificates-grid q-mt-md">
          <!-- Cisco - English for IT 1 -->
          <q-card flat bordered class="certificate-card">
            <q-img src="/portfolio/assets/english_for_it_1.png" height="200px" class="certificate-image" />
            <q-card-section>
              <div class="text-h6">English for IT 1</div>
              <div class="text-subtitle2">Cisco</div>
              <div class="text-caption">Dezembro 2024</div>
              <div class="text-caption q-mt-sm">
                Competências: Inglês técnico, Terminologia de TI, Comunicação técnica
              </div>
            </q-card-section>
            <q-card-actions>
              <q-btn
                flat
                :label="$t('see_certificate')"
                @click="
                  showCertificate({
                    imgPath: '/portfolio/assets/english_for_it_1.png',
                    linkVerificacao:
                      'https://www.credly.com/badges/653290c1-1be0-4b1d-b434-67256fa7d17d/linked_in_profile',
                  })
                "
              />
            </q-card-actions>
          </q-card>

          <!-- Senai - Fundamentos do Python -->
          <q-card flat bordered class="certificate-card">
            <q-img
              src="/portfolio/assets/fundamentos_do_python_1.jfif"
              height="200px"
              class="certificate-image"
            />
            <q-card-section>
              <div class="text-h6">Fundamentos do Python 1</div>
              <div class="text-subtitle2">Senai São Paulo</div>
              <div class="text-caption">Dezembro 2024</div>
              <div class="text-caption q-mt-sm">
                Competências: Python, Raciocínio lógico, Organização
              </div>
            </q-card-section>
            <q-card-actions>
              <q-btn
                flat
                :label="$t('see_certificate')"
                @click="
                  showCertificate({
                    imgPath: '/portfolio/assets/fundamentos_do_python_1.jfif',
                    linkVerificacao:
                      'https://www.sp.senai.br/consulta-certificado?qrcode=11324276446/14814334',
                  })
                "
              />
            </q-card-actions>
          </q-card>

          <!-- Cisco - JavaScript Essentials 1 -->
          <q-card flat bordered class="certificate-card">
            <q-img
              src="/portfolio/assets/javascript_essentials_1.png"
              height="200px"
              class="certificate-image"
            />
            <q-card-section>
              <div class="text-h6">JavaScript Essentials 1</div>
              <div class="text-subtitle2">Cisco</div>
              <div class="text-caption">Dezembro 2024</div>
              <div class="text-caption q-mt-sm">
                Competências: JavaScript básico, Lógica de programação, Desenvolvimento web frontend
              </div>
            </q-card-section>
            <q-card-actions>
              <q-btn
                flat
                :label="$t('see_certificate')"
                @click="
                  showCertificate({
                    imgPath: '/portfolio/assets/javascript_essentials_1.png',
                    linkVerificacao:
                      'https://www.credly.com/badges/912b6c79-e360-46e5-bbe4-ea88dc389986/linked_in_profile',
                  })
                "
              />
            </q-card-actions>
          </q-card>

          <!-- Cisco - JavaScript Essentials 2 -->
          <q-card flat bordered class="certificate-card">
            <q-img
              src="/portfolio/assets/javascript_essentials_2.png"
              height="200px"
              class="certificate-image"
            />
            <q-card-section>
              <div class="text-h6">JavaScript Essentials 2</div>
              <div class="text-subtitle2">Cisco</div>
              <div class="text-caption">Dezembro 2024</div>
              <div class="text-caption q-mt-sm">
                Competências: JavaScript avançado, DOM manipulation, Programação orientada a objetos
              </div>
            </q-card-section>
            <q-card-actions>
              <q-btn
                flat
                :label="$t('see_certificate')"
                @click="
                  showCertificate({
                    imgPath: '/portfolio/assets/javascript_essentials_2.png',
                    linkVerificacao:
                      'https://www.credly.com/badges/16cb9599-91a5-4ffb-8ffa-2c4a0ed2d4e4/linked_in_profile',
                  })
                "
              />
            </q-card-actions>
          </q-card>

          <!-- Codecademy - Learn Python 3 -->
          <q-card flat bordered class="certificate-card">
            <q-img
              src="/portfolio/assets/learn_python_3_course.jfif"
              height="200px"
              class="certificate-image"
            />
            <q-card-section>
              <div class="text-h6">Learn Python 3 Course</div>
              <div class="text-subtitle2">Codecademy</div>
              <div class="text-caption">Dezembro 2024</div>
              <div class="text-caption q-mt-sm">Competências: Python</div>
            </q-card-section>
            <q-card-actions>
              <q-btn
                flat
                :label="$t('see_certificate')"
                @click="
                  showCertificate({
                    imgPath: '/portfolio/assets/learn_python_3_course.jfif',
                    linkVerificacao:
                      'https://www.codecademy.com/profiles/bit0626256187/certificates/6c152bd262967f8c941c9707ed636bda',
                  })
                "
              />
            </q-card-actions>
          </q-card>

          <!-- IBM - Web Development -->
          <q-card flat bordered class="certificate-card">
            <q-img
              src="/portfolio/assets/web_development_fundamentals.jfif"
              height="200px"
              class="certificate-image"
            />
            <q-card-section>
              <div class="text-h6">Web Development Fundamentals</div>
              <div class="text-subtitle2">IBM</div>
              <div class="text-caption">Dezembro 2024</div>
              <div class="text-caption q-mt-sm">
                Competências: HTML, CSS, JavaScript, Desenvolvimento web
              </div>
            </q-card-section>
            <q-card-actions>
              <q-btn
                flat
                :label="$t('see_certificate')"
                @click="
                  showCertificate({
                    imgPath: '/portfolio/assets/web_development_fundamentals.jfif',
                    linkVerificacao:
                      'https://www.credly.com/badges/cf001a2d-ac5d-454d-b771-e224c928e19f/linked_in_profile',
                  })
                "
              />
            </q-card-actions>
          </q-card>

          <!-- Google Cloud -->
          <q-card flat bordered class="certificate-card">
            <q-img
              src="/portfolio/assets/google_cloud_computing_foundations_certificate.png"
              height="200px"
              class="certificate-image"
            />
            <q-card-section>
              <div class="text-h6">Google Cloud Computing Foundations</div>
              <div class="text-subtitle2">Google</div>
              <div class="text-caption">Novembro 2024</div>
              <div class="text-caption q-mt-sm">
                Competências: Computação em nuvem, Google Cloud Platform, Infraestrutura em nuvem
              </div>
            </q-card-section>
            <q-card-actions>
              <q-btn
                flat
                :label="$t('see_certificate')"
                @click="
                  showCertificate({
                    imgPath: '/portfolio/assets/google_cloud_computing_foundations_certificate.png',
                    linkVerificacao:
                      'https://www.credly.com/badges/3f0317df-acb6-4f9c-b88d-1402876a08b7/linked_in_profile',
                  })
                "
              />
            </q-card-actions>
          </q-card>

          <!-- SENAI - Excel -->
          <q-card flat bordered class="certificate-card">
            <q-img src="/portfolio/assets/excel_basico.jfif" height="200px" class="certificate-image" />
            <q-card-section>
              <div class="text-h6">Excel Básico</div>
              <div class="text-subtitle2">SENAI Morvan Figueiredo</div>
              <div class="text-caption">Setembro 2024</div>
              <div class="text-caption q-mt-sm">Competências: Microsoft Excel</div>
            </q-card-section>
            <q-card-actions>
              <q-btn
                flat
                :label="$t('see_certificate')"
                @click="
                  showCertificate({
                    imgPath: '/portfolio/assets/excel_basico.jfif',
                    linkVerificacao:
                      'https://www.sp.senai.br/consulta-certificado?qrcode=00032846/4046422',
                  })
                "
              />
            </q-card-actions>
          </q-card>

          <!-- Cisco - IT Essentials -->
          <q-card flat bordered class="certificate-card">
            <q-img src="/portfolio/assets/it_essentials.jfif" height="200px" class="certificate-image" />
            <q-card-section>
              <div class="text-h6">IT Essentials</div>
              <div class="text-subtitle2">Cisco</div>
              <div class="text-caption">Setembro 2024</div>
              <div class="text-caption q-mt-sm">
                Competências: Hardware, Software, Redes básicas, Manutenção de computadores
              </div>
            </q-card-section>
            <q-card-actions>
              <q-btn
                flat
                :label="$t('see_certificate')"
                @click="
                  showCertificate({
                    imgPath: '/portfolio/assets/it_essentials.jfif',
                    linkVerificacao:
                      'https://www.credly.com/badges/25e10c9a-9ed2-4c4b-86bc-3b2b0ddbb5cb/linked_in_profile',
                  })
                "
              />
            </q-card-actions>
          </q-card>

          <!-- Cisco - IoT -->
          <q-card flat bordered class="certificate-card">
            <q-img
              src="/portfolio/assets/introduction_to_iot.png"
              height="200px"
              class="certificate-image"
            />
            <q-card-section>
              <div class="text-h6">Introduction to IoT</div>
              <div class="text-subtitle2">Cisco</div>
              <div class="text-caption">Setembro 2024</div>
              <div class="text-caption q-mt-sm">
                Competências: Internet das Coisas, Redes de sensores, Conectividade
              </div>
            </q-card-section>
            <q-card-actions>
              <q-btn
                flat
                :label="$t('see_certificate')"
                @click="
                  showCertificate({
                    imgPath: '/portfolio/assets/introduction_to_iot.png',
                    linkVerificacao: '',
                  })
                "
              />
            </q-card-actions>
          </q-card>

          <!-- SENAI - Segurança do Trabalho -->
          <q-card flat bordered class="certificate-card">
            <q-img
              src="/portfolio/assets/seguranca_do_trabalho.jfif"
              height="200px"
              class="certificate-image"
            />
            <q-card-section>
              <div class="text-h6">Segurança do Trabalho</div>
              <div class="text-subtitle2">SENAI Morvan Figueiredo</div>
              <div class="text-caption">Setembro 2024</div>
              <div class="text-caption q-mt-sm">
                Competências: Normas de segurança, Prevenção de acidentes, Gestão de riscos
              </div>
            </q-card-section>
            <q-card-actions>
              <q-btn
                flat
                :label="$t('see_certificate')"
                @click="
                  showCertificate({
                    imgPath: '/portfolio/assets/seguranca_do_trabalho.jfif',
                    linkVerificacao:
                      'https://www.sp.senai.br/consulta-certificado?qrcode=00032847/4046422',
                  })
                "
              />
            </q-card-actions>
          </q-card>

          <!-- SENAI - Ética na IA -->
          <q-card flat bordered class="certificate-card">
            <q-img src="/portfolio/assets/etica_na_ia.jfif" height="200px" class="certificate-image" />
            <q-card-section>
              <div class="text-h6">Ética na IA</div>
              <div class="text-subtitle2">SENAI Morvan Figueiredo</div>
              <div class="text-caption">Setembro 2024</div>
              <div class="text-caption q-mt-sm">
                Competências: Inteligência Artificial, Ética digital, Responsabilidade tecnológica
              </div>
            </q-card-section>
            <q-card-actions>
              <q-btn
                flat
                :label="$t('see_certificate')"
                @click="
                  showCertificate({
                    imgPath: '/portfolio/assets/etica_na_ia.jfif',
                    linkVerificacao:
                      'https://www.sp.senai.br/consulta-certificado?qrcode=00032850/4046422',
                  })
                "
              />
            </q-card-actions>
          </q-card>
        </div>
      </div>

      <q-dialog v-model="showModal">
        <q-card style="width: 800px; max-width: 90vw">
          <q-card-section class="row items-center q-pb-none">
            <q-space />
            <q-btn icon="close" flat round dense v-close-popup />
          </q-card-section>

          <q-card-section>
            <q-img
              :src="selectedCertificate.imgPath"
              class="full-width"
              style="max-height: 70vh; object-fit: contain"
            />
          </q-card-section>

          <q-card-actions align="right">
            <q-btn
              :label="$t('verify')"
              :href="selectedCertificate.linkVerificacao"
              target="_blank"
            />
          </q-card-actions>
        </q-card>
      </q-dialog>

      <q-separator id="separador" />

      <div class="projetos margin q-py-xl" id="projetos">
        <span class="text-h4 q-mb-lg">{{ $t('projetos') }}</span>
        <div class="projects-grid q-mt-md">
          <q-card flat bordered class="project-card">
            <q-img src="caminho-para-imagem" />
            <q-card-section>
              <div class="text-h6">Em Construção</div>
              <p class="text-body2">Em Construção</p>
            </q-card-section>
            <q-card-actions align="right">
              <q-btn flat label="Demo" />
              <q-btn flat label="Código" />
            </q-card-actions>
          </q-card>
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
import { ref } from 'vue'

const showModal = ref(false)
const selectedCertificate = ref('')

const showCertificate = (certificate) => {
  selectedCertificate.value = certificate
  showModal.value = true
}

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
* {
  object-fit: contain !important;
}

.certificate-image {
  transition: transform 0.3s ease;
}

.certificate-image:hover {
  transform: scale(1.03);
}

.q-dialog__inner > .q-card {
  border-radius: 12px;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
}

.text-caption {
  color: rgba(255, 255, 255, 0.7);
}

.certificate-card {
  min-height: 200px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.q-card-section {
  flex-grow: 1;
}
</style>

<style scoped>
.certificates-grid,
.projects-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
}

.certificate-card,
.project-card {
  background: rgba(255, 255, 255, 0.05);
  transition: all 0.3s ease;
}

.certificate-card:hover,
.project-card:hover {
  transform: translateY(-5px);
  background: rgba(255, 255, 255, 0.1);
}

@media (max-width: 768px) {
  .certificates-grid,
  .projects-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 480px) {
  .certificates-grid,
  .projects-grid {
    grid-template-columns: 1fr;
  }
}
</style>

<style>
/* Estilo para navegadores WebKit (Chrome, Safari, Edge) */
::-webkit-scrollbar {
  width: 10px;
}

::-webkit-scrollbar-track {
  background: #00000000;
}

::-webkit-scrollbar-thumb {
  background: #00bd00;
  border-radius: 5px;
}

::-webkit-scrollbar-thumb:hover {
  background: #00bd00;
}

/* Estilo para Firefox */
* {
  scrollbar-width: thin;
  scrollbar-color: #00bd00 #00000000;
}

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
