<template>
    <v-row>
        <v-col>
            <NavBarDesktop/>
            <v-row class="container-about mb-16" justify="center">
                <v-col align="center">
                    <v-row>
                        <v-col align="start" class="px-40p">
                            <v-row>
                                <v-col align="start">
                                    <h1 class="title-about mb-5 pl-10 mt-5">About</h1>
                                </v-col>
                            </v-row>
                            <v-row>
                                <v-col align="center">
                                    <v-img
                                            aspect-ratio="16/9"
                                            cover
                                            src="../assets/aboutBanner.jpg"
                                            width="80%"
                                            height="50%"
                                    ></v-img>
                                    <v-row>
                                        <v-col cols="12" lg="2"></v-col>
                                        <v-col cols="12" lg="8"><h3 class="my-10 about-text">Hi, my name's Rodrigo. I'm
                                            Brazilian software engineer
                                            and student System Information in Belo Horizonte, state of Minas
                                            Gerais.</h3>
                                            <h3 class="my-10 about-text"> I started my carreer on the initial months of
                                                2021, and haven't stopping my
                                                studies yet, and i will not, cause i love what i'm doing.</h3>
                                            <h3 class="my-10 about-text">Experience on Expert Code Software, which is
                                                a software company and
                                                industry and implements system for other enterprises. There we develop
                                                and maintain web systems applications,
                                                using the most modern framework and technologies on the moment, such as
                                                Spring Framework, VueJS, ReactJS, Node,
                                                Docker, K8S and cloud platforms as AWS for example.</h3>
                                          <h3 class="my-10 about-text">But is actually, I'm working on Nic-Labs Tech, which
                                          is a SAP Consult Enterprise. Having contact with SAP technologies such as SAP Fiori
                                          and CDS Views. Also doing some projects in integration with SAP, but focusing on mobile
                                          devices, using React Native.</h3>
                                        </v-col>
                                        <v-col cols="12" lg="2"></v-col>
                                    </v-row>
                                </v-col>
                            </v-row>
                        </v-col>
                    </v-row>
                </v-col>
            </v-row>
        </v-col>
    </v-row>
    <FooterComponent/>
</template>
<script>
import {defineComponent} from 'vue';
import NavBarDesktop from "@/components/NavBarDesktop.vue";
import FooterComponent from "@/components/FooterComponent.vue";

export default defineComponent({
    name: 'AboutView',
    components: {FooterComponent, NavBarDesktop},
});
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');

.container-about {
    margin-bottom: 5%;
}

.title-about {
    font-size: 50px;
}

.about-text {
    text-align: justify;
    word-spacing: 5px !important;
    font-weight: lighter;
    font-family: 'Montserrat', sans-serif;
}
</style>
