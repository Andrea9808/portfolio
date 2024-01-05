<script>
export default {
    name: "MainApp",

    data() {
        return {
            mostraModale: false,
            mostraModaleAboutMe: false,
        };
    },

    methods: {

        // MODALE CONTACT
        apriModale() {
            console.log("Apri Modale");
            this.mostraModale = true;
        },
        chiudiModale() {
            console.log("Chiudi Modale");
            this.mostraModale = false;
        },

        // MODALE ABOUT ME
        apriModaleAboutMe() {
            console.log("Apri Modale");
            this.mostraModaleAboutMe = true;
        },
        chiudiModaleAboutMe() {
            console.log("Chiudi Modale");
            this.mostraModaleAboutMe = false;
        }
    }
};
</script>

<template>
    <div class="container">
        <div class="row">
            <div class="col-6">
                <div>
                    <h1>Hi, I'm Andrea Manigrasso</h1>
                    <h4>Full-Stack Developer</h4>

                    <p>Studente di web development con una passione contagiosa per il codice e un approccio solare alla
                        risoluzione delle sfide. Creativo di natura, cerco ispirazione in ogni linea di codice per creare
                        soluzioni uniche e innovative. <span class="portfolio">Esplora il mio mondo di progetti cliccando
                            sulla sezione Portfolio.</span>
                    </p>

                    <div>
                        <button @click="apriModaleAboutMe" class="gap-button">About me</button>
                        <button @click="apriModale">Contact</button>
                    </div>
                </div>
            </div>

            <div class="col-6">
                <!-- FOTO PROFESSIONALE -->
            </div>
        </div>

         <!-- MODALE CONTACT -->
    <transition name="modal" appear>
      <div v-show="mostraModale" class="modal">
        <div class="modal-content">
          <span class="chiudi" @click="chiudiModale">&times;</span>

          <div class="v-space">
            <img class="italianflag" src="/italianFlag.png" alt="italianFlag" />
            <p>Recapito telefonico: +39 ...............</p><br />
          </div>

          <p>Indirizzo mail: ........@gmail.com</p>
        </div>
      </div>
    </transition>

    <!-- MODALE ABOUT ME -->
    <transition name="modal" appear>
      <div v-show="mostraModaleAboutMe" class="modal">
        <div class="modal-content">
          <span class="chiudi" @click="chiudiModaleAboutMe">&times;</span>
          <div class="row">
            <div class="col-6">
              <div>
                <h5>Chi sono:</h5>
                <p>
                  Ciao! Sono Andrea Manigrasso, uno studente appassionato di
                  web development. Attualmente sto studiando una varietà di
                  tecnologie per diventare un Full-Stack Developer.
                </p>
              </div>
            </div>

            <div class="col-6">
              <div>
                <h5>Linguaggi di Programmazione Studiati:</h5>
                <ul>
                  <li>HTML</li>
                  <li>CSS</li>
                  <li>Libreria: Bootstrap</li>
                  <li>Javascript</li>
                  <li>Framework VUE. JS</li>
                  <li>PHP</li>
                  <li>LARAVEL</li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </transition>
    </div>
</template>

<style lang="scss" scoped>
.portfolio {
  color: white;
}

.gap-button {
  margin-right: 10px;
}

button {
  border-radius: 5px;
  padding: 5px;
  background-color: rgb(130, 9, 136);
  color: white;
  box-shadow: 0px 0px 10px -3px;
  transition: background-color 0.3s ease-in-out;
}

button:hover {
  background-color: rgb(100, 9, 106);
}

.modal-enter-active,
.modal-leave-active {
  transition: opacity 0.3s;
}

.modal-enter-to,
.modal-leave-active {
  opacity: 1;
}

.modal-enter,
.modal-leave-to {
  opacity: 0;
}

.modal {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: rgba(0, 0, 0, 0.4);
}

.modal-content {
  background-color: #fefefe;
  padding: 20px;
  border: 1px solid #888;
  width: 50%;
  max-height: 80%;
}

.chiudi {
  display: flex;
  justify-content: end;
  color: blueviolet;
  font-size: 28px;
  font-weight: bold;
  cursor: pointer;
}

.v-space {
  display: flex;
}

.italianflag {
  width: 30px;
  height: 20px;
  margin-right: 10px;
}
</style>