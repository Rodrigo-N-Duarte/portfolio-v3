<template>
    <v-row>
        <v-col>
            <NavBarDesktop/>
            <v-row class="container-about" justify="center">
                <v-col align="center">
                    <v-row class="px-lg-16">
                        <v-col align="start" class="px-lg-16">
                            <v-card class="pa-10 ma-5 mx-lg-16" elevation="24">
                                <v-row>
                                    <v-col align="start">
                                        <h1 class="title-about mb-5 pl-10 mt-5">Contact</h1>
                                    </v-col>
                                </v-row>
                                <v-row class="mb-16">
                                    <v-col class="mb-16 px-12" cols="12" lg="6" style="margin-top: 8%">
                                        <div>
                                            <h2 class="title-contact">
                                                Got a problem to solve?
                                            </h2>
                                            <h3 class="font-weight-medium">
                                                Get your space suit ready and tell me your ideas to develop your dream
                                                website.
                                            </h3>
                                            <h4 class="mt-5">
                                                <a href="mailto:duarte.n.rodrigo@gmail.com"
                                                   style="text-decoration: none; color: goldenrod">duarte.n.rodrigo@gmail.com</a>
                                            </h4>
                                        </div>
                                    </v-col>
                                    <v-col align="center" cols="12" lg="6">
                                        <h2 class="mb-10 font-weight-medium">
                                            Want to contact me more quickly?
                                        </h2>
                                        <form>
                                            <v-text-field
                                                    label="Name"
                                                    variant="outlined"
                                            ></v-text-field>
                                            <v-text-field
                                                    label="Email"
                                                    variant="outlined"
                                            ></v-text-field>
                                            <v-textarea
                                                    label="Message"
                                                    variant="outlined">
                                            </v-textarea>
                                            <v-btn
                                                    class="me-4"
                                                    type="submit"
                                                    variant="outlined"
                                            >
                                                Submit
                                                <v-icon class="ml-5">mdi-send</v-icon>
                                            </v-btn>

                                            <v-btn
                                                    variant="outlined"
                                            >
                                                Clear
                                            </v-btn>
                                        </form>
                                    </v-col>
                                </v-row>
                                <v-row class="my-10">
                                    <v-col align="center">
                                        <h3 class="mb-5 font-weight-medium">You can contact me on my social media too,
                                            feel free to send me a message</h3>
                                        <div>
                                            <a href="https://github.com/Rodrigo-N-Duarte?tab=repositories" target="_blank">
                                                <v-icon class="mx-3 text-decoration-none" color="black"  size="40">mdi-github</v-icon>
                                            </a>
                                            <a href="https://www.linkedin.com/in/rodrigo-n-duarte/" target="_blank">
                                                <v-icon class="mx-3 text-decoration-none" color="black"  size="40">mdi-linkedin</v-icon>
                                            </a>
                                            <a href="https://www.instagram.com/rodrig0d__/" target="_blank">
                                                <v-icon class="mx-3 text-decoration-none" color="black"  size="40">mdi-instagram</v-icon>
                                            </a>
                                            <a href="https://wa.me/31999254045" target="_blank">
                                                <v-icon class="mx-3 text-decoration-none" color="black" size="40">mdi-whatsapp</v-icon>
                                            </a>
                                        </div>
                                    </v-col>
                                </v-row>
                            </v-card>
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
    name: 'ContactView',
    components: {
        FooterComponent,
        NavBarDesktop
    },
});
</script>

<style>
.title-contact {
    font-size: 40px;
}
</style>
