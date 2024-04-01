<template>
        <v-row class="footer mx-0">
            <v-col align="center" class="mt-3" cols="12" lg="6">
                <p class="font-weight-light footer-item">© Rodrigo Duarte's Website {{ new Date().getFullYear() }}</p>
            </v-col>
            <v-col align="center" class="mt-3" cols="12" lg="6">
                    <a href="/" class="default-footer-link">
                        <span class="font-weight-light footer-item">Home</span>
                        <v-icon>mdi-circle-small</v-icon>
                    </a>
                    <a href="/about" class="default-footer-link">
                        <span class="font-weight-light footer-item">About</span>
                        <v-icon>mdi-circle-small</v-icon>
                    </a>
                    <a href="/skills" class="default-footer-link">
                        <span class="font-weight-light footer-item">Skills</span>
                        <v-icon>mdi-circle-small</v-icon>
                    </a>
                    <a href="/experience" class="default-footer-link">
                        <span class="font-weight-light footer-item">Experience</span>
                        <v-icon>mdi-circle-small</v-icon>
                    </a>
            </v-col>
        </v-row>
</template>
<script>
export default {
    name: "FooterComponent"
}
</script>

<style>
.default-footer-link {
    font-size: 15px;
    color: aliceblue;
    text-decoration: none;
    position: relative;
    overflow: hidden;
    padding: 5px;
}

.footer {
    background-color: #0e0e0e;
    background-image: url("https://www.transparenttextures.com/patterns/3px-tile.png");
    background-repeat: repeat;
    color: aliceblue;
    bottom: 0;
    width: 100%;
    position: absolute;
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
</style>
