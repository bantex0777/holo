<template>
  <v-container class="hero" fluid>
    <h1 style="color: white" class="center">What Ho-Lo can do for you</h1>
    <v-row justify="center" class="ma-16">
      <v-col cols="4" class="mt-16">
        <v-img
          contain
          height="32"
          width="32"
          src="@/assets/edit.png"
        ></v-img>
        <h2 class="mt-6" style="color: white">
          Get a personalized calculation
        </h2>
        <p class="mt-6" style="color: white">
          Get to know what you can afford. Try calculating your home loan
          monthly amortization
        </p></v-col
      >
      <v-col cols="4" class="mt-16">
         <v-img
          contain
          height="32"
          width="32"
          src="@/assets/file-text.png"
        ></v-img>
        <h2 class="mt-6" style="color: white">Calculate offline</h2>
        <p class="mt-6" style="color: white">
          Get to know what you can afford. Try calculating your home loan
          monthly amortization
        </p></v-col
      >
      <v-col cols="4" class="mt-16">
          <v-img
          contain
          height="32"
          width="32"
          src="@/assets/users.png"
        ></v-img>
        <h2 class="mt-6" style="color: white">
          Create amortization forms for clients
        </h2>
        <p class="mt-6" style="color: white">
          Get to know what you can afford. Try calculating your home loan
          monthly amortization
        </p></v-col
      >
    </v-row>
  </v-container>
</template>

<script>
export default {};
</script>

<style>
.hero {
  border-radius: 25px;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-image: url("@/assets/house.png"),
    -webkit-linear-gradient(left, rgba(0, 0, 0, 1) 0%, rgba(0, 0, 0, 1) 4%, rgba(
            0,
            0,
            0,
            0
          )
          90%, rgba(0, 0, 0, 0) 100%);
  background-blend-mode: color;
  width: 90%;
}

.center {
  margin: 0;
  margin-top: 30px;
  position: absolute;
  left: 50%;
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
}
</style>