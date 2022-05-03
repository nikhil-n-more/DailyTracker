<template>
  <heading-container :contentShown="this.contentShown"></heading-container>
  <body-container :contentShown="this.contentShown"></body-container>
  
  <div id="nav_bar">
    <div class="nav_page" id="coding" ref="coding">Coding</div>
    <div class="nav_page" id="no-fap" ref="no-fap">No-Fap</div>
    <div class="nav_page" id="tasks" ref="tasks">Tasks</div>
    <div class="nav_page" id="earnings" ref="earnings">$</div>
  </div>
</template>

<script lang="ts">
import { Vue, Options } from "vue-class-component";
import HeadingContainer from '@/components/headingContainer.vue';
import BodyContainer from '@/components/bodyContainer.vue';

@Options({
  components : {
    HeadingContainer,
    BodyContainer
  },
  data(){
    return {
      tabs : ["coding", "no-fap", "tasks", "earnings"],
    };
  },

})

export default class App extends Vue{
  public $refs : Vue['$refs'] = {
    "coding" : HTMLDivElement,
    "no-fap" : HTMLElement,
    "tasks" : HTMLElement,
    "earnings" : HTMLElement
  };

  public contentShown : String = "coding";

  public mounted(): void {

        this.$refs["coding"].addEventListener('click' , () => {
          console.log("Coding is clicked");
          this.contentShown = "coding";
        });

        this.$refs["no-fap"].addEventListener('click' , () => {
          console.log("No Fap is clicked");
          this.contentShown = "no-fap";
        });

        this.$refs["tasks"].addEventListener('click' , () => {
          console.log("Tasks is clicked");
          this.contentShown = "tasks";
        });

        this.$refs["earnings"].addEventListener('click' , () => {
          console.log("Earnings is clicked");
          this.contentShown = "earnings";
        });
    }

  public created(){
    // console.log(`The refs are ${this.$refs["coding"]}`);
  }
}
</script>

<style>

 
:root{
  --background-color: #8c52ff;
  --border-color: #c7d0d8;
}

#app {
  font-family: 'Big Shoulders Display', cursive, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  min-width: 400px;
  min-height: 500px;
  background: var(--background-color);
  padding: 0;
  margin: 0;


  display: flex;
  flex-direction: column;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

#nav_bar{
    display: flex;
    justify-content: space-around;
    padding: 30px 0;
    border-radius: 12px;
    border: 2px solid var(--border-color);
    font-size: 20px;
    color: white;
}

.nav_page{
  cursor: pointer;
}
</style>
