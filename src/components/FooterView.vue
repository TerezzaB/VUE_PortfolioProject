<template>
    <v-footer>
        <v-card elevation="0" rounded="0" width="100%" class="bg-grey text-center">
            <v-card-text>
                <v-btn class="mt-4" icon="fas fa-comment" variant="plain" color="#FFF"></v-btn>
                <v-btn class="mt-4" icon="fas fa-university" variant="plain" color="#FFF"></v-btn>
                <v-btn class="mt-4" icon="fas fa-wifi" variant="plain" color="#FFF"></v-btn>
                <v-btn class="mt-4" icon="fas fa-podcast" variant="plain" color="#FFF"></v-btn>
            </v-card-text>
            <v-card-text>
                <b>{{ new Date().getFullYear() }} - </b>
                <b>AAE IdeaPro All Rights Reserved</b>
            </v-card-text>
        </v-card>
    </v-footer>
</template>

<script>
    export default {}
</script>

<style>
.v-footer { padding: 8px 0 0 !important; }
</style>