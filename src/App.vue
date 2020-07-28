<template>
  <div id="app" class="col-1">
    <link href="https://use.fontawesome.com/releases/v5.0.13/css/all.css" rel="stylesheet" />
    <div class="col-30">
      <div class="col-1">
        <div class="col-80 center">
          <img src="./assets/0.jpeg" class="img-profile" />
        </div>
      </div>
      <div class="col-1">
        <div class="col-80 center">
          <FullName FirstName="Cristian" LastName="Carvajal" />
        </div>
        <div class="col-80 center">
          <Contact v-for="contact in contacts" v-bind:key="contact.id" v-bind:contact="contact" />
        </div>
      </div>
    </div>
    <div class="col-70">
      <div class="box">
        <Paragraph
          Paragraph="Cuento con 9 años de experiencia en desarrollo .NET (C#, VB, Asp.Net, Asp.Net MVC, Web Api, WPF, WCF, Net Core).
                                    Desarrollo frontend en HTML, CSS, JavaScript, Vue.js, AngularJS, Angular, Bootstrap, Stylus, Gulp y MeteorJs, SASS.
                                    Bases de datos SQL Server, Oracle, MySQL, MongoDB, Firebase, Elasticsearch.
                                    Manejo de Reporting Services, Report Builder y Sybase InfoMaker.
                                    Lenguajes de programación C#, Visual Basic.Net, Javascript, experiencia de 1 año con Python y Node.js.
                                    Conocimientos de metodologías ágiles de desarrollo (SCRUM, XP, Kanban). Conocimientos de patrones de diseño y UML. Integración Continua CI, entrega continua CD mediante AzureDevops.
                                    Conocimiento de Git, GitHub, TFS/AzureDevops y herramientas como Sonar Qube, Resharper, JMeter, Kibana y Logstah.
                                    Conocimientos en Unit testing, integration testing, TDD, automatización con Selenium. "
        />
      </div>
      <div>
        <Title title="Certificaciones" />
        <Certifications></Certifications>
      </div>
      <div>
        <Title title="Experiencia" />
        <WorkExperience></WorkExperience>
      </div>
    </div>
  </div>
</template>

<script>
import Paragraph from "./components/Paragraph.vue";
import FullName from "./components/FullName.vue";
import WorkExperience from "./components/WorkExperience.vue";
import Contact from "./components/Contact.vue";
import Education from "./components/Education.vue";
import Certifications from "./components/Certifications.vue";
import Title from "./components/Title.vue";

export default {
  name: "app",
  components: {
    Title,
    Paragraph,
    FullName,
    WorkExperience,
    Contact,
    Education,
    Certifications,
  },
  data() {
    return {
      contacts: [
        {
          id: 1,
          icon: "fas fa-envelope",
          value: "cristian.carvajal@live.com",
          url: "mailto:cristian.carvajal@live.com",
        },
        {
          id: 2,
          icon: "fab fa-linkedin",
          value: "linkedin",
          url: "https://linkedin.com/in/cricarba/",
        },
        {
          id: 5,
          icon: "fab fa-twitter",
          value: "@cricarba",
          url: "https://twitter.com/cricarba",
        },
        {
          id: 4,
          icon: "fas fa-globe",
          value: "Hoja de vida",
          url: "https://cricarba.github.io/profile/",
        },
        {
          id: 7,
          icon: "fas fa-map-marker",
          value: "Bogotá, CO",
          url: "https://www.google.com/maps/place/Bogot%C3%A1/@4.6486259,-74.2478963,11z/data=!3m1!4b1!4m5!3m4!1s0x8e3f9bfd2da6cb29:0x239d635520a33914!8m2!3d4.7109886!4d-74.072092",
        },
      ],
    };
  },
};
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  margin-top: 3%;
  font-family: -apple-system, BlinkMacSystemFont, Segoe UI, Helvetica, Arial,
    sans-serif, Apple Color Emoji, Segoe UI Emoji;
  font-size: 18px;
  line-height: 1.5;
  color: #2c3e50;
}

.Title-Bold {
  letter-spacing: 0.1em;

  font-size: 0.8em;
  font-weight: 550;
}

.Title {
  letter-spacing: 0.1em;
  text-transform: uppercase;
  font-size: 0.8em;
}

.SubTitle {
  letter-spacing: 0.1em;
  font-size: 0.8em;
  line-height: 1.6;
}

.Footer {
  letter-spacing: 0.1em;
  font-size: 0.7em;
  line-height: 1.6;
}
.img-profile {
  border-radius: 50%;
  /*filter: grayscale(50%);*/
  width: 200px;
}

a {
  color: #2c3e50;
  text-decoration: none;
} /* Unvisited link  */
a:visited {
  color: #2c3e50;
} /* Visited link    */
a:hover {
  text-decoration: underline;
} /* Mouse over link */
a:active {
  color: #2c3e50;
} /* Selected link   */

hr {
  margin-right: 40px;
}
.center {
  text-align: center;
}
.col-1 {
  width: 100%;
  display: flex;
  -ms-flex-wrap: wrap;
  flex-wrap: wrap;
}
.col-2 {
  width: 50%;
}
.col-3 {
  width: 33%;
}
.col-4 {
  width: 25%;
}

.col-90 {
  width: 90%;
}
.col-80 {
  width: 80%;
}
.col-70 {
  width: 70%;
}
.col-60 {
  width: 60%;
}

.col-50 {
  width: 50%;
}
.col-40 {
  width: 40%;
}
.col-30 {
  width: 30%;
}
.col-20 {
  width: 20%;
}
.col-10 {
  width: 10%;
}
.box {
  border: 1px solid #e1e4e8;
  margin: 2px;
  border-radius: 6px;

  padding: 10px;
}
@media only screen and (max-width: 600px) {
  .img-profile {
    margin-left: 20%;
    width: 100px;
  }

  .Title {
    font-size: 0.6em;
    letter-spacing: 0.1em;
  }
  .SubTitle {
    font-size: 0.6em;
    letter-spacing: 0em;
  }
}

@media print {
  a {
    text-decoration: none;
  }
}
</style>
