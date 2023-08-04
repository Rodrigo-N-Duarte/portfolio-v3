<template>
    <v-sheet elevation="10">
        <v-row class="main-container">
            <v-col>
                <NavBarDesktop/>
                <v-row class="container-hello dark-texture-background" justify="center">
                    <v-col align="center">
                        <div>
                            <v-avatar size="200">
                                <v-img cover
                                       height="100%"
                                       src="../assets/profile.jpg"></v-img>
                            </v-avatar>
                            <div>
                                <div class="mb-5 mt-3">
                                    <h1 class="title-name">Hi, I'm Rodrigo</h1>
                                    <h3 class="font-weight-light">I'm a developer, who loves working on frontend and
                                        backend too but, perhaps, hate both of then.
                                        <br>Just kidding :) love coding ☕</h3>
                                </div>
                                <v-row>
                                    <v-col>
                                        <h4 class="mb-3">Actually i'm working on - <span style="color: gold">Expert Code Software</span> -
                                            <br>
                                            and living near Belo Horizonte, MG - Brasil</h4>
                                        <h4 class="font-weight-light mb-5">You can see my github and linkedin below:</h4>
                                        <a href="https://github.com/Rodrigo-N-Duarte?tab=repositories" target="_blank">
                                            <v-icon class="github-link mx-2" size="35">mdi-github</v-icon>
                                        </a>
                                        <a href="https://www.linkedin.com/in/rodrigo-n-duarte/" target="_blank">
                                            <v-icon class="github-link mx-2" size="35">mdi-linkedin</v-icon>
                                        </a>
                                    </v-col>
                                </v-row>
                            </div>
                        </div>
                    </v-col>
                </v-row>
            </v-col>
        </v-row>
    </v-sheet>
    <FooterComponent/>
</template>

<script>
import {defineComponent} from 'vue';
import NavBarDesktop from "@/components/NavBarDesktop.vue";
import FooterComponent from "@/components/FooterComponent.vue";

export default defineComponent({
    name: 'HomeView',
    components: {
        FooterComponent,
        NavBarDesktop
    },
});
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@500&display=swap');

.px-40p {
    padding-right: 20%;
    padding-left: 20%;
}

.main-container, .container-hello {
    color: aliceblue;
}

.container-hello {
    height: 70vh;
}

.dark-texture-background {
    background-color: #000000;
    background-image: url("https://www.transparenttextures.com/patterns/fabric-of-squares.png");
    background-repeat:repeat;
}

.title-name {
    font-size: 35px;
    overflow: hidden;
    border-right: .15em solid orange;
    white-space: nowrap;
    margin: 0 auto;
    letter-spacing: .15em;
    animation: typewriter 2s steps(16) 1s 1 normal both,
    blinkTextCursor 750ms steps(16) infinite normal;
}
@keyframes typewriter{
    from{width: 0;}
    to{width: 9em;}
}
@keyframes blinkTextCursor{
    from{border-right-color: rgba(255,255,255,.75);}
    to{border-right-color: transparent;}
}

.github-link {
    text-decoration: none;
    color: white;
}

.github-link:hover {
    cursor: pointer;
    color: #d3d3d3;
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
