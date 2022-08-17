<template>
  <v-app class="inter">
    <NavBar />
    <div>
      <v-main>
        <Header />
        <Info class="mt-16" />
        <AppContent class="mt-16" />
        <v-container class="mx-16 mt-16">
          <v-row>
            <v-col cols="12">
              <h1 class="text-center">
                Calculate and save<em style="color:#CCEF85">*</em>  your forms from anywhere
              </h1>
              <p class="text-center my-10">
                Access the Ho-Lo app wherever you are and save your forms on
                your mobile phone
              </p>
                <v-row class="mx-6">
                  <v-col cols="6">
                    <v-card color="#FEFDF4" elevation="4" class="rounded-lg">
                      <v-container>
                        <h2>Provide the following details</h2>
                        <v-col cols="5">
                          <v-text-field dense messages="Maximum age is 65" label="Age" outlined></v-text-field>
                        </v-col>
                        <v-col cols="12">
                          <v-container>
                            <h4 class="mb-2">Select Property Type</h4>
                            <v-row>
                              <v-col cols="2">
                                <v-card
                                  width="110"
                                  height="90"
                                  color="#DEE6C6"
                                  class="
                                    d-flex
                                    align-center
                                    flex-column
                                    rounded-lg
                                  "
                                >
                                  <v-img
                                    class="mt-6 mx-6 mb-1"
                                    contain
                                    height="22"
                                    width="22"
                                    src="@/assets/home.png"
                                  ></v-img>
                                  <span class="mb-6 mx-1">House & Lot</span>
                                </v-card>
                              </v-col>

                              <v-col cols="2">
                                <v-card
                                  width="110"
                                  height="90"
                                  color="#DEE6C6"
                                  class="
                                    trucksicons
                                    d-flex
                                    align-center
                                    flex-column
                                    rounded-lg
                                  "
                                >
                                  <v-img
                                    class="mt-6 mx-6 mb-1"
                                    contain
                                    height="22"
                                    width="22"
                                    src="@/assets/map-pin.png"
                                  ></v-img>
                                  <span class="mb-6 mx-1">Lot only</span>
                                </v-card>
                              </v-col>

                              <v-col cols="2">
                                <v-card
                                  width="110"
                                  height="90"
                                  color="#DEE6C6"
                                  class="
                                    trucksicons
                                    d-flex
                                    align-center
                                    flex-column
                                    rounded-lg
                                  "
                                >
                                  <v-img
                                    class="mt-6 mx-6 mb-1"
                                    contain
                                    height="24"
                                    width="24"
                                    src="@/assets/key.png"
                                  ></v-img>
                                  <span class="mb-6 mx-1">Condominium</span>
                                </v-card>
                              </v-col>
                            </v-row>
                          </v-container>
                        </v-col>
                        <v-col cols="12">
                          <v-row>
                            <v-col cols="5">
                              <v-text-field
                              dense
                                label="Property Amount"
                                outlined
                              ></v-text-field>
                            </v-col>
                            <v-col cols="5">
                              <v-text-field
                              dense
                                label="Downpayment %"
                                outlined
                              ></v-text-field>
                            </v-col>
                          </v-row>
                          <v-row>
                            <v-col cols="5">
                              <v-text-field
                              dense
                                label="Loanable Amount"
                                outlined
                              ></v-text-field>
                            </v-col>
                            <v-col cols="5">
                              <v-text-field
                              dense
                                label="Loan Terms in Years"
                                outlined
                              ></v-text-field>
                            </v-col>
                          </v-row>
                          <v-row>
                            <v-col cols="5">
                              <v-text-field
                              dense
                                label="Interest Rate %"
                                outlined
                              ></v-text-field>
                            </v-col>
                          </v-row>
                          <v-row>
                            <v-col class="text-right" cols="12"
                              ><v-btn
                                class="mx-3"
                                color="#DEE6C6"
                                elevation="2"
                                rounded
                                >Clear</v-btn
                              >
                              <v-btn
                                class="mx-3"
                                dark
                                color="#4B6709"
                                elevation="2"
                                rounded
                                >Calculate</v-btn
                              ></v-col
                            >
                          </v-row>
                        </v-col>
                      </v-container>
                    </v-card>
                  </v-col>
                  <v-col cols="6">
                    <v-card color="#FEFDF4" elevation="4" class="rounded">
                      <v-container>
                        <h2>Here’s your monthly amortization</h2>
                        <v-col cols="12">
                          <v-card
                            color="#DEE6C6"
                            elevation="4"
                            class="rounded"
                          >
                            <v-container>
                              <v-row class="ma-1">
                                <p>Required gross monthly income</p>
                                <v-spacer></v-spacer>
                                <v-icon>mdi-alert-octagon-outline</v-icon>
                                <v-col cols="12">
                                  <h2>Php 50,000.00</h2>
                                </v-col>
                              </v-row>
                            </v-container>
                          </v-card>
                        </v-col>
                        <v-col cols="12">
                          <template class="ma-6">
                            <v-data-table
                              :headers="headers"
                              :items="dummyData"
                              :items-per-page="5"
                              class="elevation-1"
                            ></v-data-table>
                          </template>
                        </v-col>
                      </v-container>
                    </v-card>
                  </v-col>
                </v-row>
            </v-col>
          </v-row>
        </v-container>
      </v-main>
    </div>
    <v-spacer></v-spacer>
    <v-footer color="white">
      <v-row justify="center" class="mt-16">
        <v-col class="lighten-2 py-4" cols="2">
          <v-img max-height="33" max-width="95" src="@/assets/logo.png" />
        </v-col>
        <v-col class="lighten-2 py-4 text-center" cols="2">
          <h4 style="color:black">Product</h4>
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
          <h4 style="color:black">Company</h4>
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
  </v-app>
</template>

<script>
import NavBar from "./components/Navbar.vue";
import Header from "./components/Header.vue";
import Info from "./components/InfoContent.vue";
import AppContent from "./components/AppContent.vue";

export default {
  name: "App",

  components: {
    NavBar,
    Header,
    Info,
    AppContent,
    AppContent,
  },

  data: () => ({
    items: [
      { text: "Overview" },
      { text: "Mobile App" },
      { text: "Term & privacy" },
    ],
    Company: [{ text: "About Us" }],
    headers: [
      {
        text: "Period",
        value: "index",
      },
      { text: "Monthly Payment", value: "monthlyPayment" },
      { text: "Principal", value: "principal" },
      { text: "Interest", value: "interest" },
      { text: "Pricipal Balance", value: "principalBalance" },
    ],
    dummyData: [
      {
        index: 1,
        monthlyPayment: "8,394.11",
        principal: "2,164.18",
        interest: "6,229.93",
        principalBalance: "932,324.85",
      },
      {
        index: 2,
        monthlyPayment: "8,394.11",
        principal: "2,164.18",
        interest: "6,229.93",
        principalBalance: "932,324.85",
      },
      {
        index: 3,
        monthlyPayment: "8,394.11",
        principal: "2,164.18",
        interest: "6,229.93",
        principalBalance: "932,324.85",
      },
    ],
  }),
};
</script>
<style scoped>
@font-face {
  font-family: inter;
  src: url("@/fonts/Inter-Regular.ttf");
}

.inter {
  font-family: inter;
}
.top {
  margin-top: 180px;
}

.white {
  color: white;
}

.transparent {
  background-color: white !important;
  opacity: 0.65;
  border-color: transparent !important;
}
.center {
  margin: 0;
  margin-top: 30px;
  position: absolute;
  left: 50%;
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
}

.center-p {
  margin: auto;
  margin-top: 5%;
  position: absolute;
}
</style>
