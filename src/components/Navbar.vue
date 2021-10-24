<template>
    <nav>
        <span class="dot"><p id="eo">EO</p></span>
        <p id="name">Elias Oljemark</p>
        <a id="logout" href="">Kirjaudu ulos</a>
    </nav>
</template>

<script>
export default {
  name: 'Navbar',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

nav {
    background-color: #234e52;
    width: 100%;
    height: 3.5em;
    color: white;
    display: flex;
    justify-content: space-between;
}

a {
    color: white;
}


.dot {
  height: 30px;
  width: 30px;
  background-color: #950f48;
  border-radius: 50%;
  display: inline-block;
  margin-top: 10px;
  margin-left: 15px;
}

#eo {
    font-size: 1em;
    text-align: center;
    margin: auto;
    margin-top: 3px;
}

#name {
    margin-top: 1em;
    margin-left: 3.5em;
    position: absolute;
    font-size: 0.9em;
}

#logout {
    font-size: 0.9em;
    margin-top: 1em;
    margin-right: 1em;
}
</style>
