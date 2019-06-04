<template>
  <div class="home">
    <Hero/>
    <AboutMe />
    <Resume />
    <Education/>
    <Skills />
  </div>
</template>

<script>
import Hero from '../components/Home/Hero.vue'
import AboutMe from '../components/Home/AboutMe.vue'
import Resume from '../components/Home/Resume.vue'
import Education from '../components/Home/Education.vue'
import Skills from '../components/Home/Skills.vue'


export default {
  name: 'home',
  components: {
    Hero,
    AboutMe,
    Resume,
    Education,
    Skills
  }, 
  data() {
    return {
    }
  },
  created(){
    document.title = "Forrest Dunlap | Home";
  }
}
</script>

<style>
  .container{
    width: 85%;
    margin: auto;
  }

  .container hr{
    margin: auto;
    margin-top: 3%;
  }

@media screen and (max-width: 768px){
  .container{
    
  }
}

</style>
