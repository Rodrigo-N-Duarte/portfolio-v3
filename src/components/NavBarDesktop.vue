<template>
    <v-row justify="center" class="main-container dark-texture-background">
        <v-col cols="0" lg="12">
            <v-col cols="0" lg="2"></v-col>
            <v-col class="mobile-app-bar" cols="12" lg="6">
                <div>
                    <v-menu location="end">
                        <template v-slot:activator="{ props }">
                            <v-btn rounded style="background-color: inherit" v-bind="props" variant="plain">
                                <v-icon size="35">mdi-format-list-bulleted</v-icon>
                            </v-btn>
                        </template>
                        <v-list class="menu-mobile">
                            <v-list-item
                                v-for="item in items"
                                :key="item"
                            >
                                <v-list-item-title>
                                    <span><a :href="item.link" style="text-decoration: none; color: black">{{item.name}}</a></span>
                                </v-list-item-title>
                            </v-list-item>
                        </v-list>
                    </v-menu>
                </div>
            </v-col>
            <v-col align="center" class="pt-2 desktop-div" cols="12" lg="6">
                <div>
                    <router-link class="name-link mx-5" to="/">Rodrigo Duarte</router-link>
                    <router-link class="default-link mx-2 text-uppercase" v-for="item in items" :key="item" :to="item.link">{{item.name}}</router-link>
                </div>
            </v-col>
            <v-col cols="0" lg="4"></v-col>
        </v-col>
    </v-row>
</template>

<script>

export default {
    name: 'NavBarDesktop',
    data() {
        return {
            items: [
                {
                    name: 'Home',
                    link: '/'
                },
                {
                    name: 'About',
                    link: '/about'
                },
                {
                    name: 'Projects',
                    link: '/projects'
                },
                {
                    name: 'Skills',
                    link: '/skills'
                },
                {
                    name: 'Experience',
                    link: '/experience'
                },
                {
                    name: 'Contact',
                    link: '/contact'
                }
            ]
        }
    },
}
</script>

<style>
.default-link {
    font-family: 'Inter', sans-serif;
    font-size: 15px;
    color: aliceblue;
    text-decoration: none;
    position: relative;
    overflow: hidden;
    padding: 5px;
}

.default-link::after {
    content: '';
    display: block;
    position: absolute;
    bottom: 0;
    left: 0;
    width: 0;
    height: 1px;
    background-color: white;
}

.default-link:hover::after {
    animation: loading-bar 0.2s linear forwards;
}

@keyframes loading-bar {
    0% {
        width: 0;
    }
    100% {
        width: 100%;
    }
}


.name-link {
    color: aliceblue;
    text-decoration: none;
    font-family: 'Inter', sans-serif;
}

.desktop-div {
    display: block;
}



.mobile-app-bar {
    display: none;
}

@media (max-width: 1279px) {
    .desktop-div {
        display: none;
    }

    .mobile-app-bar {
        display: block;
    }
}

@media (min-width: 1280px) {
    .mobile-app-bar {
        display: none;
    }

    .desktop-div {
        display: block;
    }
}

.menu-mobile {
    background-color: aliceblue;
    padding: 20px 80px 20px 20px;
}
</style>
