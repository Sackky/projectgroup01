<template>
  <v-app>
    <v-app-bar
      absolute
      color="#fcb69f"
      src="https://i.imgur.com/sD33gxz.jpg"
      app
    >
      <h1>Store</h1>
      <v-spacer />
    </v-app-bar>
    <v-main>
      <v-container>
        <div v-if="$store.state.page == 1">
          <sigin />
        </div>
        <div v-if="$store.state.page == 2">
          <register />
        </div>
        <div v-if="$store.state.page == 3">
          <forgetpassword />
        </div>
        <div v-if="$store.state.page == 4">
          <alreadyregistered />
        </div>        
        <div v-if="$store.state.page == 5">
          <confirmcode />
        </div>
        <div v-if="$store.state.page == 6">
          <changpassword />
        </div>
        <div v-if="$store.state.page == 7">
          <passchangedsuccess />
        </div>
        <div v-if="$store.state.page == 8">
          <homepage />
        </div>
      </v-container>
    </v-main>
    <v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed>
    </v-navigation-drawer>
    <v-footer :absolute="!fixed" app> </v-footer>
  </v-app>
</template>

<script>
import sigin from "./components/sigin";
import register from "./components/register"
import forgetpassword from "./components/forgetpassword"
import alreadyregistered from "./components/alreadyregistered"
import confirmcode from "./components/confirmcode"
import changpassword from "./components/changpassword"
import passchangedsuccess from "./components/passchangedsuccess"
import homepage from "./components/homepage"

export default {
  name: "App",

  components: {
    sigin,
    register,
    forgetpassword,
    alreadyregistered,
    confirmcode,
    changpassword,
    passchangedsuccess,
    homepage,

  },

  data() {
    return {
      page : 1,
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
    };
  },
};
</script>
