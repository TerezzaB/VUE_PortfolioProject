<template>
   <v-app-bar app color="black" dark flat class="px-12">
    <v-btn >
        <v-icon color="purple" left class="mr-2">fas fa-signature</v-icon>Terezza
    </v-btn>
    <v-spacer></v-spacer>
    <v-btn text @click="scroll('home')" class="text-purple">Home</v-btn>
    <v-btn text @click="scroll('about')">About</v-btn>
    <v-btn text @click="scroll('portfolio')">Portfolio</v-btn>
    <v-btn text @click="scroll('services')">Services</v-btn>
    <v-btn text @click="scroll('page')">Page</v-btn>
    <v-btn text @click="scroll('biog')">Blog</v-btn>
    <v-btn text @click="scroll('contact')">Contact</v-btn>
   </v-app-bar>
</template>

<script>
    export default {
        methods: {
            scroll(refName) {
                const element = document.getElementById(refName);
                element.scrollIntoView({ behavior: "smooth" });
            }
        }
    }
</script>

<style scoped>
    v-app-bar { background-color: #000; }
    @media(max-width: 400px) {
        v-btn { font-size: 12px; }
    }
</style>
