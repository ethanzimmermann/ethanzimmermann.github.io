<template>
  <div id="app">
    <VueNavigationBar :options="navbarOptions" />
    <HelloWorld msg="Welcome to my site!!!"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import VueNavigationBar from "vue-navigation-bar"
import "vue-navigation-bar/dist/vue-navigation-bar.css";

export default {
  name: 'App',
  components: {
    HelloWorld,
    VueNavigationBar
  },
  data() {
    return {
      navbarOptions: {
        elementId: "main-navbar",
        isUsingVueRouter: false,
        mobileBreakpoint: 992,
        brandImagePath: "./",
        brandImage: require("../src/assets/logo.png"),
        brandImageAltText: "brand-image",
        collapseButtonOpenColor: "grey",
        collapseButtonCloseColor: "blue",
        showBrandImageInMobilePopup: true,
        ariaLabelMainNav: "Main Navigation",
        tooltipAnimationType: "shift-away",
        tooltipPlacement: "bottom",
        menuOptionsRight: [
          {
            type: "link",
            text: "Coming Soon",
            arrowColor: "black",
            subMenuOptions: [
              {
                type: "link",
                text: "Personal Interests",
                subText: "Activities and topics I enjoy pursuing and researching",
                path: { name: "" },
                arrowColor: "#659CC8",
              },
              {
                type: "hr",
              },
              {
                type: "link",
                text: "Untitled Animation Project",
                subText: "",
                path: { name: "" },
                arrowColor: "#659CC8",
              },
              {
                type: "hr",
              },
              {
                type: "link",
                text: "Graphing Tool Demos",
                subText: "I will be posting data displayed in a variety of different vue-friendly graphing packages and comparing them based on functionality, extensibility, and ease of use.",
                path: { name: "" },
                arrowColor: "#659CC8",
              }
            ]
          }
        ],
        menuOptionsLeft: [
          {
            type: "link",
            text: "Home",
            path: { name: "" },
          },
          {
            type: "link",
            text: "Professional Work",
            path: { name: "" },
          }
        ]
      }
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.vnb .button-red {
  background: #ff3b30;
}
 
.vnb .button-red:hover {
  background: #fc0d00;
}
</style>
