<template>
    <v-sheet elevation="10">
        <v-row class="main-container">
            <v-col>
                <v-row justify="center">
                    <v-col cols="0" lg="12">
                        <v-col cols="0" lg="2"></v-col>
                        <v-col class="pt-2 mobile-app-bar" cols="12" lg="6">
                            <div>
                                <v-menu location="end">
                                    <template v-slot:activator="{ props }">
                                        <v-btn rounded style="background-color: inherit" v-bind="props" variant="plain">
                                            <v-icon size="35">mdi-format-list-bulleted</v-icon>
                                        </v-btn>
                                    </template>
                                    <v-list class="menu-mobile">
                                        <v-list-item
                                                v-for="(item, index) in ['About', 'Projects', 'Contact']"
                                                :key="index"
                                        >
                                            <v-list-item-title>{{ item }}</v-list-item-title>
                                        </v-list-item>
                                    </v-list>
                                </v-menu>
                            </div>
                        </v-col>
                        <v-col align="center" class="pt-2 desktop-div" cols="12" lg="6">
                            <div>
                                <router-link class="name-link mx-5" to="/">Rodrigo Duarte</router-link>
                                <router-link class="default-link mx-5 text-uppercase" to="/">About</router-link>
                                <router-link class="default-link mx-5 text-uppercase" to="/">Projects</router-link>
                                <router-link class="default-link mx-5 text-uppercase" to="/">Contact</router-link>
                            </div>
                        </v-col>
                        <v-col cols="0" lg="4"></v-col>
                    </v-col>
                </v-row>
                <v-row class="container-hello" justify="center">
                    <v-col align="center">
                        <div>
                            <v-avatar size="200">
                                <v-img cover
                                       height="100%"
                                       src="https://us-tuna-sounds-images.voicemod.net/9f26bf21-2741-4615-b814-bd29765465f0-1671151360126.jpg"></v-img>
                            </v-avatar>
                            <div>
                                <div class="mb-5">
                                    <h1 class="title-name">Hi, I'm Rodrigo</h1>
                                    <h3 class="font-weight-light">I'm a developer, who loves working on frontend and
                                        backend too but, perhaps, hate both of then.
                                        <br>Just kidding :)</h3>
                                </div>
                                <v-row>
                                    <v-col>
                                        <h4 class="mb-3">Actually i'm work on Expert Code Software
                                            <br>
                                            and live near Belo Horizonte, MG - Brasil</h4>
                                        <h4 class="font-weight-light mb-5">You can see my github below:</h4>
                                        <router-link to="">
                                            <v-icon class="github-link" size="35">mdi-github</v-icon>
                                        </router-link>
                                    </v-col>
                                </v-row>
                            </div>
                        </div>
                    </v-col>
                </v-row>
            </v-col>
        </v-row>
    </v-sheet>
    <v-row class="container-tecnologies">
        <v-col align="start" class="pt-16 px-16" cols="12" lg="6">
            <h3 class="mb-16">Here are some tecnologies that i'm studying on moment:</h3>
           <v-row>
               <v-col align="center">
                   <v-row>
                       <v-col cols="6" lg="2">
                           <v-icon class="icon-tecnologies icon-html">mdi-language-html5</v-icon>
                       </v-col>
                       <v-col cols="6" lg="2">
                           <v-icon class="icon-tecnologies icon-css">mdi-language-css3</v-icon>
                       </v-col>
                       <v-col cols="6" lg="2">
                           <v-icon class="icon-tecnologies icon-js">mdi-language-javascript
                           </v-icon>
                       </v-col>
                       <v-col cols="6" lg="2">
                           <v-icon class="icon-tecnologies icon-ts">mdi-language-typescript
                           </v-icon>
                       </v-col>
                       <v-col cols="6" lg="2">
                           <v-icon class="icon-tecnologies icon-node">mdi-nodejs</v-icon>
                       </v-col>
                       <v-col cols="6" lg="2">
                           <v-icon class="icon-tecnologies icon-docker">mdi-docker</v-icon>
                       </v-col>
                   </v-row>
                   <v-row>
                       <v-col cols="6" lg="2">
                           <v-icon class="icon-tecnologies icon-boot">mdi-bootstrap</v-icon>
                       </v-col>
                       <v-col cols="6" lg="2">
                           <v-icon class="icon-tecnologies icon-react">mdi-react</v-icon>
                       </v-col>
                       <v-col cols="6" lg="2">
                           <v-icon class="icon-tecnologies icon-vue">mdi-vuejs</v-icon>
                       </v-col>
                       <v-col cols="6" lg="2">
                           <v-icon class="icon-tecnologies icon-git">mdi-git</v-icon>
                       </v-col>
                       <v-col cols="6" lg="2">
                           <v-icon class="icon-tecnologies icon-java">mdi-language-java</v-icon>
                       </v-col>
                       <v-col cols="6" lg="2">
                           <v-icon class="icon-tecnologies icon-spring">mdi-leaf</v-icon>
                       </v-col>
                   </v-row>
               </v-col>
           </v-row>
        </v-col>
        <v-col cols="12" lg="6">

        </v-col>
    </v-row>
    <v-sheet elevation="10">
        <v-row class="footer">
            <v-col align="center" class="mt-3" cols="6">
                <p class="font-weight-light footer-item">© Rodrigo Duarte's Website {{ new Date().getFullYear() }}</p>
            </v-col>
            <v-col align="center" class="mt-3" cols="6">
                <div>
                    <span class="font-weight-light footer-item">Home</span>
                    <v-icon>mdi-circle-small</v-icon>
                    <span class="font-weight-light footer-item">About</span>
                    <v-icon>mdi-circle-small</v-icon>
                    <span class="font-weight-light footer-item">Projects</span>
                    <v-icon>mdi-circle-small</v-icon>
                    <span class="font-weight-light footer-item">Contact</span>
                </div>
            </v-col>
        </v-row>
    </v-sheet>
</template>

<script>
import {defineComponent} from 'vue';

export default defineComponent({
    name: 'HomeView',
    components: {},
});
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@500&display=swap');

.desktop-div {
    display: block;
}

.footer {
    background-color: black;
    color: aliceblue;
    height: 10vh;
}

.icon-tecnologies {
    font-size: 90px !important;
    color: black !important;
}

.icon-tecnologies:hover {
    animation: iconJump 0.1s linear forwards;
}

@keyframes iconJump {
    from {
    }
    to {
        transform: scale(120%);
    }
}

.footer-item {
    font-family: 'Inter', sans-serif;
    color: #bbbbbb;
    font-size: 14px;
}

.footer-item:hover {
    color: aliceblue;
    cursor: pointer;
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

.main-container, .container-hello {
    background-color: black;
    color: aliceblue;
}

.container-hello {
    height: 60vh;
}

.container-tecnologies {
    height: 80vh;
}

.title-name {
    font-size: 45px;
}

.name-link {
    color: aliceblue;
    text-decoration: none;
    font-family: 'Inter', sans-serif;
}

.github-link {
    text-decoration: none;
    color: white;
}

.github-link:hover {
    cursor: pointer;
    color: #d3d3d3;
}

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

.icon-html:hover {
    color: #e34c26 !important;
    cursor: pointer;
}

.icon-css:hover {
    color: #2965f1 !important;
    cursor: pointer;
}

.icon-js:hover {
    color: #f0db4f !important;
    cursor: pointer;
}

.icon-ts:hover {
    color: #007acc !important;
    cursor: pointer;
}

.icon-java:hover {
    color: #cf88d8 !important;
    cursor: pointer;
}

.icon-spring:hover {
    color: #0a953a !important;
    cursor: pointer;
}

.icon-boot:hover {
    color: #59287a !important;
    cursor: pointer;
}

.icon-react:hover {
    color: #61dafb !important;
    cursor: pointer;
}

.icon-vue:hover {
    color: #42b883 !important;
    cursor: pointer;
}

.icon-docker:hover {
    color: #0db7ed !important;
    cursor: pointer;
}

.icon-node:hover {
    color: #3c873a !important;
    cursor: pointer;
}

.icon-git:hover {
    color: #e24329 !important;
    cursor: pointer;
}
</style>
