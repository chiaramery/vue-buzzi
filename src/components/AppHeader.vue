<script>
export default {
    name: "AppHeader",
    data() {
        return {
            nav: [
                {
                    label: "Home",
                    routeName: "home",
                },
                {
                    label: "Chi Siamo",
                    routeName: "chi-siamo",
                },
            ]
        }
    }
}
</script>

<template>
    <header>
        <div class="wrapper-header d-flex">
            <div class="logo">
                <img src="../img/30.JPG" alt="">
            </div>
            <div class="links">
                <ul class="link-list d-flex justify-content-center">
                    <li v-for="(item, index) in nav" :key="index">
                        <a href="">
                            <router-link :to="{ name: item.routeName }" class="nav-link" aria-current="page">{{ item.label
                            }}</router-link>
                        </a>
                    </li>
                </ul>
            </div>

        </div>
    </header>
</template>

<style lang="scss">
.wrapper-header {
    padding: 1em;
    background-color: rgb(11 113 184);
    align-items: center;

    .logo {
        width: 150px;
    }

    .links {

        .link-list {
            li {
                font-size: 1.3em;
                padding: .5em;
                color: white;
            }
        }
    }

    .right-header {
        display: flex;

        .languages {
            padding-right: 1em;
        }
    }
}
</style>