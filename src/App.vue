<template>
  <div id="app" :class="{ 'hide-menu': !isMenuVisible }">
    <HeaderTemplate title="Base de Conhecimento" :hideToggle="false" />
    <MenuTemplate />
    <ContentTemplate />
    <FooterTemplate />
  </div>
</template>

<script>
import { mapState } from "vuex";
import HeaderTemplate from "./components/template/HeaderTemplate.vue";
import MenuTemplate from "./components/template/MenuTemplate.vue";
import ContentTemplate from "./components/template/ContentTemplate.vue";
import FooterTemplate from "./components/template/FooterTemplate.vue";

export default {
  name: "App",
  components: {
    HeaderTemplate,
    MenuTemplate,
    ContentTemplate,
    FooterTemplate,
  },
  computed: mapState(["isMenuVisible"]),
};
</script>

<style>
* {
  font-family: "Lato", sans-serif;
}

Body {
  margin: 0;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  height: 100vh;
  display: grid;
  grid-template-rows: 60px 1fr 40px;
  grid-template-columns: 300px 1fr;
  grid-template-areas:
    "header header"
    "menu content"
    "menu footer";
}

#app.hide-menu {
  grid-template-areas:
    "header header"
    "content content"
    "footer footer";
}
</style>
