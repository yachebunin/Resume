<template>
  <div id="toggle">
    <button @click="changeLanguage()">{{lang}}</button>
    <div id="load" v-if="load">{{loadLang}}</div>
  </div>
</template>

<script>
  export default {
    name: 'toggle',
    data() {
      return {
        en: false,
        load: false,
        language: {},
      }
    },
    created() {
      import('../ru')
            .then(RU => {
              let langModule = RU;
              this.language = langModule.RU;
            })

      setTimeout(() => this.$emit('changeLanguage', this.language), 1000);
    },
    computed: {
      lang: function() {
        if (this.en) {
          return 'EN'
        } else {
          return 'RU';
        }
      },

      loadLang: function() {
if (this.en) {
          return 'Loading...'
        } else {
          return 'Загрузка...';
        }
      }
    },
    methods: { 
      changeLanguage() {
        if (this.en) {
          import('../ru')
            .then(RU => {
              let langModule = RU;
              this.language = langModule.RU;
            })
           
           this.en = false;
        } else {
          import('../en')
            .then(EN => {
              let langModule = EN;
              this.language = langModule.EN;
            })

        this.en = true;
        }

       this.load = true;

        setTimeout(() => this.$emit('changeLanguage', this.language), 1000);
        setTimeout(() => this.load = false, 1000);
      }
    },
  }
</script>

<style>
 #toggle {
   position: absolute;
   z-index: 1000;
   left: 100.6%;
   margin-top: -5px;
 }

 #toggle > button {
   padding: 7px;
   border: 1px solid #00887A;
   outline: none;
   background: #77A6F7;
   color: #fff;
   font-size: 0.5em;
 }

 #toggle > button:hover {
   cursor: pointer;
 }

 #load {
    position: absolute;
    top: 50px;
    left: 0px;
    color: #00887A;
    font-size: 1em;
    letter-spacing: 2px;
  }
</style>

<style>
  @media all and (min-width: 1280px) and (max-width: 1439px) {
    #load {
        top: 10px;
        left: -180px;
        color: #fff;
      }
  }
</style>

<style>
  @media all and (min-width: 1024px) and (max-width: 1279px) {
    #toggle {
      margin-top: -2px;
    }

    #load {
        top: 5px;
        left: -150px;
        color: #fff;
      }
  }
</style>

<style>
  @media all and (min-width: 768px) and (max-width: 1023px) {
    #toggle {
      left: 101%;
    }

    #toggle > button {
      padding: 4px;
      font-size: 0.4em;
    }

    #load {
        top: 5px;
        left: -150px;
      }
  }
</style>

<style>
  @media all and (min-width: 0px) and (max-width: 767px) {
    #toggle {
      left: 100.8%;
    }

    #toggle > button {
      padding: 2px;
      font-size: 0.4em;
    }

    #load {
        top: 3px;
        left: -100px;
      }
  }
</style>

