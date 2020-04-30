<template>
    <span>
        <v-toolbar app color="teal lighten-2" dark>
            <v-toolbar-side-icon class="hidden-md-and-up" @click="drawer = !drawer"></v-toolbar-side-icon>
            <v-spacer class="hidden-md-and-up"></v-spacer>
            <img src="../assets/white-labs-plain.png" height="50" />
            <v-spacer class="hidden-sm-and-down"></v-spacer>
            <v-btn flat class="hidden-sm-and-down" text rounded>HOME</v-btn>
            <v-btn flat class="hidden-sm-and-down" text rounded>LOGIN</v-btn>
        </v-toolbar>
    </span>
</template>
