<template>
    <v-row>
        <v-col>
            <NavBarDesktop/>
            <v-row class="container-about mb-10" justify="center">
                <v-col align="center">
                    <v-row class="px-lg-16">
                        <v-col align="start" class="px-lg-16">
                            <v-row class="mt-16">
                                <v-col align="center">
                                    <v-row >
                                        <v-col cols="12">
                                            <h1>
                                                <span v-for="(letter, index) in animatedTitle" :key="index"
                                                      class="letter-title-skills">
                          {{ letter !== " " ? letter : "&nbsp;" }}
                        </span>
                                            </h1>
                                        </v-col>
                                    </v-row>
                                    <div style="width: 70%">
                                        <h3 class="font-weight-medium">Have knowledge on backend and frontend areas</h3>
                                        <h3 class="font-weight-light">However I have my favorite technologies on which area,
                                        on frontend, I love work with VueJS because it's simple, productive and efficient and,
                                        on backend, appreciate softwares using Node and Spring because it's strong and trustable.</h3>
                                    </div>
                                </v-col>
                            </v-row>
                            <v-row class="container-tecnologies mb-16">
                                <v-col align="start" class="pt-16 px-16" cols="12">
                                    <v-row>
                                        <v-col align="center">
                                            <v-row justify="center">
                                                <v-col cols="6" lg="1">
                                                    <v-icon class="icon-tecnologies icon-html">mdi-language-html5
                                                    </v-icon>
                                                </v-col>
                                                <v-col cols="6" lg="1">
                                                    <v-icon class="icon-tecnologies icon-css">mdi-language-css3</v-icon>
                                                </v-col>
                                                <v-col cols="6" lg="1">
                                                    <v-icon class="icon-tecnologies icon-js">mdi-language-javascript
                                                    </v-icon>
                                                </v-col>
                                                <v-col cols="6" lg="1">
                                                    <v-icon class="icon-tecnologies icon-ts">mdi-language-typescript
                                                    </v-icon>
                                                </v-col>
                                                <v-col cols="12" lg="1">
                                                    <v-icon class="icon-tecnologies icon-node">mdi-nodejs</v-icon>
                                                </v-col>
                                            </v-row>
                                            <v-row justify="center">
                                                    <v-col cols="6" lg="1">
                                                        <v-icon class="icon-tecnologies icon-docker">mdi-docker</v-icon>
                                                    </v-col>
                                                <v-col cols="6" lg="1">
                                                    <v-icon class="icon-tecnologies icon-boot">mdi-bootstrap</v-icon>
                                                </v-col>
                                                <v-col cols="6" lg="1">
                                                    <v-icon class="icon-tecnologies icon-react">mdi-react</v-icon>
                                                </v-col>
                                                <v-col cols="6" lg="1">
                                                    <v-icon class="icon-tecnologies icon-vue">mdi-vuejs</v-icon>
                                                </v-col>
                                                <v-col cols="6" lg="1">
                                                    <v-icon class="icon-tecnologies icon-git">mdi-git</v-icon>
                                                </v-col>
                                                <v-col cols="6" lg="1">
                                                    <v-icon class="icon-tecnologies icon-java">mdi-language-java
                                                    </v-icon>
                                                </v-col>
                                                <v-col cols="12" lg="1">
                                                    <v-icon class="icon-tecnologies icon-spring">mdi-leaf</v-icon>
                                                </v-col>
                                            </v-row>
                                        </v-col>
                                    </v-row>
                                </v-col>
                            </v-row>
                        </v-col>
                    </v-row>
                </v-col>
            </v-row>
        </v-col>
    </v-row>
    <FooterComponent class="mt-16"/>
</template>

<script>
import {defineComponent} from 'vue';
import NavBarDesktop from "@/components/NavBarDesktop.vue";
import FooterComponent from "@/components/FooterComponent.vue";

export default defineComponent({
    name: 'SkillsView',
    components: {
        FooterComponent,
        NavBarDesktop
    },
    data() {
        return {
            animatedTitle: []
        }
    },
    methods: {
        setTitle() {
            const title = "Skills"
            for (const letter of title) {
                this.animatedTitle.push(letter)
            }
        }
    },
    beforeMount() {
        this.setTitle()
    }
});
</script>

<style>

.icon-tecnologies {
    font-size: 100px !important;
    color: black !important;
}

.icon-tecnologies:hover {
    animation: jumpIcon 0.1s linear forwards;
}

@keyframes jumpIcon {
    from {
    }
    to {
        transform: scale(120%);
    }
}

.letter-title-skills {
    font-weight: bold;
    font-size: 80px !important;
}

.letter-title-skills:hover {
    display: inline-block;
}

.letter-title-skills:hover {
    cursor: pointer;
    animation: fontJump 0.5s linear forwards;
}

@keyframes fontJump {
    from {
        -webkit-transform: scale3d(1, 1, 1);
        transform: scale3d(1, 1, 1);
    }

    20% {
        color: #f4c95d;
    }

    30% {
        -webkit-transform: scale3d(1.25, 0.75, 1);
        transform: scale3d(1.25, 0.75, 1);
    }

    40% {
        -webkit-transform: scale3d(0.75, 1.25, 1);
        transform: scale3d(0.75, 1.25, 1);
    }

    50% {
        color: #f4be49;
        -webkit-transform: scale3d(1.15, 0.85, 1);
        transform: scale3d(1.15, 0.85, 1);
    }

    65% {
        -webkit-transform: scale3d(0.95, 1.05, 1);
        transform: scale3d(0.95, 1.05, 1);
    }

    75% {
        -webkit-transform: scale3d(1.05, 0.95, 1);
        transform: scale3d(1.05, 0.95, 1);
    }

    to {
        color: #f4b049;
        -webkit-transform: scale3d(1, 1, 1);
        transform: scale3d(1, 1, 1);
    }
}

</style>
