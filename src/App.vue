<template>
  <body>
    <navbarVue />
    <homeVue />
    <aboutVue />
    <skillsVue />
    <projectsVue />
    <footerVue class="footerVue" />
  </body>
</template>

<script>
import aboutVue from './components/about.vue'
import footerVue from './components/footer.vue'
import homeVue from './components/home.vue'
import navbarVue from './components/navbar.vue'
import projectsVue from './components/projects.vue'
import skillsVue from './components/skills.vue'

export default {
  name: 'App',
  components: {
    navbarVue,
    homeVue,
    aboutVue,
    skillsVue,
    projectsVue,
    footerVue
  }
}
</script>

<style>
  *{
    margin: 0;
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  }

  body{
    background-color: #30303C;
  }
</style>