<script data-host="https://app.microanalytics.io" data-dnt="false" src="https://app.microanalytics.io/js/script.js" id="ZwSg9rf6GA" async defer></script>
<template>
  <div id="index" data-aos="fade-up" data-aos-duration="2000">
    <div id="greeting">
      <h1>{{greeting}}!</h1>
    </div>
    <div id="hometext">
      <p>Hi, I'm <strong>Danielle Odigie</strong>, student @ Columbia University majoring in <strong>computer science</strong> and minoring in <strong>linguistics</strong>. I'm interested in <strong>frontend development</strong> and <strong>quantum computing</strong>.</p>
    </div>
    <div class="button">
      <a href="mailto:odigiedanielle@gmail.com">email me!</a>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import aosMixin from '~/mixins/aos'

export default Vue.extend({
  mixins: [aosMixin],
  name: 'IndexPage',
  data() {
    return{
      greetings: [
        "Hello",
        "Bonjour",
        "Hola",
        "Privet",
        "Hallo",
        "Ciao",
        "Shalom",
        "Koyo"
      ],
      index: 0
    }
  },
  mounted() {
    setInterval(function(this:any) {
      this.index = Math.trunc(Math.random() * this.greetings.length)
    }.bind(this), 2000);
  },
  computed: {
    greeting: function(): string{
      return this.greetings[this.index]
    }
  }
})
</script>

<style>
  @font-face{
      font-family: 'MomcakeBold';
      src: url('../static/fonts/MomcakeBold-WyonA.otf');
  }
  @font-face{
        font-family: 'ThinLine';
        src: url('../static/fonts/Thin_Line_Font.otf');
    }

  #index{
    padding-bottom: 30px;
  }

  #greeting{
    font-family: "TypoGraphica";
    font-size: 50px;
    padding: 100px;
    padding-bottom: 5px;
    text-align: center;
  }

  #hometext{
    font-family: "ThinLine";
    font-size: 25px;
    width: 50%;
    text-align: center;
    margin: auto;
  }

  .button{
    margin: auto;
    padding-top: 1em;
    padding-bottom: 1em;
    text-align: center;
  }

  .button a{
    text-decoration: none;
    color: #061507;
    font-family: "MomcakeBold";
    font-size: 20px;
    border: solid #061507;
    background-color: #95ab90;
    color: black;
    border-radius: 15px;
    padding-left: 40px;
    padding-right: 40px;
    padding-top: 8px;
    padding-bottom: 8px;
  }

  @media only screen and (max-width: 480px){

    #greeting{
      font-size: 40px;
    }
  }
</style>
