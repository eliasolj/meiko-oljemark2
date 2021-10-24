<template>
    <div id="content">
    <nav>
        <Navbar />
    </nav>
        <Project />
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
nav {
    width: 99%;
    margin: auto;
}

a {
    text-decoration: none;
}

#content {
    background-color: #f0efef;
    width: 100%;
}

</style>
