<template>
  <MainBanner />
  <AboutMe />
  <ProCareer />
  <SkillSet />
  <ProjectsWorks />
  <ContactMe />
</template>

<script>
import MainBanner from './components/MainBanner.vue'
import AboutMe from './components/AboutMe.vue'
import ProCareer from './components/ProCareer.vue'
import SkillSet from './components/SkillSet.vue'
import ProjectsWorks from './components/ProjectsWorks.vue'
import ContactMe from './components/ContactMe.vue'

export default {
  name: 'App',
  components: {
    MainBanner,
    AboutMe,
    ProCareer,
    SkillSet,
    ProjectsWorks,
    ContactMe
  }
}
</script>

<style>
html {
  padding: 0;
  margin: 0;
  background-color: #08090D;
  font-family: Arial, Helvetica, sans-serif;
}

body {
  margin: 0;
  padding: 0;
}

a {
    color: inherit;
    text-decoration: inherit;
}

p {
  margin: 0;
  padding: 0;
}

</style>
