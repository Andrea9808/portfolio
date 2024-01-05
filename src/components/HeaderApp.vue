<script>
export default {
    name: "HeaderApp",

    data() {
        return {
            isMenuOpen: false,
            activeIndex: 0,
            links: [
                {
                    text: "Home",
                    url: "#",
                    current: true
                },
                {
                    text: "About",
                    url: "#",
                    current: false
                },
                {
                    text: "Services",
                    url: "#",
                    current: false
                },
                {
                    text: "Portfolio",
                    url: "https://github.com/Andrea9808",
                    current: false
                },
                {
                    text: "Contacts",
                    url: "#",
                    current: false
                },
            ]
        }
    },
    methods: {
        toggleMenu() {
            this.isMenuOpen = !this.isMenuOpen;
        },
        setActiveIndex(index) {
            this.activeIndex = index;
        }
    },

}


</script>

<template>
    <header>
        <div class="container py-4">
            <div class="row align-items-center">
                <div class="col-6">
                    <div>
                        <h5>Andrea.</h5>
                    </div>
                </div>
                <div class="col-6 col-sm-6 col-md-6 col-lg-6 d-flex align-items-center justify-content-end">
                    <div v-if="!isMenuOpen" class="hamburger-icon" @click="toggleMenu">
                        <i class="fa-solid fa-bars d-lg-none d-md-block"></i>
                    </div>
                    <div v-if="isMenuOpen" class="close-icon" @click="toggleMenu">
                        <i class="fa-solid fa-times d-lg-none"></i>
                    </div>

                    <!-- MENU HAMB -->
                    <ul class="hamb_menu d-lg-none" v-show="isMenuOpen">
                        <li v-for="link in links" :key="link" :class="{ 'active': link.current }">
                            <a :href="link.url" @click="toggleMenu">
                                {{ link.text }}
                            </a>
                        </li>
                    </ul>

                    <!-- MENU LG -->
                    <ul class="d-none d-lg-block">
                        <li v-for="(link, index) in links" :key="index" :class="{ 'active': index === activeIndex }">
                            <a :href="link.url" @click="setActiveIndex(index)">
                                {{ link.text }}
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </header>
</template>
  

<style lang="scss" scoped>
ul {
    list-style-type: none;

    li {
        display: inline;
        margin-left: 50px;

        a {
            text-decoration: none;
            color: black;
            transition: background-color 0.3s, color 0.3s, padding 0.3s, border-radius 0.3s;


            &:hover {
                background-color: white;
                color: blueviolet;
                padding: 12px 12px;
                border-radius: 5px;
            }
        }

    }

    li.active a {
        color: rgb(88, 3, 167);
    }
}

.hamb_menu {

    li {
        display: block;
        margin-top: 10px;

        a {
            text-decoration: none;
            color: black;
            transition: background-color 0.3s, color 0.3s, padding 0.3s, border-radius 0.3s;

            &:hover {
                background-color: white;
                color: blueviolet;
                padding: 12px 12px;
                border-radius: 5px;
            }
        }
    }
}


.close-icon {
    margin-right: 20px;
    cursor: pointer;
    position: absolute;
    top: 10px;
    right: 10px;
}

// Quando il menu è aperto, mostra la "x"
.hamb_menu {
    .close-icon {
        display: block;
    }
}

.fa-bars {
    cursor: pointer;
}
</style>
