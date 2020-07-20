<template>
  <v-app>
     <NavigationComponent/>
      <router-view>
          <LoginViewComponent />
          <RegisterViewComponent />
          <HomeViewComponent />
      </router-view>
  </v-app>
</template>

<script>

import NavigationComponent from "./components/NavigationComponent/NavigationComponent";
import LoginViewComponent from "./views/LoginViewComponent";
import RegisterViewComponent from "./views/RegisterViewComponent";
import HomeViewComponent from "./views/HomeViewComponent";
export default {
  name: 'App',
  components: {
      HomeViewComponent,
      LoginViewComponent,
      NavigationComponent,
      RegisterViewComponent
  }
};
</script>
<style>
    a{
        text-decoration: none;
    }
    a:visited{
        color:white;
    }
    body{
        overflow: no-display;
        overflow: hidden;
    }
</style>