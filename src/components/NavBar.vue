<template>
    <v-app-bar class="px-16" elevation="0" style="background-color: red">
        <v-row justify="start">
            <v-app-bar-title>Rodrigo Duarte</v-app-bar-title>
            <router-link to="/about">
                <v-app-bar-title>About</v-app-bar-title>
            </router-link>
        </v-row>
    </v-app-bar>
</template>

<script>

export default {
    name: 'NavBar',
    data() {
        return {}
    },
}
</script>
