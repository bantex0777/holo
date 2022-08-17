<template>
  <v-app-bar app color="#FEFDF4" flat class="px-12">
    <v-img max-height="33" max-width="85.04" src="@/assets/logo.png" />
    <v-spacer></v-spacer>
    <v-btn @click="scroll('context')" color="#4B6709" text class="inter"
      >Contact Us</v-btn
    >
    <v-btn @click="scroll('login')" color="#4B6709" text>Log In</v-btn>
  </v-app-bar>
</template>

<script>
import Logo from "./../assets/logo.svg";

export default {
  comments: {
    Logo,
  },
  methods: {
    scroll(refName) {
      const element = document.getElementById(refName);
      element.scrollIntoView({ behavior: "smooth" });
    },
  },
};
</script>

<style>
@font-face {
  font-family: inter-font;
  src: url("@/fonts/Inter-Regular.ttf");
}

.inter {
  font-family: inter-font;
}
</style>