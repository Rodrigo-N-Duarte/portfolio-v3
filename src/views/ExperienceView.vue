<template>
    <v-row>
        <v-col>
            <NavBarDesktop/>
            <v-row class="container-about" justify="center">
                <v-col align="center">
                    <v-row class="px-lg-16">
                        <v-col align="start" class="px-lg-16">
                               <v-row>
                                   <v-col align="center">
                                       <h1 class="title-about mb-5 pl-10 mt-5">Experience</h1>
                                   </v-col>
                               </v-row>
                               <v-row class="mb-16">
                                   <v-col>
                                       <v-timeline align="start" side="end">
                                           <v-timeline-item
                                               v-for="(item, i) in items"
                                               :key="i"
                                               :dot-color="item.color"
                                               :icon="item.icon"
                                               fill-dot
                                           >
                                               <v-card>
                                                   <v-card-title>
                                                       {{item.title}}
                                                   </v-card-title>
                                                   <v-card-text class="bg-white text--primary">
                                                    <p class="my-2">{{item.content}}</p>
                                                   </v-card-text>
                                               </v-card>
                                           </v-timeline-item>
                                       </v-timeline>
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
    name: 'ExperienceView',
    components: {
        FooterComponent,
        NavBarDesktop
    },
    data() {
        return {
            items: [
                {
                    color: 'yellow',
                    icon: 'mdi-briefcase',
                    title: "Internship - Expert Code Software",
                    content: `Working on frontend and backend on a real enterprise and software factory. Working with teams and agile methods. Being part of squads
                    and having contact with modern technologies, like VueJS, Node with Fastify, Java and Spring Framework, SQL databases, Docker.`
                },
                {
                    color: 'purple',
                    icon: 'mdi-book',
                    title: "Monitor - University",
                    content: "Help other students learning the basics of programming, the logic, using C# and working like a partner to the university."
                },
                {
                    color: 'black',
                    icon: 'mdi-layers-triple',
                    title: "Graduating - Information Systems",
                    content: `Studying on PUC Minas - Betim, start the course on the start of 2022
                    and it's previous to end on final of 2025. However, i'm on 4 period and learning subjects linke OOP, data estructure and graphs.`
                },
            ],
        }
    }
});
</script>

<style>
.title-contact {
    font-size: 40px;
}
</style>
