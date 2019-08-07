<template>
  <v-container>
    <v-layout
      text-center
      wrap
    >


      <v-flex mb-4>
          <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
  <ol class="carousel-indicators">
    <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
  </ol>
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img src="https://ipc.milaulas.com/pluginfile.php/1895/course/overviewfiles/reporte-de-asistencia.png" class="d-block w-100" alt="...">
    </div>
    <div class="carousel-item">
      <img src="https://ipc.milaulas.com/pluginfile.php/1895/course/overviewfiles/reporte-de-asistencia.png" class="d-block w-100" alt="...">
    </div>
    <div class="carousel-item">
      <img src="https://ipc.milaulas.com/pluginfile.php/1895/course/overviewfiles/reporte-de-asistencia.png" class="d-block w-100" alt="...">
    </div>
  </div>
  <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>

        <h1 class="display-2 font-weight-bold mb-3">
          Bienvenido a la App de toma de asistencia
        </h1>
        <p class="subheading font-weight-regular">
          Para registrar a tus estudiantes
          Rellena el formulario debajo
          <br>
          <template v-if="loginType === 'username'">
  <label></label>
  <br>
  <input placeholder="Enter your username" key="username-input">
</template>
<template v-else>
  <label></label>
  <input placeholder="Enter your email address" key="email-input">
</template>
<br>
<v-flex xs12>
        <v-img
          :src="require('../assets/logo.svg')"
          class="my-3"
          contain
          height="200"
        ></v-img>
      </v-flex>
<v-btn>Login</v-btn>
        </p>
      </v-flex>

      <v-flex
        mb-5
        xs12
      >
        <h2 class="headline font-weight-bold mb-3">What's next?</h2>

        <v-layout justify-center>
<div class="accordion" id="accordionExample">
  <div class="card">
    <div class="card-header" id="headingOne">
      <h2 class="mb-0">
        <button class="btn btn-link" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
          Estudiantes
        </button>
      </h2>
    </div>

    <div id="collapseOne" class="collapse show" aria-labelledby="headingOne" data-parent="#accordionExample">
      <div class="card-body">
         aquí van todos los estudiantes
         <table class="table">
  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">nombre1</th>
      <th scope="col">nombre2</th>
      <th scope="col">apellido1</th>
      <th scope="col">apellido2</th>
      <th scope="col">idacudientes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>primer nombre</td>
      <td>segundo nombre</td>
      <td>primer apellido</td>
      <td>segundo apellido</td>
      <td> el id del acudiente con populacion para nombre</td>
    </tr>
  </tbody>
</table>
      </div>
    </div>
  </div>
  <div class="card">
    <div class="card-header" id="headingTwo">
      <h2 class="mb-0">
        <button class="btn btn-link collapsed" type="button" data-toggle="collapse" data-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
          asistencias
        </button>
      </h2>
    </div>
    <div id="collapseTwo" class="collapse" aria-labelledby="headingTwo" data-parent="#accordionExample">
      <div class="card-body">
          aqui va asistencias
                   <table class="table">
  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">asistencia</th>
      <th scope="col">inasistencias</th>
      <th scope="col">fecha</th>
      <th scope="col">id_estudiante</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>asistencias</td>
      <td>faltas a clase</td>
      <td>fecha</td>
      <td>id del estudiante populado</td>
    </tr>
  </tbody>
  </table>

    </div>
    </div>
  </div>
  <div class="card">
    <div class="card-header" id="headingThree">
      <h2 class="mb-0">
        <button class="btn btn-link collapsed" type="button" data-toggle="collapse" data-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
          listado
        </button>
      </h2>
    </div>
    <div id="collapseThree" class="collapse" aria-labelledby="headingThree" data-parent="#accordionExample">
      <div class="card-body">
       aqui va listado
       <table class="table">
  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">id_profesor</th>
      <th scope="col">id_materia</th>
      <th scope="col">fecha</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>id profesor</td>
      <td>id de materia</td>
      <td>fecha</td>
    </tr>
  </tbody>
  </table>
    </div>
  </div>
</div>
    <a href="#" class="btn btn-primary">Llama al acudiente</a>
  </div>
</div>
        </v-layout>
      </v-flex>

      <v-flex
        xs12
        mb-5
      >
        <h2 class="headline font-weight-bold mb-3">Registrar estudiantes</h2>

        <v-layout justify-center>
          <a
            <form>
  <div class="form-group">
    <label for="exampleInputEmail1">Email address</label>
    <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Enter email">
    <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
  </div>
  <div class="form-group">
    <label for="exampleInputPassword1">Password</label>
    <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Password">
  </div>
  <div class="form-group form-check">
    <input type="checkbox" class="form-check-input" id="exampleCheck1">
    <label class="form-check-label" for="exampleCheck1">Check me out</label>
  </div>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>
          </a>
        </v-layout>
      </v-flex>

      <v-flex
        xs12
        mb-5
      >
        <h2 class="headline font-weight-bold mb-3">ayuda</h2>

        <v-layout justify-center>
          <a
            v-for="(eco, i) in ecosystem"
            :key="i"
            :href="eco.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ eco.text }}
          </a>
        </v-layout>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    ayuda: [
      {
        text: 'vuetify-loader',
        href: 'https://github.com/deyes1219/trabajo/tree/master/bin/models',
      },
      {
        text: 'github',
        href: 'https://github.com/deyes1219/trabajo/tree/master/bin/models',
      },
      {
        text: 'awesome-vuetify',
        href: 'https://github.com/deyes1219/trabajo/tree/master/bin/models',
      },
    ],
    importantLinks: [
      {
        text: 'Documentation',
        href: 'https://github.com/deyes1219/trabajo/tree/master/bin/models',
      },
      {
        text: 'Chat',
        href: 'https://community.vuetifyjs.com',
      },
      {
        text: 'Made with Vuetify',
        href: 'https://madewithvuejs.com/vuetify',
      },
      {
        text: 'Twitter',
        href: 'https://twitter.com/vuetifyjs',
      },
      {
        text: 'Articles',
        href: 'https://medium.com/vuetify',
      },
    ],
    whatsNext: [
      {
        text: 'Explore components',
        href: 'https://vuetifyjs.com/components/api-explorer',
      },
      {
        text: 'Select a layout',
        href: 'https://vuetifyjs.com/layout/pre-defined',
      },
      {
        text: 'Frequently Asked Questions',
        href: 'https://vuetifyjs.com/getting-started/frequently-asked-questions',
      },
    ],
  }),
};
</script>
