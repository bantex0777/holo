<template>
  <v-footer width="auto" color="#FF9E80" padless>
    <v-row justify="center" no-gutters class="mt-16">
      <v-col class="lighten-2 py-4" cols="1">
        <v-img max-height="33" max-width="95" src="@/assets/logo.png" />
      </v-col>
      <v-col class="lighten-2 py-4 text-center" cols="2">
        <h4>Product</h4>
        <v-list>
          <v-list-item-group>
            <v-list-item v-for="(item, i) in items" :key="i">
              <v-list-item-content>
                <v-list-item-title v-text="item.text"></v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-col>
      <v-col class="lighten-2 py-4 text-center" cols="2">
        <h4>Company</h4>
        <v-list>
          <v-list-item-group>
            <v-list-item v-for="(item, i) in Company" :key="i">
              <v-list-item-content>
                <v-list-item-title v-text="item.text"></v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-col>
    </v-row>
    <v-spacer></v-spacer>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    items: [
      { text: "Overview" },
      { text: "Mobile App" },
      { text: "Term & privacy" },
    ],
    Company: [{ text: "About Us" }],
  }),
};
</script>

<style>
</style>