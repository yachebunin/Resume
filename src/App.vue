<template>
  <div id="app">
    <section>
      <photo :info="parsedobj"></photo>
      <profile :info="parsedobj"></profile>
      <contact :info="parsedobj"></contact>
    </section>
    <section>
      <toggle @changeLanguage="changeLanguage"></toggle>
      <experience :info="parsedobj"></experience>
      <skills :info="parsedobj"></skills>
      <education :info="parsedobj"></education>
    </section>
  </div>
</template>

<script>
import photo from "./components/Photo";
import profile from "./components/Profile";
import experience from "./components/Experience";
import skills from "./components/Skills";
import education from "./components/Education";
import toggle from "./components/Toggle";
import contact from "./components/Contact";

export default {
  name: "app",
  methods: {
    changeLanguage(value) {
      this.parsedobj = JSON.parse(JSON.stringify(value));
    },
  },
  data() {
    return {
      parsedobj: {},
    };
  },
  components: {
    photo,
    profile,
    contact,
    experience,
    skills,
    education,
    toggle,
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Jura:wght@400;600&display=swap');

body {
  background: #fff;
  /* background: url('./assets/bg1.jpg'); */
  color: rgb(245, 245, 245);
  font-family: 'Jura', sans-serif;
  font-size: 28px;
  margin: 10px;
}

#app {
  position: relative;
  display: flex;
  flex-wrap: wrap;
  margin: 0px auto;
  max-width: 1290px;
}

#app > section:first-child {
  margin-right: 10px;
  max-width: 35%;
  text-align: center;
}

#app > section:last-child {
   max-width: 64%;
}

ul {
  margin: 0px;
  padding: 0px;
}

li {
  display: flex;
  flex-wrap: wrap;
}

.name_blocks-left, .name_blocks-right {
  padding: 5px 0px;
  text-align: center;
  font-size: 1.2em;
  text-transform: uppercase;
  background: #019b8b;
}

.content_blocks-left, .content_blocks-right {
  padding: 30px;
  background: #77A6F7;
}

.itemName {
  position: relative;
  margin-left: 20px;
  flex-grow: 1;
  font-size: 1em;
  text-transform: uppercase;
}

.itemName::before {
  position: absolute;
  top: -6px;
  left: -20px;
  content: "\2022";
  font-size: 1.2em;
}

.itemDate {
  font-size: 1em;
}

.itemDescription {
  margin-top: 5px;
  font-size: 1em;
  flex-basis: 100%;
  padding: 20px;
  box-shadow: 2px 2px 2px 3px #7aa8f8,
              -2px -2px 2px 3px #7aa8f8;
  margin-top: 30px;
}
</style>


<style>
  @media all and (min-width: 1280px) and (max-width: 1439px) {
    #app {
      max-width: 1150px;
    }
  }
</style>

<style>
  @media all and (min-width: 1024px) and (max-width: 1279px) {
    body {
      font-size: 20px;
    }

    #app {
      max-width: 920px;
    }

    #app > section:first-child {
      max-width: 35%;
    }

    #app > section:last-child {
      max-width: 63.91%;
    }
  }
</style>

<style>
  @media all and (min-width: 768px) and (max-width: 1023px) {
    body {
      font-size: 23px;
    }

    #app {
      max-width: 690px;
    }

    #app > section:first-child {
      margin-right: 0px;
      min-width: 690px;
    }

    #app > section:last-child {
      margin-top: 10px;
      min-width: 690px;
    }
  }
</style>

<style>
  @media all and (min-width: 0px) and (max-width: 767px) {
    body {
      font-size: 16px;
    }

    #app {
      max-width: 285px;
    }

    #app > section:first-child {
      margin-right: 0px;
      min-width: 285px;
    }

    #app > section:last-child {
      margin-top: 10px;
      min-width: 285px;
    }
  }
</style>

