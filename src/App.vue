<script setup>
    import Home from './components/pages/Home.vue'
    import AboutMe from './components/pages/AboutMe.vue'
    import Skills from './components/pages/Skills.vue'
    import Project from './components/pages/Project.vue'
    import Contact from './components/pages/Contact.vue'
    import Layout from './components/layouts/Layout.vue'

    import {ref} from 'vue'
    const selectedDisplay = ref(0)

    const components = [Home, AboutMe, Skills, Project, Contact]

    const onSelect = (index) => {
      selectedDisplay.value = index
    }

</script>

<template>
    <Layout :onSelect="onSelect">
      <component :is="components[selectedDisplay]" :onSelect="onSelect" class="content"/>
    </Layout>
</template>

<style scope>
  .content {
    width: 100%;
  }
  
</style>

