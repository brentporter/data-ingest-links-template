<template>
  <v-layout>
    <v-app-bar title="DAC REDI Data Ingest Index" color="indigo">
      <template v-slot:prepend>
        <v-app-bar-nav-icon

        ></v-app-bar-nav-icon>
      </template>
    </v-app-bar>
<!--    <v-navigation-drawer
        class="bg-blue ml-2"
        theme="dark"
        v-model="drawer"
        floating
    >
      <v-list color="transparent">
        <v-list-item prepend-icon="mdi-view-dashboard" title="Dashboard"></v-list-item>
        <v-list-item prepend-icon="mdi-account-box" title="Account"></v-list-item>
        <v-list-item prepend-icon="mdi-gavel" title="Admin"></v-list-item>
      </v-list>

    </v-navigation-drawer>-->

    <v-main>
      <v-container fluid color="indigo">
        <ContentList/>
      </v-container>
<!--      <ElevationControls/>-->
      <!--      <LeafletMap/>-->
    </v-main>
  </v-layout>
</template>

<script >
import { RouterLink, RouterView } from 'vue-router'
import ContentList from "@/components/ContentList.vue";
/*
import LeafletMap from "@/components/LeafletMap.vue";
import ControlPallete from "@/components/ControlPallete.vue";
import ElevationControls from "@/components/ElevationControls.vue";
*/
export default {
  components: {ContentList},
  data () {
    return {
      drawer: false,
    }
  },
}
</script>

<style>
.esri-dynamic-attribution{
  display: none !important;
}
.leaflet-control-attribution{
  display: none !important;
}
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

#scriptText{
  font-weight: bolder !important;
}

@media (min-width: 1248px) {
  header {
    display: flex;
    /* place-items: center;
     padding-right: calc(var(--section-gap) / 2);*/
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
