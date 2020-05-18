<template>
  <v-app>
     <NavigationComponent/>
      <router-view>
          <LoginViewComponent />
          <RegisterViewComponent />
      </router-view>
  </v-app>
</template>

<script>

import NavigationComponent from "./components/NavigationComponent/NavigationComponent";
import LoginViewComponent from "./views/LoginViewComponent";
import RegisterViewComponent from "./views/RegisterViewComponent";
export default {
  name: 'App',
  components: {
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
</style>