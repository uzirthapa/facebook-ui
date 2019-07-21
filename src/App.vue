<template>
  <v-app>
    <Toolbar/>
    <DrawerLeft/>
    <DrawerRight/>

    <v-content>
      <Feed/>
    </v-content>
  </v-app>
</template>

<script>
import Toolbar from './components/ToolBar'
import DrawerLeft from './components/DrawerLeft'
import DrawerRight from './components/DrawerRight'
import Feed from './components/Feed'

export default {
  name: 'App',
  components: {
    Toolbar,
    DrawerLeft,
    DrawerRight,
    Feed
  },
  data: () => ({
    //
  }),
};
</script>
<style>
@import url("https://fonts.googleapis.com/css?family=Questrial");

.questrial {
  font-family: "Questrial";
}
</style>
