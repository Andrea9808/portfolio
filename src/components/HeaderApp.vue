<script>
export default {
    name: "HeaderApp",

    data() {
        return {
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
                    url: "https://github.com/Andrea9808",
                    current: false
                },
            ]
        }
    }
}


</script>

<template>
    <header>
        <div class="container py-4">
            <div class="row">
                <div class="col-6">
                    <div>
                        <h5>Andrea.</h5>
                    </div>
                </div>
                <div class="col-6">
                    <div>
                        <ul>
                            <li v-for="link in links" key="link">
                                <a :href="link.url">
                                    {{ link.text }}
                                </a>
                            </li>
                        </ul>
                    </div>
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
        padding-left: 50px;

        a {
            text-decoration: none;
            color: black;
        }
    }
}
</style>
