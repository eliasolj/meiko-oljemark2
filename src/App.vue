<template>
    <div id="content">
        <Navbar />
        <Project />
        <Buttons />
    </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Project from './components/Project.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    Project
  },
}
</script>

<style>
a {
    text-decoration: none;
}
#content {
    background-color: #f0efef;
    width: 100%;
}
</style>
