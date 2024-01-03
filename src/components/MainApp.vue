<script>
export default {
    name: "MainApp",

    data() {
        return {
            mostraModale: false,
        };
    },

    methods: {
        apriModale() {
            console.log("Apri Modale");
            this.mostraModale = true;
        },
        chiudiModale() {
            console.log("Chiudi Modale");
            this.mostraModale = false;
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
                            sulla sezione Portfolio.</span></p>

                    <div>
                        <button class="gap-button">About me</button>
                        <button @click="apriModale">Contact</button>
                    </div>
                </div>
            </div>

            <div class="col-6">
                <!-- FOTO PROFESSIONALE -->
            </div>
        </div>

        <div v-if="mostraModale" class="modal">
            <div class="modal-content">
                <span class="chiudi" @click="chiudiModale">&times;</span>

                <div class="cellular">
                    <img class="italianflag" src="/italianFlag.png" alt="italianFlag">
                    <p>Recapito telefonico: +39 ...............</p><br>
                </div>
                
                <p>Indirizzo mail: ........@gmail.com</p>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
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
    float: right;
    font-size: 28px;
    font-weight: bold;
    cursor: pointer;
}

.cellular{
    display: flex;
}

.italianflag{
   width: 30px;
   height: 20px;
   margin-right: 10px;
}
</style>
