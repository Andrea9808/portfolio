<script>
  export default{
    name:"MainApp",
  }
</script>

<template>
    <div class="container">
        <div class="row">
            <div class="col-6">
                <div>
                    <h1>Hi, I'm Andrea Manigrasso</h1>
                    <h4>Full-Stack Developer</h4>

                    <p>Studente di web development con una passione contagiosa per il codice e un approccio solare alla risoluzione delle sfide. Creativo di natura, cerco ispirazione in ogni linea di codice per creare soluzioni uniche e innovative. <span class="portfolio">Esplora il mio mondo di progetti cliccando sulla sezione Portfolio.</span></p>

                    <div>
                        <button class="gap-button">About me</button>
                        <button>Contact</button>
                    </div>
                </div>
            </div>

            <div class="col-6">
                <!-- FOTO PROFESSIONALE -->
            </div>
        </div>
    </div>
</template>

<style lang="scss">

    .portfolio{
        color: white;
    }
    
    .gap-button{
        margin-right: 10px;
    }

    button{
        border-radius: 5px;
        padding: 5px;
        background-color: rgb(130, 9, 136);
        color: white;
        box-shadow: 0px 0px 10px -3px;
    }
</style>
