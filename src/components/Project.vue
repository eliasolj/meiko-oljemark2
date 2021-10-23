<template>
    <div id="container">

    <div id="info">
        <div id="teamInfo">
            <p>Seura:</p>
            <p class="teamState">Kova</p>
        </div>
        <div id="stateInfo">
            <p>Tila:</p>
            <p class="teamState">Aktiivinen</p>
        </div>
    </div>

        <div id="content">
            <h3>Projektitilanne</h3>
            <h1>{{ state.otsikko }}</h1>
            <p id="date">Tila päivitetty viimeksi: {{ state.pvm }}</p>
        </div>
        <p id="setState">Aseta tila:</p>
        <div id="buttons">
            <button class="button" v-on:click="kesken">Kesken</button>
            <button class="button" v-on:click="pidossa">Pidossa</button>
            <button class="button" v-on:click="paattynyt">Päättynyt</button>
            <p>Aseta projektin tila käyttäen ylläolveia painikkeita.</p>
        </div>
    </div>
</template>

<script>

import { reactive } from 'vue';

export default {
  name: 'Project',
  props: {
      title: String,
  },
  setup() {
    const state = reactive({
        otsikko: "KESKEN",
        pvm: new Date().toString()
    })

    const pidossa = () => {
        state.otsikko = 'PIDOSSA';
        state.pvm = new Date().toString();
    }
    
    const kesken = () => {
        state.otsikko = 'KESKEN';
        state.pvm = new Date().toString();
    }

    const paattynyt = () => {
        state.otsikko = 'PÄÄTTYNYT';
        state.pvm = new Date().toString();
    }

    return { state, pidossa, kesken, paattynyt }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

#content {
  border-radius: 25px;
  background: white;
  width: 95%;
  text-align: center;
  margin: auto;
  margin-top: 1em;
  margin-bottom: 4em;
  box-shadow: 0px 2px 5px #d8d7d7;
}


#content > h3 {
    padding-top: 1.5em;
    font-size: 1em;
    font-weight: 400;
}

#content > h1 {
    font-weight: bold;
    font-size: 2em;
    margin-bottom: 2em;
}

#buttons {
    text-align: center;
    display: grid;
}

#buttons > p {
    color: #79879b;
    font-size: 0.8em;
    margin-bottom: 100%;
}
.button {
    width: 90%;
    margin: auto;
    margin-bottom: 0.5em;
    border-radius: 10px;
    border-color: #2c7a7b;
    background-color: #2c7a7b;
    font-weight: 600;
    color: white;
    padding: 0.5em;
}

#info {
    display: flex;
    justify-content: space-between;
}

#teamInfo > p {
    margin-left: 1em;
    margin-top: 1em;
}

#stateInfo > p {
    margin-right: 1em;
    margin-top: 1em;
}

#date {
    font-weight: bold;
    color: #285e61;
    padding-bottom: 1.5em;
}

#setState {
    margin-left: 1em;
}

.teamState {
    font-weight: 700;
}
</style>
