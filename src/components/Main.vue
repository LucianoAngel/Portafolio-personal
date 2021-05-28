<template>
  <div id="app">
    <header class="degradado mh-50">
      <b-container fluid>
        <b-row>
          <b-col>
            <div class="display-2 md-5  mt-3 white-text text-center">
              <h3
                class="display-3 font-weight-bold white-text mb-0 pt-md-5 pt-5"
              >
                ¿Necesítas Un Desarrollador?
              </h3>
              <h2 class="mt-3">
                Desarrollo "Lógico y Creativo" antes que nada
              </h2>
            </div>
            <p class="mt-5 white-text text-center font-weight-bold">
              Estuiante de UVM, Freelancer, Autodidacta. Con Experiencia en los
              ámbitos:
            </p>
            <b-row class="mt-3 mb-3">
              <b-col>
                <b-avatar
                  icon="terminal"
                  size="3rem"
                  class="mt-3 mb-3"
                  variant="dark"
                ></b-avatar>
                <b-badge variant="dark">Front-End</b-badge>
              </b-col>
              <b-col>
                <b-avatar
                  icon="hdd-stack-fill"
                  size="3rem"
                  class="mt-3 mb-3"
                  variant="dark"
                ></b-avatar>
                <b-badge variant="dark">Back-End</b-badge>
              </b-col>
              <b-col>
                <b-avatar
                  icon="journal-check"
                  size="3rem"
                  class="mt-3 mb-3"
                  variant="dark"
                ></b-avatar>
                <b-badge variant="dark">Unit-Testing</b-badge>
              </b-col>
            </b-row>
            <b-button id="pretty-button" class="text-dark"
              >Conoce más, sigue bajando</b-button
            >
          </b-col>
          <b-col>
            <b-img
              thumpbail
              fluid
              right
              :src="require('../assets/retratopng.png')"
            ></b-img>
          </b-col>
        </b-row>
      </b-container>
    </header>
    <b-button block variant="outline-info" class="font-weight-bold"
      >Proyectos Realizados <b-avatar icon="terminal" variant="info"></b-avatar
    ></b-button>
    <main>
      <div class="container">
        <b-card>
          <b-card-group>
            <div
              v-for="(proyecto, i) in proyectos"
              :key="proyecto.nombre + `${i}`"
            >
              <b-card
                :title="proyecto.nombre"
                :sub-title="proyecto.tecnologias"
                class="mb-2 ml-3 mr-3 mt-3"
                tag="article"
                :img-src="proyecto.link"
                img-top
                style="max-width: 20rem;"
                bg-variant="dark"
                text-variant="white"
              >
                <b-card-text>
                  {{ proyecto.descripcion }}
                </b-card-text>
                <b-button
                  class="mr-2"
                  v-if="proyecto.front"
                  :href="proyecto.front"
                  variant="danger"
                  target="_blank"
                >
                  Repo front
                </b-button>
                <b-button
                  class="ml-2"
                  v-if="proyecto.front && proyecto.back"
                  :href="proyecto.back"
                  variant="info"
                  target="_blank"
                >
                  Repo back
                </b-button>
                <b-button
                  v-if="!proyecto.front && !proyecto.back"
                  :href="proyecto.redirect"
                  variant="info"
                  target="_blank"
                >
                  Ir al Repositorio
                </b-button>
              </b-card>
            </div>
          </b-card-group>
        </b-card>
      </div>
      <b-button block variant="outline-info" class="font-weight-bold"
        >Experiencia Obtenida <b-avatar icon="award" variant="info"></b-avatar
      ></b-button>
      <!-- Explicación más detallada sobre la experiencia obtenida -->
      <div>
        <b-card>
          <b-container fluid="sm">
            <b-row class="mt-3 mb-3">
              <b-col col lg="4"></b-col>
              <b-col col lg="4" class="text-center">
                <b-img
                  thumpbail
                  fluid
                  right
                  :src="require('../assets/html.png')"
                  class="mt-5"
                ></b-img>
              </b-col>
              <b-col col lg="2">
                <h4 class="font-weight-bold">2019</h4>
                En el 2019 empezó mi redescubrimiento de la programación, luego
                de aprender un montón de conceptos básicos, llego la hora de
                ponerlos en práctica, el primer lenguaje de programación que
                aprendí fue JavaScript, con ello necesitaba un interprete, y
                para hacerlo más complejo me ví en la obligación de aprender
                html y css para emprender un proyecto, mi primer paso fue la
                creación de "JARVIS"
              </b-col>
              <b-col col lg="2">
                <h4 class="font-weight-bold">2020</h4>
                Con lo complejo que es el mundo del desarrollo web, al conocer
                las bases de la programación, estuve preparado para más, y con
                ello adquirí experiencia en los proyectos de "first in first
                out", además del proyecto de reproductor de música, y la
                creación del clon web de NodeJS
              </b-col>
            </b-row>
            <b-row>
              <b-col col lg="4">
                <h4 class="font-weight-bold">2020</h4>
                JEST: JavaScript Test; si tuviera que describir lo que fue
                aprender el Test Unitario en una sola palabra sería: "WOW",
                simplemente increible, al conocer el mundo de los test, se abre
                tu comprensión de la programación en cantidades abismales, con
                ella trabajé de freelance realizando más de 200 test de
                aplicaciones Front-End
              </b-col>
              <b-col col lg="4">
                <b-avatar
                  :src="require('../assets/jest.png')"
                  variant="light"
                  size="8rem"
                  rounded=""
                  class="mt-5"
                ></b-avatar>
              </b-col>
              <b-col col lg="4"></b-col>
            </b-row>
            <b-row>
              <b-col></b-col>
              <b-col
                ><b-avatar
                  :src="require('../assets/logo.png')"
                  variant="light"
                  size="8rem"
                  rounded=""
                  class="mt-5 t-5"
                ></b-avatar
              ></b-col>
              <b-col>
                <h4 class="font-weight-bold">2020</h4>
                Con la Popularidad de los Frameworks en el desarrollo web, mi
                aprendizaje de VUE fue leyendolo, para la realización de Test
                Unitarios en Componentes de VUE, me ví en la necesidad de
                aprenderlo, con ello junto a la maravillosa documentación que
                tiene el mismo, realicé mi proyecto personal del manejo contable
                y administrativo de un comercio, y a finales de año la
                implementación de VUE en el reproductor de música dinamico
                "DAYLUC" y esta mísma página web, mi portafolio personal.
              </b-col>
            </b-row>
            <b-row>
              <b-col>
                <h4 class="font-weight-bold">2020</h4>
                Mi experiencia en el back-end empezó con la necesidad de
                administrar mis proyectos personales sin depender de datos
                estáticos, luego de aprender a realizar APIs, vendí mi trabajo
                realizando un proyecto de FREELANCE manejando el back-end de una
                página web, con los conocimientos obtenidos los transladé a mis
                proyectos personales como lo són el reproductor "DAYLUC" y mi
                proyecto de administracion de un comercio.
              </b-col>
              <b-col>
                <b-avatar-group size="8rem" class="mt-5">
                  <b-avatar
                    :src="require('../assets/nodejs.png')"
                    variant="light"
                  ></b-avatar>
                  <b-avatar
                    :src="require('../assets/mongo.png')"
                    variant="light"
                  ></b-avatar>
                  <b-avatar
                    :src="require('../assets/express.png')"
                    variant="light"
                  ></b-avatar>
                </b-avatar-group>
              </b-col>
              <b-col></b-col>
            </b-row>
          </b-container>
        </b-card>
      </div>
      <b-button block variant="outline-info" class="font-weight-bold"
        >Información de Contacto
        <b-avatar icon="telephone" variant="info"></b-avatar
      ></b-button>
    </main>
    <footer>
      <b-conntainer-fluid>
        <b-card align="center" bg-variant="dark" text-variant="light">
          <b-card-text>
            <b-row>
              <b-col>
                <h4 class="font-weight-bold">Contacto</h4>
                <p>Telegram: 04247750438</p>
                <p>Mail: ragadurana@uvm.edu.ve</p>
                <p>GitHub: github.com/lucianoangel</p>
              </b-col>
              <b-col>
                <h4 class="font-weight-bold">Herramientas de trabajo</h4>
                <p>Bitbucket</p>
                <p>Trello</p>
                <p>Visual Studio Code</p>
              </b-col>
              <b-col class="mt-5">
                <p>"Soñar es tán facil, es gratis"</p>
              </b-col>
            </b-row>
            <b-row class="mt-3">
              <b-col>
                <b-badge pill class="text-center" variant="light">
                  <p class="font-weight-bold mt-3 ml-2 mr-2">
                    Diseño: Angel Raga. Derechos Reservados
                  </p>
                </b-badge>
                <p class="font-weight-bold mt-3">
                  Version: 1.10
                </p>
              </b-col>
            </b-row>
          </b-card-text>
        </b-card>
      </b-conntainer-fluid>
    </footer>
  </div>
</template>

<script>
// Agregar carrusel de fotos a las cartas
// Agregar substring y botón de ver más a las cartas
// Actualizar info de la experiencia obtenida
// Agregar panel de hobbies
// Agregar distintas resoluciones a las fotos para optimizar la web
export default {
  name: "main",
  data() {
    return {
      proyectos: [
        {
          nombre: "DANHYLUC",
          descripcion:
            "Esta aplicación les permite a los usuarios almacenar información referente a su negocio, clientes, servidores del sistema, categorías de los servicios, servicios disponibles con sus montos además de la muestra de las transacciones realizadas con sus respectivas especificaciones, siendo adaptable a cualquier negocio que preste un servicio",
          tecnologias: "VUE, BOOTSTRAP, EXPRESS, MONGO",
          link: require("../assets/proyectos/danhyluc.png"),
          front: "https://github.com/LucianoAngel/danhyluc",
          back: "https://github.com/LucianoAngel/danhyluc-back",
        },
        {
          nombre: "Administrador de una ciudad",
          descripcion:
            'CRUD encargado de administrar las edificaciones de una ciudad, en ella puedes agregar a tu ciudad todo tipo de edificaciones con sus especificaciones correspondientes, además cuenta con un diseño reesponsive y una base de datos NOSQL',
          tecnologias: "VUE, BOOTSTRAP, EXPRESS, MONGO",
          link: require("../assets/proyectos/gestionCiudad.jpg"),
          front: "https://github.com/LucianoAngel/City-management",
          back: "https://github.com/LucianoAngel/City-management-back",
        },
        {
          nombre: "E-Shop",
          descripcion:
            'Proyecto personal, cuenta con la funcionalidad de administrar: compras, ventas, ingresos, personal y clientes de un comercio, es una "SPA", cuenta con manejo de sesiones y una landing page',
          tecnologias: "VUE, BOOTSTRAP, EXPRESS, MONGO",
          link: require("../assets/proyectos/shop1.jpg"),
          front: "https://github.com/LucianoAngel/e-shop",
          back: "https://github.com/LucianoAngel/e-shop",
        },
        {
          nombre: "Portafolio Personal",
          descripcion:
            'Es la página web en la que estás navegando actualmente, es una "SPA" con datos estáticos, es completamente "responsive", muestra un portafolio personal, agradable a la vista, con redireccionamientos a repósitorios de GitHub',
          tecnologias: "VUE, BOOTSTRAP",
          link: require("../assets/proyectos/portafolio.png"),
          redirect: "https://github.com/LucianoAngel/Portafolio-personal",
        },
        {
          nombre: "DAYLUC",
          descripcion:
            'Es una "NUBE" de canciones con la funcionalidad de ser un reproductor de música (dinámico), cuenta con un manejo de usuarios, sesiones,  registro, inicio y cierre de sesión, cada usuario puede subir sus canciones y escuchar las de los demás, tambien puede editar los nombres de la cancion y eliminarlas solo si el usuario las ha subido',
          tecnologias: "VUE, BOOTSTRAP, MONGO, NODE, EXPRESS",
          link: require("../assets/proyectos/dayluc.png"),
          front: "https://github.com/LucianoAngel/dayluc/tree/main/front-end",
          back: "https://github.com/LucianoAngel/dayluc/tree/main/back-end",
        },
        {
          nombre: "Reproductor de Música",
          descripcion:
            "Es un proyecto que resuelve la necesidad de escuchar musica, la web cuenta con la administracion de: las listas de reproduccion, mostrar tu historial de canciones escuchadas, y ser agradable a la vista",
          tecnologias: "HTML, CSS, JQUERY",
          link: require("../assets/proyectos/musicPlayer.png"),
          redirect: "https://github.com/LucianoAngel/musicPlayer",
        },
        {
          nombre: "JARVIS",
          descripcion:
            "Proyecto que simula la inteligencia de JARVIS o VIERNES de la pelicula IRON-MAN, con el fin de controlar nuestra habitación, haciendo uso de sensores y accionadores en la pagina web y en la habitación con la lógica de ser aplicado en: (internet of things)",
          tecnologias: "HTML, CSS, JQUERY",
          link: require("../assets/proyectos/jarvis.png"),
          redirect: "https://github.com/LucianoAngel/jarvis",
        },
        {
          nombre: "Clon NodeJS",
          descripcion:
            "Proyecto basado en la clonación de una pagina web (página web de NodeJs)",
          tecnologias: "HTML, CSS",
          link: require("../assets/proyectos/node.png"),
          redirect: "https://github.com/LucianoAngel/node-js-clon",
        },
      ],
    };
  },
  methods: {},
  mounted: function() {},
};
</script>

<style>
.degradado {
  background-image: linear-gradient(
    to left,
    #00bfff,
    #01bfff,
    #ff4041,
    #ff4040,
    #ff4039
  );
  /* background-image: linear-gradient(to right top, #051937, #004d7a, #008793, #00bf72, #a8eb12); */
}
#pretty-button {
  background: none;
  font-size: 20px;
  font-weight: bold;
  padding: 20px 40px;
  display: inline-block;
  border: 5px solid #001f3f;
  transition: 0.3s all ease;
}
#pretty-button:hover {
  border: 5px solid #01bfff;
  color: #01bfff;
}
</style>
