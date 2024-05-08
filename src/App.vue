<template>
  <body>
    <div class="carnet">
      <aside>
        <div>
          <span>CEDULA DE INDENTIDAD</span>
          <img width="40" src="./assets/img/chile_bandera.png" alt="" />
        </div>
        <img src="./assets/img/foto_elon.jpg" alt="" />
        <p>RUN {{ run }}</p>
      </aside>
      <main>
        <header>
          <p>REPUBLICA DE CHILE</p>
          <span>SERVICIO DE REGISTRO CIVIL E IDENTIFICACIÓN</span>
        </header>
        <section>
          <article>
            <header>APELLIDOS</header>
            <span>{{ apellidos }}</span>
          </article>
          <article>
            <header>NOMBRES</header>
            <span>{{ nombres }}</span>
          </article>
          <div class="grid-2-colums">
            <article>
              <header>NACIONALIDAD</header>
              <span>{{ nacionalidad }}</span>
            </article>
            <article>
              <header>GENERO</header>
              <span>{{ genero }}</span>
            </article>
          </div>
          <div class="grid-2-colums">
            <article>
              <header>FECHA DE NACIMIENTO</header>
              <span> {{ fechaNacimiento }}</span>
            </article>
            <article>
              <header>NÙMERO DOCUMENTO</header>
              <span>{{ numeroDocumento }}</span>
            </article>
          </div>
          <div class="grid-2-colums">
            <article>
              <header>FECHA DE EMISIÒN</header>
              <span>{{ fechaEmision }}</span>
            </article>
            <article>
              <header>FECHA DE VENCIMIENTO</header>
              <span>{{ fechaVencimiento }}</span>
            </article>
          </div>
          <article>
            <header>FIRMA DEL TITULAR</header>
            <span>{{ firma }}</span>
          </article>
        </section>
      </main>
    </div>
  </body>
</template>

<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      run: "35.343.445-X",
      apellidos: "Musk",
      nombres: " Elon Reeve",
      nacionalidad: "Brasileña",
      genero: "Masculino",
      fechaNacimiento: "28 junio 1971",
      numeroDocumento: "222.222.222",
      fechaEmision: "30 abril 2024",
      fechaVencimiento: "28 junio 2034",
      firma: "(:ElonRM:)",
    };
  },
};
</script>

<style scoped>
body {
  display: flex;
  justify-content: center;
  align-items: center;

  font-size: 10px;
  font-family: sans-serif;
  background-image: url("assets/img/LogoDelRegistroCivil.png");
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;
  width: 100vw;
  height: 100vh;
}

.carnet {
  height: 40vh;
  width: 400px;
  background: #c8deed;
  border-radius: 20px;
  display: grid;
  grid-template-columns: 30% 1fr;
  padding: 15px;
  box-shadow: 0px 0px 10px 2px black;
  justify-content: center;
}

aside div {
  display: flex;
}

aside > img {
  margin-top: 15px;
  width: 100%;
}

aside p {
  text-align: center;
  font-size: 12px;
  font-weight: bold;
}

main {
  padding: 0px 14px;
}

main article {
  margin: 4px 0px;
}

main article header {
  font-weight: bold;
  color: #0235a4;
  font-size: 8px;
}

main header p {
  font-size: 20px;
  margin: 0;
  font-weight: bold;
  color: #0235a4;
}

main header span {
  font-size: 8px;
  color: #399be1;
}

main section {
  margin-top: 10px;
}

main section article span {
  font-size: 13px;
  font-weight: 600;
}

main section .grid-2-colums {
  display: grid;
  grid-template-columns: 50% 50%;
}
</style>